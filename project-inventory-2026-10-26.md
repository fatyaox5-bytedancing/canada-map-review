# 拼豆图纸转换工具现状盘点报告

> 盘点日期：2026-10-26
> 目的：为接入 PixelOE / RTV / L0 / XDoG 算法升级提供现状依据（只读盘点，未修改任何代码）

## 1. 技术栈与目录结构

- **技术栈**：纯前端项目，Vue 3.5 + TypeScript + Vite 6，无后端（仅 AI 风格化走云端 API）。无任何图像处理第三方依赖，所有算法均自研（依赖仅 `vue` + `crypto-js`）
- **启动方式**：`npm run dev`（Vite，默认 5173 端口）
- **构建**：`npm run build`（`vue-tsc -b && vite build`）
- **目录结构**：

```
src/
├── App.vue                    # 主状态容器：生成管线、编辑、暂存、导出
├── coreLogic.ts               # 核心算法层（纯函数，无 DOM）
├── core/
│   ├── downsample.ts          # 下采样（纯逻辑）
│   ├── beadColors.ts          # MARD 色卡 291 色
│   ├── colorMerge.ts          # 贪心颜色合并
│   ├── colorValidation.ts     # 色号校验
│   ├── exportUtils.ts         # 图纸 PNG 导出
│   ├── referenceAlgorithm.ts  # "丰富"对比算法
│   ├── jimengService.ts       # 即梦 AI 图生图 API
│   ├── imageHostService.ts    # 图床上传（AI 流程用）
│   └── volcengineSign.ts      # 火山引擎签名
├── composables/
│   ├── useImageProcessor.ts   # 图片加载/Canvas 下采样（DOM 层）
│   ├── useAIStylize.ts        # AI 风格化流程
│   └── useDraftStore.ts       # localStorage 草稿暂存
└── components/
    ├── LeftSidebar.vue        # 参数面板
    ├── CanvasArea.vue         # Canvas 图纸渲染
    └── RightSidebar.vue       # 色号统计与编辑
reference/perler-beads-master/ # 参考项目（含色号对应表.csv，仅对照用）
```

## 2. 现有转换流程（实际调用链）

入口：`handleGenerate` → `executeGenerate`（App.vue:177）

| 环节 | 位置 | 说明 |
|---|---|---|
| 原图导入 | `loadImage()` useImageProcessor.ts:66 | FileReader → HTMLImageElement |
| 图片预处理 | ❌ **不存在** | 无平滑/去噪/线稿等任何预处理步骤 |
| 缩放/像素化 | `downsampleWithModeFromImage()` useImageProcessor.ts:142 → `downsampleWithMode()` downsample.ts:214 | Canvas 取全图像素后逐格计算；卡通模式=区域主色（`calculateDominantColor`），真实模式=区域平均色 |
| 颜色量化 | 标准算法：`removeDirtyColors()` → `quantizeColors()`（K-Means++，coreLogic.ts）；丰富算法：无量化，直接映射（referenceAlgorithm.ts:103） | App.vue:305-311 |
| 色卡映射 | `findClosestBeadColor()`（DeltaE 2000，App.vue:319-328）；丰富算法用 RGB 欧氏距离 | 映射到 `getColorsByMode()` 选定色卡 |
| 颜色合并 | `mergeColors()` colorMerge.ts:45（贪心合并到 maxColors） | 仅标准算法 |
| 网格渲染 | `CanvasArea.vue` | Canvas 2D 逐格绘制 + 色号标注 + 网格线 |
| 导出 | `exportPatternToPNG()` exportUtils.ts:109 | PNG，标准/高清/超高清三档 |

注：`coreLogic.ts` 里已有 `detectEdges`（Sobel）、`cannyEdgeDetection`、`addBlackEdge` 等边缘函数，但当前生成管线（App.vue:313 `afterOutlines = afterQuantized`）**未启用描边步骤**。

## 3. 现有功能清单

- 参数：算法（标准/丰富）、像素模式（卡通/真实）、网格宽度 5–208、最大颜色数 2–120、色卡范围（常用 234 色 / 全部 291 色）、色号标注开关、网格线开关
- AI 风格化：即梦图生图（可选，需 API key）
- 编辑：单点/选中像素换色、批量替换色号、自动匹配图内相近色号（ΔE2000）、隐藏色号、左右镜像
- 统计与导出：各色号用量统计、PNG 导出（三档尺寸）、草稿暂存与恢复
- **不支持**：多品牌色卡（仅 MARD）、图纸对比视图、线稿预览

## 4. 新算法接入初步评估

整体架构判断：管线分层良好——`core/` 为纯函数算法层（无 DOM），`useImageProcessor` 为 DOM 桥接层，`App.vue` 为编排层。新算法以"ImageData → ImageData"或"RGB矩阵 → RGB矩阵"的纯函数形式插入是可行的。

| 算法 | 可行性 | 接入位置 | 主要风险/待核查 |
|---|---|---|---|
| **PixelOE**（细节保留像素化） | ⚠️ 中 | 替换/并列 `downsampleWithModeFromImage`（第 2 环节），作为第三种像素化模式 | 官方实现为 Python（PyTorch/Numpy 重度依赖）。JS 移植工作量大；无现成 npm 包。需确认：用纯 JS 重写哪个子集？或是否考虑 onnxruntime-web / WebAssembly？**依赖风险最高的一项** |
| **RTV**（相对总变差平滑） | ✅ 中高 | 新增第 1.5 环节"预处理"：在 `downsampleWithModeFromImage` 之前对原图 ImageData 平滑 | RTV 需解大型稀疏线性方程组，JS 无现成实现，需自研迭代求解器；大图（>2000px）在浏览器中可能慢，可能需要 Web Worker |
| **L0**（L0 梯度最小化平滑） | ✅ 中高 | 同 RTV，二选一或并存为预处理选项 | 比 RTV 更易 JS 实现（逐像素+FFT 或分离逼近）；同样有性能风险，建议 Worker 化 |
| **XDoG**（线稿提取） | ✅ 高 | 独立模块 `core/xdog.ts`，输入 ImageData 输出线稿；可在 UI 加"线稿预览" | 高斯差分+阈值，纯卷积运算，JS 实现直接；项目已有 Sobel/Canny 实现可作基础设施参考；风险低 |
| **XDoG 引导 PixelOE** | ⚠️ 待验证 | 位置上有空间：XDoG 输出可作为下采样时的区域分割权重或描边叠加（`addBlackEdge` 已预留类似位置） | PixelOE 官方并无线稿引导机制，这是自定义研究项；需先确定引导的数学形式（加权采样？边缘约束量化？） |

**共性问题需先确认**：
1. 三个算法（PixelOE/RTV/L0）均无成熟 JS/npm 实现——是接受"自研移植"，还是考虑引入 Python 后端服务？这是方向性决策
2. 是否允许引入 Web Worker / WASM / onnxruntime-web 等运行时依赖？
3. 新算法参数如何进 UI（LeftSidebar 目前只有滑条/单选，结构简单可扩展）

## 5. 升级时必须保护的现有功能

1. **暂存/恢复**：`useDraftStore` + App.vue 的 visibilitychange/watch 保存逻辑，恢复时依赖 `syncDraftState` 同步 composable ref——新增状态字段需同步更新草稿 schema（key: `dotplanet_draft_v1`）
2. **两套生成算法流程**：`processWithPerlerPlanetAlgorithmFlow` 和 `processWithReferenceAlgorithmFlow`（用户已熟悉"标准/丰富"选项）
3. **编辑功能**：gridMatrix 为唯一事实源，替换/镜像/隐藏色号/自动匹配均直接操作它，新管线输出格式必须是同一 `GridCell[][]` 结构
4. **导出**：`exportPatternToPNG` 依赖 gridMatrix + beadStats 结构
5. **色卡**：`beadColors.ts` 291 色号数据（前导零格式问题已记录但未修，改动会影响历史草稿里的 code 匹配）
6. **四级参数联动**：`watch(gridWidth)` 自动重算 gridHeight 的逻辑

## 6. 尚不确定、需进一步核查的问题

1. PixelOE/RTV/L0/XDoG 采用纯前端 JS 实现还是引入后端？（决定架构方向）
2. 是否允许引入 Web Worker / WASM / onnxruntime-web 等运行时依赖？
3. XDoG 引导 PixelOE 的具体数学机制，需要先看 PixelOE 论文/源码确认可干预的位置
4. 性能基线：当前最大网格 208 列、原图分辨率上限未做限制，新算法在典型原图（1–4K）上的耗时未测量
5. 草稿 schema 版本化策略（新增算法参数后旧草稿如何兼容）

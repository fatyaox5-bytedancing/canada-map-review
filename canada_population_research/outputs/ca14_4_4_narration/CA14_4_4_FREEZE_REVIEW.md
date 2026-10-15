# CA-14.4.4 冻结审查报告（V4 → V5）

**性质**：最后一轮微修订。本文档记录**修改前后文本、敏感性检验结果及未解决风险**，供人工确认冻结 `CA14_4_4_NARRATION_V5_CANDIDATE.md`。

**未生成**分镜、图片、地图、音频或视频；**未覆盖** V1 / V2 / V3 / V4 及任何历史版本。

**输入**：`CA14_4_3_NARRATION_V4_CANDIDATE.md`、`CA14_4_3_FINAL_CHECK_REPORT.md`，以及 CA-04A 机器可读产物（`_ca04a_centres.csv`、`_ca04a_stats.json`）。

---

## 一、修改汇总

| # | 位置 | 改动性质 | 词数变化 |
|---:|---|---|---:|
| 1 | 第 1 章 1.4 | 表达澄清 | +3 |
| 2 | 第 3 章 3.1 | **分母与份额类型澄清** | +11 |
| 3 | 第 3 章 3.5 | **量化解模糊 + 补免责说明** | +48 |
| 4 | 第 3 章 3.3 | **删除经不起敏感性检验的倍数** | +17 |
| — | 第 5 章 5.1 | 与第 3 章口径一致化 | +8 |

**全片词数**：V4 **871** → V5 **958**（**+87**）

| 章 | V4 | V5 | 135 wpm | 140 wpm | 150 wpm |
|---:|---:|---:|---:|---:|---:|
| 1 | 112 | **115** | 51 s | 49 s | 46 s |
| 2 | 152 | **152** | 68 s | 65 s | 61 s |
| 3 | 278 | **354** | 157 s | 152 s | 142 s |
| 4 | 162 | **162** | 72 s | 69 s | 65 s |
| 5 | 167 | **175** | 78 s | 75 s | 70 s |
| **合计** | **871** | **958** | **426 s** | **411 s** | **383 s** |

**关于时长的如实说明**：按任务要求**未为满足 379 秒而填充或删减内容**，但必须指出 V5 在 135 wpm 下估算为 **426 秒**，已明显超出 379 秒。

**增量几乎全部来自第 3 项（+48 词）**：把 `the gap disappears` / `nothing` 改为明确的采样点计数，并加上「不等于中间的土地是空的」这句免责说明，在英文里必然要占用字数。这属于**任务明确要求的澄清**，不是填充。

**若人工希望压缩，最可压缩处是第 3 章 3.5**（见 §七 待裁定项），但压缩会重新引入模糊表达。**本稿不自行压缩。**

> ⚠️ **所有时长为按词数估算，无任何实测。** 本项目 TTS 路径被沙箱阻断（CA-13.4 已穷尽 6 条路径），**没有任何一段旁白被实际试读或合成过**。

---

## 二、第 1 项｜第 1 章六中心表述

**V4（被替换）**

> The six largest, and not one of them next to another. So where is everybody?

**问题**：`not one of them next to another` 是以**否定**方式表达「彼此相距遥远」，在英语口语中容易读作「它们互不相邻」这种弱表述，没有传达出 2,700 公里中位数所代表的实际距离感。

**V5（采用）**

> The six largest are spread far apart, from the Pacific coast to the Atlantic. So where is everybody?

**依据**：六个中心中最西的 Vancouver（lon −122.90）位于太平洋沿岸省份，最东的 Montréal / Ottawa-Gatineau（lon −73.67 / −75.68）位于大西洋方向；用 `from the Pacific coast to the Atlantic` 描述其跨度是地理上成立的。

---

## 三、第 2 项｜第 3 章 59% 的分母与份额类型

**V4（被替换）**

> Inside the map we drew for that corridor, four hundred and fourteen population centres hold fifty-nine percent of the total.

**问题（两重歧义）**：

1. **分母歧义**：`of the total` 未指明是加拿大人口中心合计人口，还是加拿大总人口。
2. **份额类型歧义（更隐蔽）**：`four hundred and fourteen population centres hold fifty-nine percent` 中，主语是「中心」，容易读成**「414 个中心占全部中心数量的 59%」**。这是完全错误的——414 与 1,026 是不同口径的两个数，**且 CA-14.3 已记录 414 与 424 的集合关系都无法证明**。

**V5（采用）**

> Inside the map we drew for that corridor, four hundred and fourteen population centres hold about fifty-nine percent. That is a share of the people in Canada's population centres — not of the country's population, and not of the number of centres.

**处理要点**：

- ✅ **份额类型明写**：`a share of the people in Canada's population centres`（是**人口份额**）。
- ✅ **两种错误读法逐一排除**：`not of the country's population, and not of the number of centres`。
- ✅ **补 `about`**：58.67% → 旁白念「约 59%」，与既有取整口径一致。
- ✅ **第 5 章 5.1 同步口径一致化**：`One corridor in the east: about fifty-nine percent of the people in Canada's population centres.`

**口径复核**：17,829,125 ÷ 30,389,999 = **58.6677%** → 旁白「约 59%」✅；分母 = 1,026 个人口中心的合计人口 ✅

---

## 四、第 3 项｜第 3 章采样阈值的量化

**V4（被替换）**

> Then the line turns to Montreal, and the gap disappears. Across a hundred and fifty-seven kilometres, not one sample point is beyond the limit. And Montreal to Quebec City: nothing. Zero percent, across two hundred and thirty-two kilometres.

**问题**：

1. `the gap disappears` 是**因果/状态式**表述，仿佛空隙被填上了。
2. `nothing` 极其模糊——可被理解为「中间什么都没有」「没有聚落」。
3. `not one sample point is beyond the limit` 未给出采样点**总数**，观众无法判断「零」是在多大的样本上得到的。

**V5（采用）**

> Then the line turns to Montreal, and the picture changes. Sampling the same way from Ottawa to Montreal, across a hundred and fifty-seven kilometres, none of the thirty-two sample points has its nearest population centre beyond twenty-five kilometres. And from Montreal to Quebec City, over two hundred and thirty-two kilometres, again none of the forty-seven. Along those two stretches, every sample point stays within twenty-five kilometres of some population centre. That measures the spacing of these centres. It does not mean the land between them is empty.

**处理要点**：

- ✅ 改为**明确的测量结果**：`none of the thirty-two sample points`、`none of the forty-seven`。
- ✅ **给出采样点总数**，使「零」有分母。
- ✅ **阈值写全**：`beyond twenty-five kilometres`。
- ✅ **补免责说明**：`That measures the spacing of these centres. It does not mean the land between them is empty.`
- ✅ **`the gap disappears` / `nothing` 全部删除**（程序化检索 0 处）。

### 4.1 ⚠️ 本次核验中发现并修正的一处数字错误

在改动过程中我一度把采样点数写成「71 个（渥太华→蒙特利尔）」与「65 / 41 个」，**回查 `_ca04a_stats.json` 后确认这是错的**。该文件第 1023–1048 行的三段记录为：

| 段 | `length_km` | `n_samples` | 隐含采样间距 |
|---|---:|---:|---:|
| Toronto → Ottawa-Gatineau | 354.8262 | **71** | 5.0 km ✅ |
| Ottawa-Gatineau → Montréal | 157.3978 | **32** | 4.9 km ✅ |
| Montréal → Québec | 232.2349 | **47** | 4.9 km ✅ |

**结论**：`71` 属于 **Toronto → Ottawa** 那一段（即第 3 章 3.4 所述「每隔 5 公里取一个采样点」的那一段），**不是** 157 km 段；157 km 段存的是 **32** 点。V5 已按 32 / 47 改写。

**同时注意 3.4 与 3.5 的采样点数不同（71 vs 32、47）**，原因是各段长度不同、采样间距同为约 5 km。旁白未声称各段点数相同。

---

## 五、第 4 项｜经度带边界敏感性检验（本次实际执行）

### 5.1 方法与一个必须说明的方法论修正

现有脚本 `ca04a_analyze.py` 的分箱口径为 `round(lon*2)/2`，其箱边界落在 lon = …, .25, .75, …。

> ⚠️ **第一次尝试我用了错位半个箱宽的方案（`floor(lon*2+0.5)/2`），结果两组数字完全没变。原因是：错位半个箱宽只是给同一个划分重新编号，**统计量在数学上必然不变**——那不是一次有效的敏感性检验。**已废弃该方案。**

**有效做法**：让箱边界**穿过数据点**，即错位四分之一箱宽（±0.25°），边界移到 lon = …, .0, .5, …。这仍是同一分箱函数的平移，**未构成新的空间分析**，未扩大项目范围。

### 5.2 检验结果

| 口径 | 边界位置 | Toronto 带 n | Toronto 中位 | 以西四带 n | 以西中位 | **比值** |
|---|---|---:|---:|---:|---:|---:|
| **A 原口径** `round(lon*2)/2` | .0 / .5 | **31** | **6,507** | **109** | **4,227** | **1.5394** |
| B 错位 −0.25° | .5 / .0 | 28 | 7,517 | 116 | 4,189 | **1.7946** |
| C 错位 +0.25° | .25 / .75 | 34 | 6,481 | 98 | 3,764 | **1.7217** |

**比值范围 = 1.5394 ~ 1.7946（极差 0.2552）**

### 5.3 检验结论：**不稳定**

- ❌ **「约 1.5 倍」这一说法不稳健。** 在 B 口径下比值变成 **1.79 倍**，与 1.5 倍相差 **19.6%**。若旁白念「约 1.5 倍」，在另一种同样合理的分箱定义下就是不准确的。
- ❌ **中位数值本身也不稳健**：西侧中位在 **3,764 ~ 4,227** 之间浮动（相对原口径变化 **11.0%**）；Toronto 侧在 **6,481 ~ 7,517** 之间浮动。
- ❌ **组内样本量也不稳健**：以西四带的中心数在 **98 ~ 116** 之间浮动；Toronto 带在 **28 ~ 34** 之间浮动。
- ✅ **但方向始终一致**：三种口径下比值**全部大于 1.5**（1.54 / 1.72 / 1.79），即「Toronto 带的中位中心比西侧大」这一**方向**是稳健的。

### 5.4 据此对旁白做的处理

**V4（被替换的末句）**

> The median population centre in Toronto's band is only about one and a half times the size of the median one to the west — small, in both places.

**V5（采用）**

> That average is pulled up by a few very large centres — Toronto itself accounts for five and a half million of the six and a quarter million. The median population centre in that band is not much bigger than the median one to the west.

**处理逻辑**：

- ❌ **删除「about one and a half times」**——敏感性检验证明该倍数取决于分箱边界，不宜在旁白中给出具体数值。
- ✅ 改为**单调比较** `is not much bigger than`。该表述在三种口径下都成立（比值 1.54 ~ 1.79，均属「大一些但不算悬殊」）。
- ✅ **改用无需分箱的硬数据来支撑「均值被拉高」**：Toronto 本身 5,647,656 人 ÷ 该带合计 6,223,244 人 = **90.8%**。该比值是对单个中心的直接读取，**不依赖任何分箱边界，因此完全稳健**。
- ✅ 保留「不是所有中心都更大」的核心限定。

### 5.5 未做的部分（如实披露）

- 本次只做了**网格原点的两类错位**（±0.25°），**未穷举全部可能的箱边界定义**。
- **未做**纬度方向的分箱敏感性检验。
- **未做**「改为按人口等分位数分组」等替代分组的检验。
- 样本量小（Toronto 带 n = 28 ~ 34），中位数对个别中心的进出较敏感。

---

## 六、保持不变的内容（逐项确认）

| 项 | V5 状态 |
|---|---|
| 五章结构 | ✅ 未改（1 A Country That Looks Empty / 2 Two Squares / 3 One Corridor, Two Different Things / 4 The Other Half / 5 What This Map Does and Doesn't Say） |
| 六个最大中心的 **15 组两两距离中位数约 2,698.1 km** | ✅ 未改 |
| 两个 200 km × 200 km 网格、**80,000 km²**、**43%** | ✅ 未改，分母写明 |
| **414** 个走廊中心 / 旁白约 **59%** / 画面 **58.7%** | ✅ 未改；分母与份额类型本次已明确 |
| 走廊主证据 **51.8 km / 21.1%**、最大空缺 **52 km**、段长 **232 km** | ✅ 未改 |
| 第 3 章 3.3 的**平均规模表述**（约 20 万 vs 约 2.7 万） | ✅ 未改；本次**新增**了一个核验值 90.8%（见 §5.4），它只出现在报告中，旁白用的是等价的容量表述「550 万 / 625 万」 |
| 省级百分比分母 = **1,026 个人口中心合计人口** | ✅ 未改（`not of Canada` 保留） |
| 34 个中心的 **561 组**两两距离中位数约 **1,400 km** | ✅ 未改 |
| 北部两口径 **12 / 69,029** 与 **14 / 71,592**，0.24% | ✅ 未改，两口径独立 |
| 不增加未经核验的成因解释 | ✅ 0 处；第 3 章新增句为纯测量学陈述 |
| 不继续追查 414 与 424 的集合关系 | ✅ 旁白 0 处出现 424；报告仅在解释歧义时提及 |
| 不恢复未核验的面积类比 | ✅ 0 处 Ireland；`northern third` 未回归 |
| 不为 379 秒填充或删减 | ✅ 见 §一 说明 |

---

## 七、未解决风险与待裁定事项

### 7.1 待人工裁定（冻结前）

| # | 事项 | 本稿处理 | 需要决定什么 |
|---:|---|---|---|
| 1 | 全片 135 wpm 估算 **426 秒**，超出 379 秒 | 未自行压缩 | 是否接受；或指定压缩第 3 章 3.5（可省约 40 词，但会重新引入模糊） |
| 2 | 第 3 章倍数的处理 | 改为单调比较，删除 1.5 倍 | 是否同意不再给出具体倍数 |
| 3 | `from the Pacific coast to the Atlantic` | 采用 | 是否接受该地理跨度表述 |
| 4 | 3.4 与 3.5 采样点数不同（71 / 32 / 47） | 按各段实际值写 | 是否需要在画面上标注各段采样点数 |

### 7.2 仍然存在的口径残留（不影响旁白正确性，但需入档）

1. **经度带比较的纬度带不同**：Toronto 带纬度跨度 3.40°，以西四带 4.08°。
2. **以西四带被 BOUNDS 西界（lon −81.6）截断**：lon −81.75 ~ −81.6 另有 **8 个中心 / 41,188 人**未计入。
3. **以西四带的分组本身随边界定义变化**（98 / 109 / 116 个中心），因此「四个带」这一分组不宜被当作固定事实陈述——V5 旁白保留该表述，因为它与画面所用的具体分箱一致。
4. **414 与 424 的成员关系仍无法证明**，本次按任务要求**未再追查**。
5. **画面精确值 58.7% 与旁白 59% 并存**，沿用 CA-14.4.1 起的既有裁定，本次未变。

### 7.3 技术限制

1. **所有时长为按词数估算，无实测。** 无任何旁白被真正朗读过。
2. **英文为书面稿，未经英语母语者朗读测试。**
3. **`PCCLASS` 官方含义未确认**；V5 避开依赖该码值的表述。
4. **population centre 的官方定义文本本项目未取得**，V5 只说 `A population centre is where people are concentrated`。

---

## 八、程序化纪律自检结果

（对 V5 英文正文运行，非人工目视）

| 检查项 | 结果 |
|---|---|
| city / cities（人口中心称谓） | **0** ✅（Quebec City 作地名 2 次，已剔除） |
| metropolitan / metro / CMA / urban area / built-up area | **0** ✅ |
| scattered / isolated / remote | **0** ✅ |
| **`the gap disappears`** | **0** ✅（本次删除） |
| **`nothing`** | **0** ✅（本次删除） |
| **`not one of them next to another`** | **0** ✅（本次删除） |
| **`one and a half times` / `1.5 times`** | **0** ✅（敏感性检验后弃用） |
| `Most of those places` / `all in the east` | **0** ✅ |
| `northern third` / `two-tenths of one percent` | **0** ✅ |
| `the distance between any two of them` | **0** ✅ |
| 18.12 / Gini / 0.8843 / 0.80 | **0** ✅ |
| 424 / 226 km / 53.8 / 24.8 / 17,859,490 | **0** ✅ |
| island of Ireland | **0** ✅ |
| 1.5394 / 1.79 / 1.72（敏感性检验的过程值不入旁白） | **0** ✅ |
| 0.2356 / 2,698.1（应口播取整而非原值） | **0** ✅ |
| 必需表述 26 项 | **全部在位** ✅ |

> **综合自检结果：通过。**

---

## 九、本次执行的只读计算

1. **分箱边界敏感性检验**：以两个错位量（±0.25°）重算 Toronto 带与其以西四带的中位中心规模 → 比值 1.5394 / 1.7946 / 1.7217，判定**不稳定**，据此从旁白中删除具体倍数。
2. **采样点数复核**：回查 `_ca04a_stats.json` 第 1023–1048 行，确认三段 `n_samples` 为 **71 / 32 / 47**，并据此修正了旁白中一度写错的采样点数。
3. **Toronto 占比计算**：5,647,656 ÷ 6,223,244 = **90.8%**，用于支撑「均值被少数超大中心拉高」这一表述（该比值不依赖分箱边界）。
4. **59% 分母复核**：17,829,125 ÷ 30,389,999 = **58.6677%** → 约 59%。

**未执行**：未重跑空间分析；未做多边形裁剪；未做纬度方向或替代分组的敏感性检验；未追查 414 与 424 的集合关系；未改任何已有文件；未生成分镜、图片、地图、音频或视频。


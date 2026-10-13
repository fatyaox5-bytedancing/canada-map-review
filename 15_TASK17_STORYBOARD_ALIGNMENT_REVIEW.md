# 15 · Task 17 分镜对齐审查报告

> **文件性质**：审查报告，只读结论。**未修改**任何既有文件——未改 V1／V2 旁白稿、未覆盖分镜表、未改动任何音频、未生成新旁白、未制作 BGM 或混音。
> **生成时间**：2026-10-13T10:28:34Z｜审计脚本 `_dsh-watch/task17-align-review.py`（本报告全部数字由该脚本从实际文件算出）

## 0. 核对依据（实际文件，非转述）

| 文件 | sha256 | 说明 |
| --- | --- | --- |
| `BehindTheBreakdown/docs/04_TRICOLOR_SCRIPT_V2.md` | `c3a5b9da2788a2a54eafd2b9330e961cc5600dab4f5cb1aa838f12db175dafd2` | 唯一正式旁白稿；任务书给定前缀 `C3A5B9DA2788A2A5` —— **实测匹配：是（大小写不敏感比较）** |
| `BehindTheBreakdown/docs/05_TRICOLOR_STORYBOARD_V1.md` | `6f21d524c38f963d7fe33d48d94eeb0febc60f0940bf748a015897f98efad2ef` | 被审查的分镜表 |
| `BehindTheBreakdown/assets/audio/narration/tencent-101050/ch01.wav` | `ea9b566bde289de437e3a5e867731f6f72a80441e7d7b3ad6016426b9f0d8e1f` | 第一章音频（Task A 的唯一音频源） |
| `BehindTheBreakdown/assets/audio/narration/tencent-101050/ch01.timings.json` | `b0112bb5d5ce907b2c56bbfa334150fa30db5107f8b22e0adc99a1efc2c5e4c7` | 词级时间戳，253 条 |
| `BehindTheBreakdown/assets/audio/narration/tencent-101050/narration_report.json` | `d452e760c88f9dbdf891c3764de9a52db160490638779f9f7edb087eb1ecd31f` | 全 8 章时长 |

- 第一章音频实测：1462880 帧 / 16000 Hz = **91.430 秒**
- 全片音频：11m25.2s，8 章，9919 字符
- 词条件字符流与正文逐字符比对：**一致**（否则脚本会中止，时间码不可能给出）

---

## 1. 实际镜头总数及核对依据

- **实际镜头数：13 个**，编号 01–13。
- 核对依据：机械解析 `05_TRICOLOR_STORYBOARD_V1.md` 第 1 节表格中**以两位数字编号开头的行**，得 13 行；另有 1 行非镜头行（表格末尾的「（说明）」行，非镜头）。
- **与文档声称一致**：05 号文件第 0 节声称「镜头编号 ✅ 已完整（13 个）」，实测 13 个，**相符**。
- ⚠️ 更正本会话早前的一句话：我曾据一个错误正则说「按行匹配到 11 行」，那是因为表格首列是 `| 01 |` 而非 `| 镜头 |`。**以本次机械核对为准：13 个。**

## 2. 全片各章节覆盖情况

| 章 | 章节标题 | 旁白字符 | 音频 | 分镜 | 镜头数 |
| --- | --- | --- | --- | --- | --- |
| 1 | The Business Behind the Collapse | 1352 | ✅ 91.4s | ✅ | 13 个 |
| 2 | From Car Loans to Financial Securities | 1681 | ✅ 118.6s | ❌ | **无（未建立）** |
| 3 | When the Same Loans Support More Than One Deal | 1275 | ✅ 82.2s | ❌ | **无（未建立）** |
| 4 | What Investigators Allege Happened | 1446 | ✅ 102.8s | ❌ | **无（未建立）** |
| 5 | When Funding Dries Up | 1333 | ✅ 93.6s | ❌ | **无（未建立）** |
| 6 | The Legal Cases | 838 | ✅ 64.9s | ❌ | **无（未建立）** |
| 7 | The Weak Point in the System | 1119 | ✅ 73.8s | ❌ | **无（未建立）** |
| 8 | What the Collapse Leaves Behind | 875 | ✅ 57.8s | ❌ | **无（未建立）** |

**结论**：分镜表只覆盖**第 1 章**（13 个镜头对应第一章 6 个段落）。**第 2–8 章没有任何镜头行**——这 7 章有旁白稿也有音频，但没有分镜。任务要求的「对全部 8 章进行对齐审查」中，**第 2–8 章无对齐对象可审**，此为本任务的硬性边界，不是遗漏。

## 3. 各镜头旁白与 V2 的匹配结果

| 镜头 | 旁白单元格类型 | 是否在 V2 第 1 章中逐字找到 | 定位到的原文片段 |
| --- | --- | --- | --- |
| 01 | 逐字引用 | ✅ 是（125 字符，`In` → `bank`） | `In the United States, some used-car dealers do more than s…` |
| 02 | 非逐字（无英文可定位） | ❌ 否 | `（单元格无英文引用，仅中文说明）` |
| 03 | 逐字引用 | ✅ 是（122 字符，`Tricolor` → `histories`） | `Tricolor was one of those businesses. Based in Texas, it s…` |
| 04 | 逐字引用 | ✅ 是（141 字符，`But` → `investors`） | `But the business did not depend only on customers making t…` |
| 05 | 逐字引用 | ✅ 是（111 字符，`Here` → `back`） | `Here is how it works. A lender makes hundreds or thousands…` |
| 06 | 逐字引用 | ✅ 是（53 字符，`it` → `funding`） | `it can group those loans together and use them to obtain f…` |
| 07 | 子串引用（英文片段） | ✅ 是（23 字符，`group` → `together`） | `group those loans together` |
| 08 | 逐字引用 | ✅ 是（78 字符，`In` → `buy`） | `In a securitization, the loans are packaged into financial…` |
| 09 | 子串引用（英文片段） | ✅ 是（50 字符，`packaged` → `buy`） | `packaged into financial securities that investors can buy` |
| 10 | 逐字引用 | ✅ 是（53 字符，`The` → `loans`） | `The lender gets money upfront, which can help finance more…` |
| 11 | 逐字引用 | ✅ 是（39 字符，`That` → `legitimate`） | `That arrangement can be perfectly legitimate.` |
| 12 | 逐字引用 | ✅ 是（128 字符，`But` → `clear`） | `But it depends on a basic assumption: the loans must exist…` |
| 13 | 逐字引用 | ✅ 是（254 字符，`Tricolor` → `funding`） | `Tricolor filed for Chapter 7 bankruptcy on September 10, 2…` |

**未能定位的镜头：2**——这些镜头的旁白来源需人工确认（见第 7 节）。

## 4. 建议时间码及其证据来源

时间码来源：`ch01.timings.json` 的**词级时间戳**。做法是把该镜头旁白文本归一化后在第一章正文的归一化字符流中定位，取首词 `BeginTime` 与末词 `EndTime`。**未使用任何按字数或语速的估算。**第一章在 `full_narration.wav` 中从 0 开始，故下表时间码对 `ch01.wav` 与 `full_narration.wav` **同时成立**。

| 镜头 | 旁白段 | 建议起始 | 建议结束 | 时长 | 证据 |
| --- | --- | --- | --- | --- | --- |
| 01 | Ch1·段1 | `00:00.250` | `00:10.040` | 9.79s | 逐字定位（词级时间戳） |
| 02 | Ch1·段1 | `PENDING_REVIEW` | `PENDING_REVIEW` | — | 单元格未引用英文原文，无法定位 |
| 03 | Ch1·段2 | `00:10.570` | `00:20.640` | 10.07s | 逐字定位（词级时间戳） |
| 04 | Ch1·段3 | `00:21.240` | `00:31.110` | 9.87s | 逐字定位（词级时间戳） |
| 05 | Ch1·段4 | `00:31.690` | `00:40.530` | 8.84s | 逐字定位（词级时间戳） |
| 06 | Ch1·段4 | `00:41.080` | `00:44.720` | 3.64s | 逐字定位（词级时间戳）；⚠️ 与镜头 07 **时间重叠** |
| 07 | Ch1·段4 | `00:41.470` | `00:42.920` | 1.45s | 逐字定位（词级时间戳）；⚠️ 与镜头 06 **时间重叠** |
| 08 | Ch1·段4 | `00:45.220` | `00:50.940` | 5.72s | 逐字定位（词级时间戳）；⚠️ 与镜头 09 **时间重叠** |
| 09 | Ch1·段4 | `00:47.790` | `00:50.940` | 3.15s | 逐字定位（词级时间戳）；⚠️ 与镜头 08 **时间重叠** |
| 10 | Ch1·段4 | `00:51.610` | `00:55.590` | 3.98s | 逐字定位（词级时间戳） |
| 11 | Ch1·段5 | `00:56.230` | `00:58.750` | 2.52s | 逐字定位（词级时间戳） |
| 12 | Ch1·段5 | `00:59.280` | `01:09.830` | 10.55s | 逐字定位（词级时间戳） |
| 13 | Ch1·段6 | `01:10.360` | `01:31.180` | 20.82s | 逐字定位（词级时间戳） |

### 4.1 镜头 01／02 的切分建议（需人工确认）

表格中**镜头 01 引用的是整个段 1（两句话）**，而镜头 02 的说明写「段 1 后半」。因此两镜头的时间码**必须由人工确定切分点**；下表给出按句边界的机械定位结果作为依据：

| 段 1 的句子 | 起始 | 结束 | 时长 |
| --- | --- | --- | --- |
| `In the United States, some used-car dealers do more than…` | `00:00.250` | `00:04.730` | 4.48s |
| `They also lend money to customers who may struggle to ge…` | `00:05.360` | `00:10.040` | 4.68s |

**建议**：镜头 01 = 第 1 句，镜头 02 = 第 2 句。此切分点位置本身有词级时间戳作证，但**是否采用该切分属创作决定，标记 `PENDING_REVIEW`**。

### 4.2 镜头 11／12 的切分

段 5 的两句话恰好对应镜头 11 与镜头 12，**无需人工决定**：

| 段 5 的句子 | 对应镜头 | 起始 | 结束 | 时长 |
| --- | --- | --- | --- | --- |
| `That arrangement can be perfectly legitimate.` | 11 | `00:56.230` | `00:58.750` | 2.52s |
| `But it depends on a basic assumption: the loans mu…` | 12 | `00:59.280` | `01:09.830` | 10.55s |

## 5. 旧文本与 V2 的差异

- 分镜表中出现 `V1` 字样的行：**4 行**，逐行核对如下：

  - 第 1 行：# 05 · Tricolor 第一章开场分镜表 V1
  - 第 5 行：> **【文件名说明】** 本文件名保留 `V1`，系按任务指示**不重命名**。文件名为历史遗留，**内容基准已切换为旁白 V2**。若后续要改名，须单独授权，并同步 `04`、`10`、`11` 中的链接与 `../README.md` 索引。
  - 第 11 行：> **本次更新范围**：仅更新本文件。**未修改** `04_V2`、V1、`06`、`07`、`08`、`09`、`10`、`11`、`12`。
  - 第 161 行：9. ⬜ **确认配音采用 V2**，禁止使用 V1（V1 含已删除的 Chu 审判日期等修正前表述）。

**判定**：这些 `V1` 字样**全部是免责声明**——说明「V1 已不作为本表依据、禁止用于配音」。**没有一处是把 V1 的文本当作旁白内容填进镜头单元格。**

- 第 1 章旁白不含 V1 独有的争议内容（`Chu`）：该字样在分镜表中共命中 **4 行**，全部是免责声明文字（见上表）；在 13 个镜头的**旁白单元格中命中 0 处**（命中镜头：无）。实测 V1 稿中确含该内容：是——第一章旁白不涉及该内容，故本表不存在把 V1 争议文本混入旁白的风险。
- **派生发现（与 `11` 号文件矛盾）**：`11_TRICOLOR_PREPUBLICATION_CHECK.md` 第 7 节 A1 行称「分镜表仍指向 V1，且其 13 个镜头的旁白／时间码字段为『待补充』」。**实测：旁白字段已填入且为 V2 逐字**（13/13 可定位），仅**起止时间**字段仍为「待补充」。11 号文件的该表述**已过时**，且与 05 号文件自身声明的 `ALIGNED_TO_V2` 冲突。**本任务不修改 11 号文件**，仅记录。

- 章级时间码表述差异：05 号文件第 97 行称第一章章级时间码为 `00:00–01:30`，**实测音频为 91.43 秒（01:31.430）**，差 1.43 秒。建议按实测值更新。

## 6. 缺失画面与授权问题

| 镜头 | 素材类型 | 磁盘上是否有画面 | 授权字段（表中） | 判定 |
| --- | --- | --- | --- | --- |
| 01 | `STOCK_FOOTAGE` | ❌ **无文件** | `PENDING_REVIEW` | `PLANNED` |
| 02 | `STOCK_FOOTAGE` | ❌ **无文件** | `PENDING_REVIEW` | `PLANNED` |
| 03 | `MAP` | ❌ **无文件** | `PENDING_REVIEW` | `PENDING_REVIEW` |
| 04 | `ORIGINAL_ANIMATION` | ✅ `ch1_shot04.png` | 原创，无第三方授权要求 | `PLANNED` |
| 05 | `ORIGINAL_ANIMATION` | ✅ `ch1_shot05.png` | 原创，无第三方授权要求 | `PLANNED` |
| 06 | `ORIGINAL_ANIMATION` | ✅ `ch1_shot06.png` | 原创，无第三方授权要求 | `PLANNED` |
| 07 | `ORIGINAL_ANIMATION` | ❌ **无文件** | 原创，无第三方授权要求 | `PENDING_REVIEW` |
| 08 | `ORIGINAL_ANIMATION` | ❌ **无文件** | 原创，无第三方授权要求 | `PENDING_REVIEW` |
| 09 | `ORIGINAL_ANIMATION` | ❌ **无文件** | 原创，无第三方授权要求 | `PENDING_REVIEW` |
| 10 | `ORIGINAL_ANIMATION` | ✅ `ch1_shot10.png` | 原创，无第三方授权要求 | `PLANNED` |
| 11 | `ORIGINAL_ANIMATION` | ✅ `ch1_shot11.png` | 原创，无第三方授权要求 | `PLANNED` |
| 12 | `ORIGINAL_ANIMATION` | ✅ `ch1_shot12.png` | 原创，无第三方授权要求 | `PLANNED` |
| 13 | `ORIGINAL_ANIMATION` | ❌ **无文件** | 原创，无第三方授权要求 | `PLANNED` |

- 磁盘实况：`assets/animations/` 内只有 **6 个 PNG**，对应镜头 04, 05, 06, 10, 11, 12；**其余 7 个镜头（01, 02, 03, 07, 08, 09, 13）没有任何画面文件**。
- **这 6 个文件是静态图，不是动画**：`ch1_animation_manifest.json` 中 `status == STILL_GENERATED` 的有 **6/6 条**，生成环境为 `ffmpeg: not installed`、`video_encoder: none`，每条的 `known_limitation` 均记明 `still image only`。表中「主要制作方式」写的是「代码动画」，**目前实际产出物为静态帧**，二者存在差距，建议在表中如实标注。
- 分镜表声明「贷款组合到证券化动画（镜头 07–09）已完成」，但**项目目录内不存在对应文件**（doc 13 §5 亦已核实为「资产不存在」）。该三项仍为 `PENDING_REVIEW`。
- 授权纪律：`ORIGINAL_ANIMATION` 判为「无第三方授权要求」只是**初步判定**，05 号文件第 4 节第 7 项要求确认未嵌入第三方字体／图标／底图后才可转 `APPROVED`；**本任务未做该确认，也未把任何一项标为已授权。**

## 7. 需要人工决定的事项

| # | 事项 | 涉及镜头 | 标记 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | 镜头 01／02 在段 1 中的切分点 | 01、02 | `PENDING_REVIEW` | 表格未给出英文切分文本；第 4.1 节给出按句边界的定位结果供决定 |
| 2 | 镜头 07 与 06 的时间重叠 | 06、07 | `PENDING_REVIEW` | 镜头 07 引用的 `group those loans together` 是镜头 06 句内的子片段，两者时间范围重叠，无法各自独立 |
| 3 | 镜头 09 与 08 的时间重叠 | 08、09 | `PENDING_REVIEW` | 同上：`packaged into financial securities that investors can buy` 是镜头 08 句内的子片段 |
| 4 | 段 4 的镜头数 | 05–10 | `PENDING_REVIEW` | 段 4 一句话被拆给 6 个镜头，其中 3 个为子片段引用；是否需要重整为更少的镜头属创作决定 |
| 5 | 第 2–8 章分镜 | — | 未建立 | 需独立任务；可引用 05 号文件第 0.1 节已确认的 V2 口径 |
| 6 | 镜头 03 地图、07–09 动画的实际文件路径 | 03、07、08、09 | `SOURCE PENDING` | 用户称已完成，但项目目录内不存在，需提供路径或重做 |
| 7 | 静态帧→动画 | 04、05、06、10、11、12 | 待补 | 当前无 ffmpeg，无法编码视频；须在具备工具的环境完成 |
| 8 | 镜头 01、02 实拍素材授权 | 01、02 | `SOURCE PENDING` | 素材尚未寻找 |
| 9 | 镜头 04–13 是否嵌入第三方字体／图标／底图 | 04–13 | `PENDING_REVIEW` | 确认后方可由「初步判定」转 `APPROVED` |

## 8. 未改动声明与验证

本任务只**新增**了两个输出：

1. `BehindTheBreakdown/outputs/voice_auditions/task17_ch1_segments/`（6 个 WAV + `SEGMENT_REPORT.md`）
2. `BehindTheBreakdown/docs/15_TASK17_STORYBOARD_ALIGNMENT_REVIEW.md`（本文件）

| 检查项 | 结果 |
| --- | --- |
| V2 旁白稿 sha256 未变 | ✅ `c3a5b9da2788a2a54eafd2b9330e961cc5600dab4f5cb1aa838f12db175dafd2`（前缀 `C3A5B9DA2788A2A5` 实测匹配：是） |
| V1 旁白稿未改 | ✅ `40d1e0edb48120140fbb23de2149797bbd09d862b4cc8112ed3b4f5445f2fe17` |
| 分镜表未被覆盖 | ✅ `6f21d524c38f963d7fe33d48d94eeb0febc60f0940bf748a015897f98efad2ef`（本轮只读） |
| 第一章源音频未变 | ✅ `ea9b566bde289de437e3a5e867731f6f72a80441e7d7b3ad6016426b9f0d8e1f` |
| 词级时间戳未变 | ✅ `b0112bb5d5ce907b2c56bbfa334150fa30db5107f8b22e0adc99a1efc2c5e4c7` |
| 是否调用 TTS 重新生成语音 | ❌ **未调用**（切分脚本不 import 任何合成函数） |
| 是否制作 BGM 或混音 | ❌ 未制作 |

---

**报告结束。**

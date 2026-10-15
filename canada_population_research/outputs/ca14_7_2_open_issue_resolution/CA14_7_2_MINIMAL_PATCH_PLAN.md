# CA-14.7.2｜V7 最小补丁计划

**对象**：[CA14_7_1_NARRATION_V7_CANDIDATE.md](../ca14_7_1_v7_candidate/CA14_7_1_NARRATION_V7_CANDIDATE.md)（实测 1,198 词）
**性质**：**只列建议，不直接修改 V7 原文件。** V7 仍为未冻结候选稿。
**依据**：[CA14_7_2_OPEN_ISSUE_DECISIONS.md](CA14_7_2_OPEN_ISSUE_DECISIONS.md)
**词数与时长**：全部经程序逐词复核（口径同 CA-14.7.1：word = 含字母或数字的空白分隔 token；同一函数复算 V7 得 **1,198**，与既有记录一致）。

> **本计划只含 3 处补丁**，对应 U2 / U3 / U4 三项裁定。
> **不新增任何未核验数字**；P3 新增的两个人口数均经本次复算（见 §四）。

---

## 一、补丁总表

| # | 来源 | 位置 | 类型 | 原词数 | 新词数 | 净变化 |
|---:|---|---|---|---:|---:|---:|
| **P1** | U2 | 镜头 1.1 | 删词 | 20 | 18 | **−2** |
| **P2** | U4 | 镜头 2.2 | 加限定语 | 64 | 67 | **+3** |
| **P3** | U3 | 镜头 3.3 前 2 句 | 改写（去掉 109） | 119 | 122 | **+3** |
| | | | | | **合计** | **+4** |

**补丁后全稿 = 1,198 ＋ 4 = 1,202 词**

---

## 二、P1｜U2：删去 `of land`

### 原文（镜头 1.1，20 词）

> This is Canada. Ten million square kilometres of land, and from up here, almost none of it looks lived in.

### 替换（18 词）

> This is Canada. Ten million square kilometres, and from up here, almost none of it looks lived in.

**改动**：只删 ` of land` 两个词。**句子其余部分一字不动。**

### 理由

1. `Ten million` 是加拿大**总面积 9,984,670 km²** 的合理取整（有效数字 1 位，误差 **0.15%**）。
   官方出处：[StatCan《International perspective》](https://www.statcan.gc.ca/pub/11-402-x/2012000/chap/geo/geo01-eng.htm) ——
   「total area of **9,984,670 km²**, including **891,163 km² of freshwater**」。
2. **但 `of land` 把口径指向陆地面积**，而官方 2021 Census 陆地面积是 **8,788,702.80 km²**
   （`data/raw/98100011.csv` 列 [14]；交叉验证：36,991,981 ÷ 8,788,702.80 = **4.2090 → 官方密度 4.2** ✅）。
   两者相差 **13.8%**。**保留 `of land` 等于说一个可被直接证伪的句子。**
3. 删 `of land` 后句子为真，**且修辞力度不变**——「一千万平方公里」作为国土尺度的口语表达成立。
4. 这是**最小修改**：不动数字、不动语序、不动节奏。

### 备选（若人工不让渡「一千万」的修辞）

> Almost nine million square kilometres of land, and from up here, almost none of it looks lived in.

22 词（**+2**）。数字与限定词都对准官方陆地面积。**代价**：把「一千万」降为「将近九百万」，
削弱第 1 章的尺度感——而这一镜的全部说服力就建立在「大」上。**故列为备选，不推荐。**

### 受影响的镜头与画面

| 项 | 影响 |
|---|---|
| 镜头 **1.1** | 20 → 18 词；@135 wpm 由 **8.9 s → 8.0 s（−0.9 s）**。拍表为 9.0 s，**仍可容纳** |
| **1.1 画面** | **零改动。** 分镜 L93 已明确「本稿默认画面上**不出现**该数字，只做视觉对比」；L314 待裁定项 2 默认选 **A（不上屏）** |
| 1.1 拍 c 文字卡 | `1,026 population centres` **不受影响** |

> ⚠️ **一处须更正的项目记录**：分镜 L314 记「项目数据中**没有**加拿大陆地面积字段」。
> **本次核验表明该记录不准确**——官方表 98-10-0011 列 [14] **就是**官方陆地面积字段，且它就在项目目录内。
> 建议后续维护时更正（属分镜侧文档，本任务不修改）。

---

## 三、P2｜U4：`Same area` → `Same area on the grid`

### 原文（镜头 2.2，64 词）

> And the two squares are not even copies of each other. The Toronto square contains eighty-nine population centres and eight and a half million people. The Montreal one contains ninety-six centres and four and a half million. **Same area**, but inside the Toronto square a centre averages about ninety-five thousand people, and inside the Montreal square about forty-eight thousand. More centres, half the people.

### 替换（67 词）

> And the two squares are not even copies of each other. The Toronto square contains eighty-nine population centres and eight and a half million people. The Montreal one contains ninety-six centres and four and a half million. **Same area on the grid**, but inside the Toronto square a centre averages about ninety-five thousand people, and inside the Montreal square about forty-eight thousand. More centres, half the people.

**改动**：`Same area`（2 词）→ `Same area on the grid`（5 词），**净 +3 词**。**句子其余部分一字不动。**

### 理由

1. **`Same area` 在网格口径下按构造成立**：两单元都是 **200 × 200 km**
   （`_ca04a_stats.json` L1445 定义 `x = R·cos45·lon, y = R·lat` 的 200 km 网格），各 40,000 km²。
2. **但在地面口径下不成立。** 本次几何复算：

   | 项 | Toronto 单元（lon −79.5 / lat 44.1） | Montréal 单元（lon −74.4 / lat 45.9） |
   |---|---|---|
   | 平面尺寸 | 200.00 × 200.00 km | 200.00 × 200.00 km |
   | 反解经纬跨度 | lon 2.5437° / lat 1.7986° | lon 2.5437° / lat 1.7986° |
   | 该纬度 1° 经度长度 | 79.8521 km | 77.3821 km |
   | **球面实际尺寸** | **203.12 × 200.00 km** | **196.83 × 200.00 km** |
   | **球面实际面积** | **40,623 km²** | **39,367 km²** |

   两者相差 **1,257 km²（−3.09%）**；合计 **79,990 km²**（与既有记录吻合 ✅）。
   成因：网格是**平面近似**（经度按固定 cos45° 折算），而 Toronto 在 44.1°N、Montréal 在 45.9°N。
3. **旁白紧接着就在这两块地里比较「每中心平均人口」**，观众有理由把 `Same area` 当成地面面积的陈述。
   加上 `on the grid` 后**口径被说清楚**，近似关系明确。
4. 任务指示「使用明确表达近似关系的措辞，不必追求数学上的绝对相等」——**本补丁正是落实该指示**。

### 备选

| 方案 | 表述 | 净词数 | 评价 |
|---|---|---:|---|
| **A（推荐）** | `Same area on the grid` | **+3** | 口径明确、语域自然、改动最小 |
| B | `Same footprint` | −1 | 同样明确且更短；`footprint` 在纪录片旁白中略偏技术 |
| C | `Each about forty thousand square kilometres` | +6 | 数学最严谨，但与本段已说的 `about eighty thousand` 重复 |
| D | 照旧 `Same area` | 0 | 无独立错误（平面口径下成立），但保留 3.1% 的误读空间 |

### 受影响的镜头与画面

| 项 | 影响 |
|---|---|
| 镜头 **2.2** | 64 → 67 词；@135 wpm **28.4 → 29.8 s（+1.3 s）** |
| **2.2 画面** | ⚠️ 建议增加一行口径行（L7 20 px，`MUTED`）：`Same area as measured on the 200 km grid.`——与旁白同期说明口径 |
| **2.1 画面** | 无需因本补丁调整。**但方块定位问题仍未决**（分镜 L97–L106 记录 **2,520 种参数组合全部失败**，属独立待裁定项）。**U4 的修改不依赖它，也不能解决它** |

---

## 四、P3｜U3：去掉 3.3 的 `109` 计数

### 原文（镜头 3.3 前两句，逐字取自 V7 候选稿 L100）

> Slice the corridor into bands half a degree of longitude wide, and the sizes change sharply. **West of Toronto, four of those bands together hold a hundred and nine population centres; Toronto's own band holds thirty-one. Those four are all the corridor contains west of Toronto.**

### 替换（把上面加粗部分整体替换）

> Slice the corridor into bands half a degree of longitude wide, and the sizes change sharply. **Four of those bands lie west of Toronto. Toronto's own band holds thirty-one population centres, and about six point two million people. Those four bands hold about three point two million between them.**

**改动**：共 2 处字面替换——
1. `West of Toronto, four of those bands together hold a hundred and nine population centres; Toronto's own band holds thirty-one.`
   → `Four of those bands lie west of Toronto. Toronto's own band holds thirty-one population centres, and about six point two million people.`
2. ` Those four are all the corridor contains west of Toronto.` → ` Those four bands hold about three point two million between them.`

**句子其余部分一字不动。**

### 理由

**① 109 不可复现（详见裁定报告 §U3）**

- CSV 记录 109 与 2,916,977 在 **CSV 内部自洽**：15+30+30+34 = 109；465,054+319,771+829,108+1,303,044 = 2,916,977。
- 但本次**穷举 7 种经纬定义**（含 CSV 自己记的走廊 BOUNDS −81.6\~−70.4 / 42.30\~47.05），
  **23 个箱中无任何一箱的中心数与 CSV 相同**；四带一律为 **118 或 120**。
- 本次**受约束扫描 104 组经纬矩形**（满足「23 箱人口 = 17,859,490」），
  其中**同时**满足「四带 = 109 且 2,916,977」「−79.5 = 31 且 6,223,244」的候选 = **0 组**。
- 结论：**不存在任何已定义的经纬口径能给出 109。** 又：CSV 的 2,916,977 与它自己引用的那四个箱
  （−81.5/−81.0/−80.5/−80.0，人口合计 3,263,797）**不是同一组数据**。

**② 替换句中的三个数字全部可复现**

| 数字 | 本次复算 | CSV 记录 | 差 |
|---|---:|---:|---:|
| Toronto 带中心数 **31** | **31** ✅ | 31 | **0** |
| Toronto 带人口 **约 620 万** | **6,234,086** | 6,223,244 | 10,842（**0.17%**） |
| 四带人口 **约 320 万** | **3,194,401** | 2,916,977 | 277,424（**9.5%**） |

**③ 为什么用人口数替换中心计数，而不是把 109 改成 118**

- 118 是**我的**复算值；CSV 用的是另一套不可复现的口径。把 118 写进旁白 = **用一个新数字替换旧数字**，
  而画面若仍按 CSV 画，音画依然不一致。
- 改用**人口**后，旁白的口径与画面（柱高按人口，见分镜 L417）**一致**，
  且 6.2M / 3.2M 两个量级在两个口径下都落在同一个舍入值上（CSV 口径下四带为 2.92M，仍可说 about three million）。
- **核心论证不受影响**：6,234,086 > 3,194,401，**1.95 倍**；「Toronto 一个带的人口多于西侧四带合计」**不依赖 109**。

**④ 关于「more than twice」这句**

原文 `Yet Toronto's band has more than twice the people.` **本次未改动**。
依据 CSV 口径：6,223,244 ÷ 2,916,977 = **2.13 倍 ✅**（该句在原稿中即以此为依据）。
**须提醒**：若改用本次复算的四带人口 3,194,401，则倍数为 **1.95**，该句将不成立。
**→ 若人工采纳 P3 并同时改动画面人口标签，必须一并复核这一句。** 本补丁默认画面沿用 CSV 口径。

### 受影响的镜头与画面

| 项 | 影响 |
|---|---|
| 镜头 **3.3** | 119 → 122 词；@135 wpm **52.9 → 54.2 s（+1.3 s）**。分镜 3.3 的拍表（L406 拍 b 为 6.0–13.0 s 等）需相应微调 |
| **3.3 拍 b（L406）的 `109 centres` 标签** | ⚠️ **必须撤下。** 建议改为不带计数的 `four western bands`，或直接删除该标签 |
| **3.3 拍 b 的框选（L406）** | ⚠️ **框选与计数必须择一**：若保留「圈住 lon −81.5/−81.0/−80.5/−80.0 四根相邻半度柱」的框选，其中心数按走廊 BOUNDS 复算为 **118**，**不是 109**。二者不可兼得 |
| **3.3 拍 b 的人口标签（L406）** | 现有 `2.9 million` 与 `6.2 million`。旁白新句说 `about three point two million`。⚠️ **必须二选一**：要么画面改标 `3.2 million`，要么旁白改说 `about three million`。**不得一个说 2.9 一个说 3.2** |
| **3.3 拍 d（L408）** | `5.5 million of 6.25 million is one centre.` **保留不动**——5.5M / 6.25M / 90.8% 三项均已核验 |
| **柱高口径（L417）** | **保留不动**——柱高按人口，与旁白一致 |
| **3.3 的中位数待裁定项（L427–L447）** | **本次不涉及。** L443 记「n=31 中位 6,507｜n=109 中位 4,227」，L447 记「109 会变成 98 或 116」。这两个中位数**至今未复现**；但 V7 的 3.3 **没有使用任何中位数数字**（CA-14.7.1 已确认），故**不构成阻断** |

> ⚠️ **一处性质变化须记录**：CA-14.7.1 把 V7 对 3.3 的处理记为「**插入**一句、未触碰原句」。
> 若 P3 获采纳，V7 的 3.3 将从「插入」变为「**改写前两句**」。**这是 U3 裁定带来的性质变化，须在冻结前在案。**

---

## 五、补丁后的词数与时长

### 逐章

| 章 | 补丁前 | P1 | P2 | P3 | **补丁后** |
|---|---:|---:|---:|---:|---:|
| 1 | 141 | −2 | | | **139** |
| 2 | 217 | | +3 | | **220** |
| 3 | 423 | | | +3 | **426** |
| 4 | 222 | | | | **222** |
| 5 | 195 | | | | **195** |
| **合计** | **1,198** | **−2** | **+3** | **+3** | **1,202** |

### 成片时长（N = 18.0 s，U1 裁定口径；**估算值，非实测配音**）

| 语速 | 纯旁白 A | 成片 = A ＋ 18 | 对 540 s 底线 | 对 555 s 目标 |
|---|---:|---:|---:|---:|
| 125 wpm | 577.0 s | **595.0 s = 9:55.0** | +55.0 | +40.0 |
| 130 wpm | 554.8 s | **572.8 s = 9:32.8** | +32.8 | +17.8 |
| **135 wpm** | 534.2 s | **552.2 s = 9:12.2** | **+12.2 ✅** | −2.8 |

> **补丁后三档语速全部守住 9 分钟底线**，最小余量 **+12.2 s**（135 wpm），
> 距 9:15 目标仅 **−2.8 s**。**无需再增减词数。**

### 逐镜变化

| 镜头 | 补丁前 | 补丁后 | 变化 | @135 wpm |
|---|---:|---:|---:|---:|
| 1.1 | 20 | 18 | −2 | 8.9 → **8.0 s** |
| 2.2 | 64 | 67 | +3 | 28.4 → **29.8 s** |
| 3.3 | 119 | 122 | +3 | 52.9 → **54.2 s** |
| 其余 18 镜 | — | — | 0 | 不变 |
| **合计** | **1,198** | **1,202** | **+4** | 532.4 → **534.2 s** |

---

## 六、本计划不做的事

| 不做 | 原因 |
|---|---|
| **不修改 V7 原文件** | 任务要求；V7 保持未冻结候选状态 |
| 不修改 V6、冻结报告、原始数据、任何既有分镜 | 只读边界 |
| **不在 P3 中新增未核验数字** | 6.2M / 3.2M / 31 三项均由本次复算支撑（§四 ②） |
| **不把 109 改成 118** | 118 是复算值，CSV 用另一套口径；换成 118 只是「换一个数字」，音画仍可能不一致（§四 ③） |
| 不改第 2 章方块定义或边界 | U4 只改措辞；方块定位（分镜 §六 项 1，2,520 组参数全败）是独立未决项 |
| 不处理 3.3 的 6,507 / 4,227 中位数 | V7 未使用该两值；且至今未复现 |
| 不生成音频、图片或视频 | 未授权 |
| 不冻结 V7 | 待人工裁定 |

---

## 七、供人工裁定的三项

| # | 须裁定 | 选项 |
|---:|---|---|
| 1 | **P1** 删 `of land`（推荐）还是改为 `Almost nine million square kilometres of land` | 见 §二 |
| 2 | **P2** 用 `Same area on the grid`（推荐）还是 `Same footprint` / `Each about forty thousand square kilometres` / 照旧 | 见 §三 |
| 3 | **P3** 采纳替换（推荐）还是把 109 换成 118 / 其他 | 见 §四 |

**三项均为独立选择，可分别采纳或拒绝。全部采纳后全稿 1,202 词、成片 @135 wpm = 552.2 s。**

---

## 八、相关文件

- 裁定报告：[CA14_7_2_OPEN_ISSUE_DECISIONS.md](CA14_7_2_OPEN_ISSUE_DECISIONS.md)
- V7 候选稿：[CA14_7_1_NARRATION_V7_CANDIDATE.md](../ca14_7_1_v7_candidate/CA14_7_1_NARRATION_V7_CANDIDATE.md)
- V7 审查报告：[CA14_7_1_V7_AUDIT_REPORT.md](../ca14_7_1_v7_candidate/CA14_7_1_V7_AUDIT_REPORT.md)
- 变更记录：[CA14_7_1_V6_TO_V7_CHANGELOG.md](../ca14_7_1_v7_candidate/CA14_7_1_V6_TO_V7_CHANGELOG.md)
- 官方来源：[Statistics Canada 98-10-0011-01](../../data/raw/98100011.csv)（Land area 8,788,702.80 km²）、[International perspective](https://www.statcan.gc.ca/pub/11-402-x/2012000/chap/geo/geo01-eng.htm)（Total area 9,984,670 km²，含淡水 891,163 km²）

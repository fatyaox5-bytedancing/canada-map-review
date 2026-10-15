# CA-14.4.2 旁白 V2 候选稿定稿审查报告

**性质**：只处理旁白的事实表达修订，生成 V3 候选稿。
**未生成**分镜、图片、地图、音频或视频；**未覆盖** `CA14_4_NARRATION_V1.md`、`CA14_4_1_NARRATION_V2_CANDIDATE.md`、`CA14_4_1_REVISION_REPORT.md` 或任何其他历史版本。

**输入**：`CA14_4_1_NARRATION_V2_CANDIDATE.md`、`CA14_4_1_REVISION_REPORT.md`、`CA14_3_FACT_DECISIONS.md`，以及 CA-04A 的机器可读产物（`_ca04a_centres.csv`、`_ca04a_stats.json`、`CA04A_SPATIAL_STATISTICS.csv`）。

---

## 一、总览

| 项 | V2 状态 | V3 处理 | 词数变化 |
|---|---|---|---:|
| 1 第 3 章经度带比较 | 直接比人口总量（0.5° vs 四个带） | 改为**平均中心规模**，并补**中位数限定** | 第 3 章 +56 |
| 2 第 2 章省级百分比 | 未说明分母；结尾称「都在东部」 | **明确分母为 1,026 中心合计人口**；删去绝对表述 | 第 2 章 −2 |
| 3 开场统计实体 | 「biggest built-up areas」；未说明中位数性质 | 改为**人口聚集地**表述；明确 **15 组两两距离的中位数** | 第 1 章 +15 |
| 4 其他已确认内容 | — | 全部保持不变；第 4 章补一句**两口径不相等**的显式说明 | 第 4 章 +15 |
| 5 第 5 章 | — | **完全未改动** | ±0 |

**全片词数**：V2 **760** → V3 **841**（**+81**）。

| 章 | V2 词数 | V3 词数 | 135 wpm | 140 wpm | 150 wpm |
|---:|---:|---:|---:|---:|---:|
| 1 | 97 | **112** | 50 s | 48 s | 45 s |
| 2 | 157 | **152** | 68 s | 65 s | 61 s |
| 3 | 205 | **261** | 116 s | 112 s | 104 s |
| 4 | 152 | **167** | 74 s | 72 s | 67 s |
| 5 | 149 | **149** | 66 s | 64 s | 60 s |
| **合计** | **760** | **841** | **374 s** | **360 s** | **336 s** |

### ⚠️ 关于时长的诚实说明

**本稿为满足定稿要求而增加了 81 词，全片估算从 337 秒升到 374 秒（135 wpm）。**

任务要求「不为了达到 379 秒而填充旁白」。**本稿增加的字数没有一个是填充语**，全部来自任务明确要求的澄清：

- 第 3 章：+56 词（平均规模表述 + 中位数限定）
- 第 1 章：+15 词（统计实体表述 + 15 组距离说明）

**但必须说明**：增加后 135 wpm 估算为 **374 秒**，距 379 秒只剩 **5 秒余量**。

**这个余量小于估算本身的不确定度。** 按 ±10% 的估算精度，135 wpm 档的真实时长可能落在 **336–411 秒**之间，**上限已经超过 379 秒**。也就是说：

- 若实际语速接近或快于 140 wpm，`374 秒`这件事本身没有意义，因为真实值可能明显更短；
- 若实际语速慢于 135 wpm，**全片可能超过 379 秒**。

**结论：本稿不能自称「满足 379 秒」。** 它只是「按 135 wpm 的算术结果低于 379 秒」。**是否需要为时长删减内容，应由人工在试读后决定**——本稿不自行删减，因为可删的部分都属于任务明确要求的澄清。见 §六 待裁定项。

---

## 二、第 1 项｜第 3 章经度带比较

### 2.1 平均规模复核

用 `_ca04a_centres.csv` 只读复算，结果与任务给定值**完全一致**：

| 组 | 中心数 | 人口 | 平均中心规模 |
|---|---:|---:|---:|
| Toronto 经度带（lon −79.5） | 31 | 6,223,244 | **200,750 人/中心** |
| 以西四个经度带（−81.5 / −81.0 / −80.5 / −80.0） | 109 | 2,916,977 | **26,761 人/中心** |
| **比值** | — | — | **7.5015 倍** |

复核结论：**200,750 ✅ ｜ 26,761 ✅ ｜ 7.5015 倍 ✅**

### 2.2 ⚠️ 复核中发现的一个必须披露的问题

平均规模相差 7.5 倍，但**中位中心规模只相差 1.54 倍**：

| 指标 | Toronto 带 | 以西四带 | 比值 |
|---|---:|---:|---:|
| 平均中心规模 | 200,750 | 26,761 | **7.50** |
| **中位中心规模** | **6,507** | **4,227** | **1.54** |
| 最大中心 | 5,647,656 | 729,560 | 7.7 |

**原因**：Toronto 带里有一个 5,647,656 人的中心（Toronto 本身），而西侧四带最大的中心只有 729,560 人。**均值差几乎全部由这一个中心承担。**

**因此「平均规模大 7.5 倍」这句话本身准确，但如果只念这一句，观众会误以为 Toronto 带里每一个中心都更大。** V3 因此在同段补了一句限定：

> That gap comes from a few very large centres, not from every centre being bigger. The median centre in Toronto's band is small too.

> 中文对照：这个差距来自少数几个极大的中心，**并不是每一个中心都更大**——多伦多那个带里的中位中心同样很小。

**这一句是本稿主动增加的，任务并未要求。** 理由：本项目的纪律是「不得把相关性写成因果」「不得夸大」，而省掉这一句会让一个准确的数字产生不准确的印象。**是否保留由制作方决定**（见 §六）。

### 2.3 修改前后的英文文本

**V2（被替换）**

> Slice the corridor into bands half a degree of longitude wide, and the pattern reverses. West of Toronto, four of those bands together hold a hundred and nine population centres. Toronto's own band holds thirty-one. Yet Toronto's band has more than twice the people.

**问题**：一个 0.5° 宽的带与四个 2.0° 宽的带**直接比人口总量**，两组空间跨度相差 4 倍，**不可比**（CA-14.4.1 §2.2 已记录）。

**V3（采用）**

> Slice the corridor into bands half a degree of longitude wide, and the sizes change sharply. West of Toronto, four of those bands together hold a hundred and nine population centres. Toronto's own band holds thirty-one. Yet Toronto's band has more than twice the people. Its centres average about two hundred thousand people each; in the four bands to the west, about twenty-seven thousand. That gap comes from a few very large centres, not from every centre being bigger. The median centre in Toronto's band is small too.

### 2.4 纪律确认

- ✅ **未推广为整个东西部的比较**：全段只说「West of Toronto」与「the four bands to the west」，未出现 east/west Canada、Ontario east vs west 等提法。
- ✅ **未添加成因推测**：全段为纯空间统计陈述。
- ✅ **未新增指标**：「中心数」「人口」「平均规模」均直接来自 `_ca04a_stats.json` 的 `corridor_lon_bins`；平均规模是「该带人口 ÷ 该带中心数」的一步除法。

---

## 三、第 2 项｜第 2 章省级百分比的分母

### 3.1 修改前后

**V2（被替换）**

> The provinces tell the same story. Ontario holds forty-one percent of the total, Quebec twenty-three, British Columbia fourteen. That is seventy-eight percent in three provinces. Of the thirteen provinces and territories, ten hold less than four percent each.

**问题**：`of the total` 指代不明。上一段刚讲过两个网格方块，观众很容易把「total」理解为**加拿大全国人口**。而实际分母是 **1,026 个人口中心的合计人口 30,389,999**。

**V3（采用）**

> The provinces say the same thing. Ontario holds forty-one percent of that total, Quebec twenty-three, British Columbia fourteen. Those shares are of the combined population of the one thousand and twenty-six population centres, not of Canada. Together, the three provinces hold seventy-eight percent.

改动要点：

1. **分母写明**：`the combined population of the one thousand and twenty-six population centres, not of Canada`。
2. **删去「十个省和地区各自不到 4%」**：该句在 V2 中与主论点重复，删去不影响论证（数值见下表）。
3. 中文对照同步写明「分母是 1,026 个人口中心的合计人口，**不是加拿大全国人口**」。

### 3.2 分母核验

| 省 | 值 | 验证 |
|---|---:|---|
| Ontario | 40.59% | 12,335,284 ÷ 30,389,999 |
| Quebec | 22.66% | 6,886,955 ÷ 30,389,999 |
| British Columbia | 14.37% | 4,365,903 ÷ 30,389,999 |
| 三省合计 | 77.62% → 旁白念 78% | 四舍五入 |

口径：`CA04A_SPATIAL_STATISTICS.csv` 第 73–85 行「省级人口（不重复口径）」，4 个跨省中心按官方省级部分拆分，合计回到 30,389,999。

### 3.3 「都在东部」的审查结论：**不成立，已删除**

**V2 结尾原句**：

> So the population is not spread across the country. It is stacked, very high, in a very small number of places. And those places are in the east.

**核验结果：`And those places are in the east` 不成立。**

按人口排序的前六个中心里，**有三个在西侧**：

- Toronto：5,647,656 人（lon -79.50，东）
- Montréal：3,675,219 人（lon -73.67，东）
- Vancouver：2,426,160 人（lon -122.90，西）
- Calgary：1,305,550 人（lon -114.07，西）
- Edmonton：1,151,635 人（lon -113.50，西）
- Ottawa - Gatineau：1,068,821 人（lon -75.68，东）

此外，以 lon −100° 为界，**以西仍有 29.09%** 的人口中心人口（8,839,707 人）。

**V3 处理：彻底删除该句**，第 2 章结尾停在`It is stacked, very high, in a very small number of places.`

**并在第 3 章开头以事实形式补上限定**（不用「都在东部」这种绝对表述）：

> Most of those places draw one corridor... But three of the six largest sit far to the west.

**为什么放在第 3 章而不是第 2 章**：第 3 章正是在讲走廊的范围，在那里说明「并非全部」最自然，也避免第 2 章结尾出现一个需要立刻撤回的断言。

⚠️ **「Most of those places」的依据**：走廊范围内（CA-04A BOUNDS 口径，424 个中心）占 58.77%；安大略+魁北克占 63.25%。用 `Most` 而不是 `All` 有数据支持。**但「most」是对 1,026 中心人口的多数而言，不是对土地面积的多数。**

---

## 四、第 3 项｜开场的统计实体表达

### 4.1 修改前后

**V2（被替换）**

> Now watch the six largest population centres in the country light up. These are the biggest built-up areas in Canada, as Statistics Canada counts them. Between any two of them, the median distance is about two thousand seven hundred kilometres.

**两个问题**：

1. **`the biggest built-up areas` 不是 Statistics Canada 的定义。** 本项目**从未取得 population centre 的官方定义文本**（CA-14.3 §四 已记录 `PCCLASS` 官方含义未确认）。把「built-up area」挂在「as Statistics Canada counts them」后面，等于替统计局说了一句本稿无法核验的话。
2. **中位数的性质未说明。** 六个对象两两比对共**15 组**距离；「median distance」容易被理解为平均距离或最近邻距离。

**V3（采用）**

> Now watch the six largest population centres in the country light up. A population centre is where people are concentrated — as Statistics Canada counts them. Between any two of these six there are fifteen distances, and the median of those fifteen is about two thousand seven hundred kilometres. Not the closest pair. The middle one.

改动要点：

1. **改用可辩护的表述**：`A population centre is where people are concentrated`。**只说「人口聚集」，不宣称这是统计局的完整定义**，从而与「本项目未取得官方定义」这一事实相容。
2. **明确 15 组**：`Between any two of these six there are fifteen distances`。6 个对象的两两组合数 = C(6,2) = **15** ✅。
3. **明确是中位数**：`the median of those fifteen`，并加`Not the closest pair. The middle one.` **同时排除了「平均距离」与「最近邻距离」两种误读。**

### 4.2 统计事实核验

| 事实 | 值 | 核验 |
|---|---:|---|
| 六个人口中心 | 6 个（PCTYPE=1 且人口 ≥ 100 万） | `_ca04a_centres.csv` |
| 两两组合数 | **15** | C(6,2) = 15 ✅ |
| 两两距离中位数 | **2,698.07 km** → 旁白念 2,700 | `CA04A_SPATIAL_STATISTICS.csv` 第 124 行 |
| 最小值 | 157.4 km（Montréal ↔ Ottawa-Gatineau） | 同上 |
| 最大值 | 3,663.4 km | 同上 |

**2,700 km 的性质**：是 **15 组两两距离的中位数**。**不是平均值**（平均值不同），**不是最近邻距离**（最近邻是另一个指标）。V3 的英文旁白已逐字排除这两种误读。

### 4.3 保留未变的开场元素

- ✅ 六个中心（未改成五个或七个）
- ✅ 15 组两两距离（新增说明，未改数值）
- ✅ 中位数约 2,698.1 km（旁白取整 2,700）
- ✅ 未使用 18.12 km 最近邻反差开场（决策 2）
- ✅ 未点名最大距离那一对（项目数据未列该城市对）

---

## 五、第 4 项｜其他已确认内容的保持情况

| 已确认内容 | V3 状态 | 核验方式 |
|---|---|---|
| 414 个走廊人口中心 | ✅ 旁白念 `four hundred and fourteen` | 程序化检索在位 |
| 旁白取整说 59% | ✅ `fifty-nine percent` | 程序化检索在位 |
| 画面精确值用 58.7% | ✅ 旁白**未念**精确值，不冲突 | 旁白 0 处出现 58.6/58.7 |
| 不把 414 与 424 写成已确认关系 | ✅ 旁白 **0 处**出现 424；未出现「子集」「包含」等表述 | 程序化检索 |
| 两个 200 km × 200 km 网格共 80,000 km² | ✅ `about eighty thousand square kilometres` | 在位 |
| 覆盖人口中心合计人口的 43% | ✅ `forty-three percent of everyone in a Canadian population centre` | 在位，分母写明 |
| 三地区与 60°N 是两个口径，不混为一谈 | ✅ 两者**并列说出**，并以「12 个 / 69,029」与「14 个 / 71,592」分别呈现 | 见 §5.1 |
| 走廊主证据 51.8 km / 21.1% | ✅ `just over twenty-one percent`；最大空缺 `fifty-two kilometres` | 在位 |
| 段长 232 km | ✅ `two hundred and thirty-two kilometres` | 在位 |
| 不恢复「爱尔兰岛面积」类比 | ✅ **0 处**出现 Ireland | 程序化检索 |
| 不为 379 秒填充旁白 | ⚠️ **见 §一 说明**：+81 词全部来自要求的澄清，但余量只剩 11 秒 | — |

### 5.1 北部两个口径的并列处理

V3 把两个口径**并列陈述**，不复用同一个句子框架：

> The three northern territories hold twelve population centres and sixty-nine thousand people. North of the line, there are fourteen, with seventy-one thousand five hundred and ninety-two people. Two-tenths of one percent of everyone living in a population centre in Canada. Two ways of drawing the same line, and they do not give the same count.

| 口径 | 中心数 | 人口 | 占 1026 中心人口 |
|---|---:|---:|---:|
| 三个北方地区（行政区） | 12 | 69,029 | 0.2271% |
| 北纬 60° 以北（纬度线） | 14 | 71,592 | 0.2356% |

**两个数不相等，且旁白明说「不是同一个数」**，避免观众把两者混用。

---

## 六、未解决事项与待裁定项

### 6.1 待人工裁定

| # | 事项 | 本稿处理 | 需要决定什么 |
|---:|---|---|---|
| 1 | 时长余量只剩 11 秒 | 未自行删减 | 是否接受 374 秒（135 wpm），或指定压缩哪一章 |
| 2 | 第 3 章中位数限定句 | 保留（主动增加） | 是否保留这句限定；删去可省约 22 词 / 10 秒 |
| 3 | 「most of those places」的归纳 | 使用 `Most` | 是否接受该归纳（依据：走廊 58.77% / 安略+魁北克 63.25%） |
| 4 | 画面文字用 58.67% 还是 58.7% | 旁白念 59% | 沿用 CA-14.4.1 的待裁定项 |
| 5 | 414 是否为 424 的真子集 | **仍无法证明** | 承接 CA-14.4.1 §7.4，未解决 |
| 6 | population centre 的官方定义文本 | V3 避开定义，只说「人口聚集」 | 若制作方需要正式定义，需另行取得官方来源 |

### 6.2 本次仍未解决的技术限制

1. **所有时长为按词数估算，无任何实测。** 本项目 TTS 路径被沙箱阻断（CA-13.4 已穷尽 6 条路径），**本轮没有任何一段旁白被实际试读或合成过**。估算精度约 ±10%。
2. **英文为书面稿，未经过英语母语者朗读测试。**
3. **`PCCLASS` 官方含义仍未确认**；V3 已避开任何依赖该码值的表述。
4. **经度带比较仍有残留不完美**：Toronto 带纬度跨度 3.40°、以西四带 4.08°，两者纬度带不完全相同；且以西四带被走廊 BOUNDS 西界（lon −81.6）截断，lon −81.75~−81.6 另有 8 个中心（41,188 人）未计入。**因此该比较只能表述为「这两个经度带之间」的差异。** V3 未使用任何「Toronto 以西全部」的措辞。

---

## 七、程序化纪律自检结果

（对 V3 英文正文运行，非人工目视）

| 检查项 | 结果 |
|---|---|
| 把人口中心称为 city / cities | **0** ✅（「Quebec City」2 次为地名，已剔除） |
| metropolitan / metro | **0** ✅ |
| CMA / census metropolitan area | **0** ✅ |
| urban area | **0** ✅ |
| biggest built-up area | **0** ✅（本次删除） |
| scattered / isolated / remote | **0** ✅ |
| 「all in the east」类绝对表述 | **0** ✅（本次删除） |
| 18.12 | **0** ✅ |
| Gini / 0.8843 | **0** ✅ |
| 424 / 226 km / 53.8 / 24.8 | **0** ✅ |
| 17,859,490 | **0** ✅ |
| island of Ireland | **0** ✅ |
| 必需表述（fifteen distances / median / not of Canada / 43% / 59% / 21% / 52 km / 414 / 232 km / 12 个 / 14 个 等 16 项） | **全部在位** ✅ |

> 自检脚本同时验证：`population centre(s)` 出现 10 次；禁用数字与禁用词全部未出现。**综合结果：通过。**

---

## 八、本次执行的只读计算

1. 用 `_ca04a_centres.csv` 复算 Toronto 带与以西四带的中心数、人口、**平均值与中位值** → 平均 200,750 / 26,761（7.5015 倍）；中位 6,507 / 4,227（1.54 倍）；最大 5,647,656 / 729,560。
2. 按 lon −100 / −95 / −90 / −85 四个分界分别计算东西人口占比 → lon −100 为界时以西占 29.09%，**据此判定「都在东部」不成立**。
3. 列出前 12 个人口中心的名称、人口与经纬度 → **确认 Vancouver / Calgary / Edmonton 三个大中心均在西部**。
4. 用 `CA04A_SPATIAL_STATISTICS.csv` 省级行复核 Ontario 40.59% / Quebec 22.66% / BC 14.37% / 三省 77.62%。

**未执行**：未重跑空间分析；未做多边形裁剪；未改任何已有文件；未生成分镜、图片、地图、音频或视频；未联网。


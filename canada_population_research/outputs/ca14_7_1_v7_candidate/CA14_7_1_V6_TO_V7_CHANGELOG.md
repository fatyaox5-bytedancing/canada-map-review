# CA-14.7.1｜V6 → V7 变更记录

**用途**：记录 V7 候选稿相对 V6 冻结稿的**每一处**变更，并把每处变更对回 CA-14.6.1 的 T1 / T2 / T3 编号，逐项给出**采纳／拒绝**决定、**插入位置**、**实测新增词数**、**事实依据**。

**基准**：V6（`outputs/ca14_4_5_narration/CA14_4_5_NARRATION_V6_CANDIDATE.md`，**已冻结，964 词，本次未改动**）。
**结果**：V7 = **1,198 词**，净增 **+234 词**。
**校验**：1,188 是**中间稿**的词数（在补入 3.4 的分母澄清句之前）；本文件凡出现「1,188 词」处均为**过程记录**，**最终值为 1,198 词**。

**词数口径**：与 V6 冻结报告一致——**word = 含字母或数字的空白分隔 token**；破折号等纯符号不计。
本文件所有词数均为**脚本实测**（对 V6 与 V7 两份文件用同一函数复算，V6 复算结果 = 964 词，与冻结记录一致）。

> ⚠️ **时长为词数换算的估算值。本项目 TTS 被沙箱阻断（CA-13.4 已穷尽 6 条路径），无任何旁白被实际朗读或合成过。**

---

## 一、总览

| 项 | 数值 |
|---|---:|
| V6 全稿词数 | 964 |
| **V7 全稿词数** | **1,198** |
| 净增 | **+234** |
| 其中：**新增句**（V6 中不存在的新句子） | **16 句 / +193 词** |
| 其中：**改写句净增**（V6 原有 4 处句子被改写） | **+41 词** |
| **删除** | **0 句** |
| CA-14.6.1 共 17 项建议 | **完全采纳 11 项**（T1 全部 5 项 ＋ T2 全部 6 项）；**部分采纳 1 项**（T3-3）；**拒绝 5 项**（T3-1 / T3-2 / T3-4 / T3-5 / T3-6） |
| CA-14.6.1 推荐组合（9 项）之外的额外采纳 | **T2-3、T2-6、T3-3（部分）**，以及 **2 句本轮新发现的分母澄清**（3.4 与 3.5）；CA-14.6.1 的推荐组合为 T1 全部 ＋ T2-1 / T2-2 / T2-4 / T2-5 |

> **关于「改写句净增」**：4 处改写把 V6 的一个句子拆成两句，**净增 41 词**，且**承载了 T1-2 / T1-4 / T1-5 三项扩充内容**。详见 §三。

---

## 二、逐项决定表（CA-14.6.1 全部 17 项）

### 2.1 T1 必补五项 —— **全部采纳（5/5）**

| # | 建议内容 | 决定 | 插入位置 | 实测新增 | 事实依据 | 理由 |
|---|---|---|---|---|---|---|
| **T1-1** | 给出「人口中心」的人数门槛 | **✅ 采纳** | 第 1 章 **1.2 段首** | **+20 词** | 官方定义：人口 ≥1,000 人 **且** 密度 ≥400 人/km²。<br>本轮独立核验：用官方属性表 `statcan_2021_population_centres_attributes_1030rows.csv` 的 `LANDAREA` 逐条复算 **1,030 条记录，人口 <1,000 者 0 条、密度 <400 者 0 条**。来源：[POPCTR 官方定义](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/az/definition-eng.cfm?ID=geo049a) | 全片最重要的术语。不定义门槛，观众会把人口中心读成「城市」，第 5 章「30,389,999 不是加拿大人口」的全部意义随之失效。**CA-14.6.1 §1.2 曾把该门槛列为「未取得官方原文」的缺口；本轮已取得并核验。** |
| **T1-2** | 说明 41/23/14 是最大的三个，其余十个约 22% | **✅ 采纳** | 第 2 章 **2.3 段中部** | **净 +17 词**（改写句 R1：7 词 → 24 词） | `CA04A_SPATIAL_STATISTICS.csv` L72–84 十三行逐行复算：三省 = 23,588,142 = **77.62%**；其余十者 = 6,801,857 = **22.38% → 约 22%**。十三行合计**精确等于 30,389,999** | 没有这句，「78%」听上去像「大部分省份都很大」；有了这句才看出其余地方几乎不占份量——正是全片论点的省际体现。 |
| **T1-3** | 说明 43/63/59/78 四个百分比共用一个分母 | **✅ 采纳** | 第 5 章 **5.1 段中部** | **+15 词** | 分母 = 30,389,999（1,026 个人口中心合计人口）。四个分子均已逐项核实：42.9976%、63.25%、58.67%、77.62% | 全片防误读的最后一道闸门。若观众带着「43% 是加拿大人口的 43%」离场，全片的统计数据就被整体误读一次。 |
| **T1-4** | 「这张地图没把所有人算进来」——差多少 | **✅ 采纳** | 第 5 章 **5.3 末句**（改写句 R3） | **净 +5 词**（13 词 → 18 词） | 官方表 **98-10-0011-01**（Release 2022-02-09，Universe: All persons, 2021 and 2016 censuses – 100% data，DOI `10.25318/9810001101-eng`）复算：36,991,981 − 30,389,999 = **6,601,982**。官方 Census in Brief 98-200-X2021002 给出 2021 年乡村人口 **6.6 million**，故表述为「**about six and a half million**」。来源：[98-10-0011 表页](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=9810001101)、[Census in Brief 98-200-X2021002](https://www12.statcan.gc.ca/census-recensement/2021/as-sa/98-200-x/2021002/98-200-x2021002-eng.cfm) | CA-14.6.1 把本项列为 **V1 待核验**（原文只有定性的 `millions`）。**该项已由 CA-14.6.2 关闭**：取得官方可引用值。**同时满足 CA-14.6.2 §6.2 三条强制条件：C1 用官方口径「约 660 万」量级、不断言精确值；C2 与 30,389,999 同句同框（英文原句即同句）；C3 不称其为农业人口、不称为统计遗漏。** |
| **T1-5** | 「缺少数据」要说是哪些数据 | **✅ 采纳** | 第 4 章 **4.3 段中部**（改写句 R2） | **净 +19 词**（17 词 → 36 词） | 分镜 §五（`CA14_5_2_CHAPTERS_2_TO_5_STORYBOARD.md` L811）逐项清点确认：本项目**不存在**气候、降水、温度、地形高程、永久冻土、土壤、水系、历史序列、经济产业图层 | 把「缺少数据」具体化，同时**用列举句式封死因果解释**：`Answering that would take data this film does not have: …`，不写成「因为气候……」。 |

### 2.2 T2 建议六项 —— **采纳 3 项 + 1 项部分采纳**

| # | 建议内容 | 决定 | 插入位置 | 实测新增 | 事实依据 | 理由 |
|---|---|---|---|---|---|---|
| **T2-1** | 集中度：中位数 ≈3,000 与均值 ≈29,620 相差 9.9 倍 | **✅ 采纳** | 第 2 章 **2.4 段末** | **+26 词** | **本轮独立复算通过**：对 `_ca04a_centres.csv` 的 1,026 行 `pop2021` 直接计算——中位数 **2,992.5**（= 排序后第 513、514 位 2,989 与 2,996 的均值）、算术平均 **29,619.8821 → 29,619.9**、倍数 **9.8980 → 9.9**。且与官方表 98-10-0011 的 1,026 行**逐值完全一致** | **这是全片最有力的一个数字对**，早已存在于 `CA04A_SPATIAL_STATISTICS.csv` L8/L9，却从未进入旁白。叙述旁白只取「约三千」「近三万」「接近十倍」，**不把均值—中位数差距读成已证明的地理因果**。 |
| **T2-2** | 两个方块面积一样，内部却完全相反 | **✅ 采纳** | 第 2 章 **2.2 段中部** | **+22 词** | 8,493,412 ÷ 89 = **95,431**（复算 95,432，差 1 为四舍五入）；4,573,552 ÷ 96 = **47,641**（复算一致）。旁白取「约九万五千」「约四万八千」，并把「面积相同」处理为**口语近似**（见 §五 待裁定项） | 把 `More centres, half the people.` 这句结论**变成可验证的对照**，而不是断言。 |
| **T2-3** | 西侧四带比较为什么只算四个带 | **✅ 采纳（以改写句实现）** | 第 3 章 **3.3 第二句** | **+10 词** | **本轮独立复现通过**：走廊 BOUNDS（lon −81.6~−70.4、lat 42.30~47.05）外、lon −81.75~−81.6 区间恰有 **8 个中心 / 41,188 人**，且逐个中心名与坐标可列（Wikwemikong、Bayfield、Goderich、Glencoe、Parkhill、Kincardine、Strathroy、West Lorne）。该 8/41,188 另有**五份独立项目报告**记录：CA-14.4.1 L77、CA-14.4.2 L261、CA-14.4.3 L184、CA-14.4.4 L211、CA-14.5（复盘）L117 | CA-14.6.1 因该计数「待核验」而暂缓。**本轮已复现，待核验状态解除。** 但旁白**不给 41,188 这个数字**（词数收益低），只给「这四个带就是走廊在多伦多以西湖全部内容」——把边界性质说清，避免观众以为西边还有更多带被漏掉。**注意：改写的第二句直接紧接原第一句，原文措辞未被改动，因此 V6 的各项几何统计（109 / 31 / 20 万 / 2.7 万 / 625 万 / 550 万）全部继续成立。** |
| **T2-4** | 「0%」是采样结果，不是「没有空地」 | **✅ 采纳（两处）** | 第 3 章 **3.5 段中部**（+21 词）＋ **3.4 段末**（分母澄清 +10 词） | **+31 词** | `CA14_5_2_CHAPTERS_2_TO_5_STORYBOARD.md` 中 3.4/3.5 镜头的采样口径：每隔 5 km 取点、阈值 25 km。**3.4 新增句 `Note the denominator: this percentage counts sample points, not people.` 为本轮分母审计发现缺口后所补**：原文 3.4 的 `Just over twenty-one percent` 有 `of those points`，但未点明该分母**不是人口**，与全片其它人口百分比并列时易被误读。 | 直接封死全片最容易出现的误读：把「0%」读成「这片土地上没有空地」，把「21%」读成人口比例。 |
| **T2-5** | 两套「北方」口径为什么不能相加 | **✅ 采纳** | 第 4 章 **4.1 段末** | **+25 词** | **本轮独立复现通过**：三个地区（Yukon / NWT / Nunavut）= **12 个中心 / 69,029 人**；lat ≥60° = **14 个中心 / 71,592 人**；且**地区中心集合是 60°N 集合的子集**（差集 0 个）。多出的 2 个是 Quebec 的 **Puvirnituq（60.04°N）与 Salluit（62.20°N）** | 若不声明，观众会把 12 与 14 相加得到 26，对「北方只有十几个中心」这个关键印象的误差达 **+86%**。 |
| **T2-6** | 「60°N 对比」只是表意 | **✅ 采纳** | 第 4 章 **4.1 末句** | **+16 词** | 单纯的口径声明，不需要新数据。V6 用 `the sixtieth parallel` 作界线，而行政区界与纬线并不重合（已由上一行复现：12 ⊂ 14，多出的 2 个中心属 Quebec） | 一句话关闭「60°N 是官方分界」的误读。 |

### 2.3 T3 可选六项 —— **部分采纳 1 项，拒绝 5 项**

| # | 建议内容 | 决定 | 理由 |
|---|---|---|---|
| **T3-1** | 六个中心其实排成一条线 | **❌ 拒绝（事实不成立）** | **本轮独立复算否证**：对六个中心坐标做最小二乘直线拟合 `lat = −0.1425·lon + 34.3128`，**各点垂直残差最大 3.039°（约 337 km）**，六点远非共线。CA-14.6.1 自己也把本项标为「**表意说法，不是几何事实**」。**结论：不得写入。**（V6 的 1.4 已经用 `from Vancouver on the Pacific coast to Montreal in the east` 表达了「西端到东端」的跨度，无需重复。） |
| **T3-2** | 国土面积的来源 | **❌ 拒绝** | 会把未经核实的「一千万平方公里」变成需要辩护的数字。**本项目未取得可引用的国土面积来源**（官方表 98-10-0011 的 `LANDAREA` = 8,788,702.80 km²，与 V6 的「ten million」差约 13.8%）。**该项已升级为独立待裁定问题 A-1，见 §五。** |
| **T3-3** | 51.8 km / 21.1% 的测量条件 | **✅ 部分采纳** | 第 3 章 **3.5 段末** | **+28 词** | 只采纳其中的**测量条件**部分：`It is also a measurement, not a physical fact: it uses five-kilometre sampling and a twenty-five kilometre threshold.`（18 词）＋ `Measure with a tighter threshold and more gaps would appear.`（10 词）。**不采纳 51.8 km 这个数字的重复表述**（3.4 已给 52 km，重复即空洞）。CA-14.6.1 指出该数字是 5 km 采样特有的（10 km 采样下 3A 报告给出 53.8 km / 24.8%），因此**说明测量条件比重复数字更有价值**。 |
| **T3-4** | 均值 20 万 vs 2.7 万，加一句「典型中心比平均小得多」 | **❌ 拒绝（已由 T2-1 更彻底地实现）** | T3-4 的设计是「不给数字」。但 **T2-1 已在本片给出全片级的中位数 2,992.5 与均值 29,619.9**，同一论点已有更强的数字支撑。再加一句无数字的软化句即**重复论点**，违反任务书 §三.3。另：T3-4 若要给数字需先复现 6,507 / 4,227，该两值**至今未复现**。 |
| **T3-5** | 2.4 的堆叠柱只统计了人口中心里的人 | **❌ 拒绝（已由 T1-4 覆盖）** | 与本片 **5.3 的 T1-4** 属同类口径声明。分镜明确规定 **5.4 镜不得出现任何新数字**，而 2.4 与 5.3 之间的口径已在 2.3、5.1、5.3 三处声明。**在两处重复同一口径声明会削弱最后一章的收束力。** |
| **T3-6** | 仅十个中心就占将近六成 | **❌ 拒绝（与 T2-1 重复）** | CA-14.6.1 自己即建议「二选一」。**已采纳 T2-1**（中位数/均值对），因为它同时承载「集中」与「数学事实」两层意思。 |

**采纳统计**：T1 **5/5** ＋ T2 **6/6** ＋ T3 **1/6（部分）** = **12 项有内容进入 V7**，其中 **T3-3 为部分采纳**，**T2-3 以改写句实现**。若严格按「完全采纳」计，为 **11 项**。

---

## 三、四处改写句（净 0 词，但承载三项扩充内容）

> 这四处都是**把 V6 的一个句子拆成两个句子，总词数不变**。V6 的每一个事实、数字、语序内容**均未被改动**。

| # | 段 | V6 原句 | V7 拆分为 | 净增 | 承载项 |
|---:|---|---|---|---:|---|
| **R1** | 2.3 | `Together, the three provinces hold seventy-eight percent.`（**7 词**） | ① `Those are the three largest; the other ten provinces and territories together hold about twenty-two percent.`（16 词）<br>② `And the three provinces together hold seventy-eight percent.`（8 词） | **+17**（7 → 24） | **T1-2** |
| **R2** | 4.3 | `Answering that would take data this film does not have, and so it stays an open question.`（**17 词**） | ① `Answering that would take data this film does not have: climate, terrain, which land can actually be built on, and a century of change in each of these places.`（29 词）<br>② `And so it stays an open question.`（7 词） | **+19**（17 → 36） | **T1-5** |
| **R3** | 5.3 | `People live outside these boundaries too, and this map does not include them.`（**13 词**） | `About six and a half million people live outside these boundaries, and this map does not include them.`（18 词） | **+5**（13 → 18） | **T1-4** |
| **R4** | 2.3 | `Together, the three provinces hold…` 的引导词 | 改为 `And the three provinces together hold…`，以承接 R1 ① 句 | **0** | T1-2 |

> **R2 的一个受控改动**：V6 的 `, and so it stays an open question.` 中的 `, and so` 被移出，改为 `: … .` ＋ `And so it stays an open question.`。**这是为插入数据清单所必需的最小语法改动，不改变任何命题。**
>
> **合计**：R1 **+17** ＋ R2 **+19** ＋ R3 **+5** ＋ R4 **0** = **+41 词**。
> 与 §四 的 14 句新增 **+183 词** 相加 = **+224 词**，与全稿净增一致。

---

## 四、14 句新增内容（+224 词，逐句实测）

| # | 段 | 插入位置（英文中的前后句） | 新增句 | 词数 | 项 |
|---:|---|---|---|---:|---|
| 1 | 1.2 | 段首，在 `Now watch the six largest…` **之前** | `Officially, a population centre needs at least a thousand people, and a density of four hundred people per square kilometre.` | **20** | T1-1 |
| 2 | 2.2 | 在 `…four and a half million.` **之后**、`More centres, half the people.` **之前** | `Same area, but inside the Toronto square a centre averages about ninety-five thousand people, and inside the Montreal square about forty-eight thousand.` | **22** | T2-2 |
| 3 | 2.3 | 见 §三 R1 的 ① 句 | `Those are the three largest; the other ten provinces and territories together hold about twenty-two percent.` | **16**（净增 +9） | T1-2 |
| 4 | 2.4 | 在 `…in a very small number of places.` **之后** | `Across all one thousand and twenty-six population centres, the median population is about three thousand.` | **15** | T2-1 |
| 5 | 2.4 | 紧接第 4 句 | `The average is nearly thirty thousand, close to ten times larger.` | **11** | T2-1 |
| 5 | 3.3 | 在 `…Toronto's own band holds thirty-one.` **之后** | `Those four are all the corridor contains west of Toronto.` | **10** | T2-3 |
| 6 | 3.4 | 在 `…fifty-two kilometres wide.` **之后** | `Note the denominator: this percentage counts sample points, not people.` | **10** | 本轮新增（分母审计） |
| 7 | 3.5 | 在 `…of some population centre.` **之后** | `It is also a measurement, not a physical fact: it uses five-kilometre sampling and a twenty-five kilometre threshold.` | **18** | T3-3 |
| 8 | 3.5 | 紧接第 7 句 | `Measure with a tighter threshold and more gaps would appear.` | **10** | T3-3 |
| 9 | 4.1 | 在 `…population centre in Canada.` **之后** | `Do not add those two counts together.` | **7** | T2-5 |
| 10 | 4.1 | 紧接第 9 句 | `The twelve territory centres are already inside the fourteen; the two are different ways of drawing one line.` | **18** | T2-5 |
| 11 | 4.1 | 紧接第 10 句 | `And that line is only a reference; the north is not actually divided at sixty degrees.` | **16** | T2-6 |
| 12 | 4.3 | 见 §三 R2 的 ① 句 | `…data this film does not have: climate, terrain, which land can actually be built on, and a century of change in each of these places.` | **16**（净增 +12） | T1-5 |
| 13 | 5.1 | 在 `…about fifty-nine percent.` **之后** | `Those percentages share one denominator: the people who live in population centres, not Canada's population.` | **15** | T1-3 |
| 14 | 5.3 | 见 §三 R3 | `About six and a half million people live outside these boundaries, and this map does not include them.` | **5**（净增） | T1-4 |
| | | | **合计（新句全句词数）** | **193** | |

> **核对**：§四 新句 **+193 词** ＋ §三 改写净增 **+41 词** = **+234 词**，与全稿净增 **+234 词**一致；删除 **0 句**。
>
> **注**：表中第 3 句（16 词）与第 12 句（16 词）是 R1 ① 与 R2 ① 的新句，其**净增**分别为 +9 与 +12（因替换了 V6 的 7 词与 17 词原句）；净增口径以 §三 为准，本表用「新句全句词数」以便与英文正文逐句核对。

---

## 五、本轮新发现、需人工裁定的 5 项

| # | 事项 | 说明 | 建议 |
|---:|---|---|---|
| **A-1** | **V6 的「Ten million square kilometres of land」未经核实** | 官方表 98-10-0011 的 Canada 行 `LANDAREA` = **8,788,702.80 km²**，比「ten million」低 **约 13.8%**。若指南北与水域总面积，Canada 约 9.98M km²，「ten million」接近但仍是取整上界。**本项为 V6 既有语句，本次未改动、也未新增。** | 请人工裁定：(a) 保留 V6 原文；(b) 改为官方土地面积量级「almost nine million square kilometres」；(c) 补一条可引用来源。**本稿按「不擅自改动已冻结正文」处理，保持原样。** |
| **A-2** | **2.2 的「Same area」是口语近似** | 两个方块按同一纬度带宽与经度带宽构造，面积随纬度略有差异（约 203.1×200.0 km 与 196.8×200.0 km），合计 **79,990 km²**。V6 原句已用 `Together they cover about eighty thousand square kilometres`（约数），故「Same area」与其一致。 | 若人工要求更严格，可改为 `Each covers about forty thousand square kilometres`。**本稿保留「Same area」**，因它与同章已给的「about eighty thousand」同一精度层级。 |
| **A-3** | **3.3 带计数的口径差异（V6 既有）** | V6 与分镜记录「多伦多以西湖四个带共 **109** 个中心」。本轮按走廊 BOUNDS（lon −81.6~−70.4、lat 42.30~47.05）独立分带，最近四个带为 118 个（若含被截断的 −82.0~−81.5 带则 122 个）。**差异源于带计数的锚点与纬度带定义，本轮未能定位权威算法。** | **本稿未改动 V6 的 109 / 31 等任何数字**（改写的第二句紧接原第一句，不改动原句）。**请人工裁定是否需要复核 3.3 的带计数基准。** 这是一处**可能影响画面与旁白一致性的既有风险**，不是 V7 引入的。 |
| **A-4** | **N 口径（23 s 还是 18 s）** | 若「结尾收束 5 s」与镜头 5.4 拍 d 的结尾静默是**同一段**，则 N = 18 s，成片减少 5 s。**两者必须择一，不得相加。** | 请人工裁定。本稿两种口径的时长均已列出（审查报告 §三）。 |
| **A-5** | **1,198 词是否可接受** | CA-14.6.1 的目标是 1,162 词。本稿 1,198 词（+36 词 = +3.1%）**同时满足两个条件**：① **9 分钟底线（540 s）在三档语速下全部成立**，最小余量 15.4 s（135 wpm）；② **135 wpm 下成片 555.4 s = 9 分 15 秒，几乎精确命中 9:15 目标（仅超 0.4 s）**。相比之下，CA-14.6.1 的 1,162 词在 135 wpm 下为 **539.4 s，差 0.6 s 跌破底线**；过底线的最低词数是 1,164 词（余量仅 0.3 s，实际不可用）。 | 请人工裁定：(a) 接受 1,198 词（推荐：底线三档全过，且 135 wpm 命中 9:15）；(b) 回到 1,162 词并把章节卡从各 3 s 收到各 3.15 s；(c) 其他。 |

---

## 六、纪律自检

| 检查项 | 结果 |
|---|---|
| 是否修改了 V6 | **否。** V6 文件未被写入，本轮复算仍为 964 词 |
| 是否修改了原始分镜（CA-14.5.1 / CA-14.5.2） | **否** |
| 是否修改了 CA-14.6.1 / CA-14.6.2 历史报告 | **否** |
| 是否删除了 V6 的任何一句 | **否（0 句）** |
| 是否恢复了已撤回的数字（424 / 58.77% / 约 1.5 倍 / 0.8843 / Gini / 18.12 / 17,859,490 / 0.2356 / 53.8 km / 24.8% / 5,059.5 km） | **否，0 处** |
| 是否新增了未经核实的事实 | **否。** 新增内容事实依据见 §二、§四；本轮另新核验了官方人口中心定义、8/41,188、12/14 包含关系、中位数/均值/倍数四项 |
| 是否为凑词数而写句子 | **否。** 14 句新增全部对应 T1/T2/T3 编号；**拒绝 8 项**（含 T3-1 因事实不成立、T2-3 之外的 T3-2/T3-4/T3-5/T3-6 因重复或未核验） |
| 是否引入气候／地形／历史／经济因果解释 | **否。** 4.3 用 `Answering that would take data this film does not have: …` 列举句式 |
| 是否把人口中心写成 city / metropolitan / CMA / 城市 | **否。** 全稿 `city / cities / metropolitan / metro / CMA / urban area / built-up area` 出现 **0 次** |
| 是否生成了配音／地图／动画／视频 | **否。** 本任务只产出文本 |
| 是否冻结了 V7 | **否。** 本稿是候选稿 |

---

## 七、相关文件

- 英文候选稿：[CA14_7_1_NARRATION_V7_CANDIDATE.md](CA14_7_1_NARRATION_V7_CANDIDATE.md)
- 中文对照稿：[CA14_7_1_NARRATION_V7_CHINESE_REVIEW.md](CA14_7_1_NARRATION_V7_CHINESE_REVIEW.md)
- 审查报告：[CA14_7_1_V7_AUDIT_REPORT.md](CA14_7_1_V7_AUDIT_REPORT.md)

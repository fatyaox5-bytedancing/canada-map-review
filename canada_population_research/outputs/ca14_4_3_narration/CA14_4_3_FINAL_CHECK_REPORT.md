# CA-14.4.3 Final Check Report（V3 → V4）

**性质**：最后一轮有限修改。**只记录实际修改、事实口径与剩余风险。**
**未生成**分镜、图片、地图、音频或视频；**未覆盖** V1 / V2 / V3 及任何历史版本。

**输入**：`CA14_4_2_NARRATION_V3_CANDIDATE.md`、`CA14_4_2_FINAL_REVIEW_REPORT.md`，以及 CA-04A 的机器可读产物（`_ca04a_centres.csv`、`_ca04a_stats.json`、`CA04A_SPATIAL_STATISTICS.csv`）。

---

## 一、修改汇总

| # | 位置 | 改动 | 词数变化 |
|---:|---|---|---:|
| 1 | 第 3 章开头 | 删「Most of those places」，改为直接描述走廊；补「三个最大中心在西部」 | +17（含第 2 项） |
| 2 | 第 3 章经度带 | 保留限定，改为「均值被少数超大中心拉高；中位约差 1.5 倍」 | 同上 |
| 3 | 第 4 章北部口径 | 三处措辞修正 | −5 |
| 4 | 第 5 章 34 中心距离 | 明确 561 组全部两两组合的中位数 | +18 |

**全片词数**：V3 **841** → V4 **871**（**+30**）

| 章 | V3 | V4 | 135 wpm | 140 wpm | 150 wpm |
|---:|---:|---:|---:|---:|---:|
| 1 | 112 | **112** | 50 s | 48 s | 45 s |
| 2 | 152 | **152** | 68 s | 65 s | 61 s |
| 3 | 261 | **278** | 124 s | 119 s | 111 s |
| 4 | 167 | **162** | 72 s | 69 s | 65 s |
| 5 | 149 | **167** | 74 s | 72 s | 67 s |
| **合计** | **841** | **871** | **387 s** | **373 s** | **348 s** |

**时长说明**：按任务要求，**接受当前长度，不为达到 379 秒而填充或删减内容**。本次修改的顺序完全由事实准确性决定，未考虑时长目标。

> ⚠️ **所有时长均为按词数估算，无任何实测。** 本项目 TTS 路径被沙箱阻断（CA-13.4 已穷尽 6 条路径），**没有任何一段旁白被实际试读或合成过**。

---

## 二、第 1 项｜第 3 章开头的指代修正

**V3（被替换）**

> Where are those places? Most of those places draw one corridor: southern Ontario down to Quebec City, following the St. Lawrence. Inside the map we drew for it, four hundred and fourteen population centres hold fifty-nine percent of the total. But three of the six largest sit far to the west.

**为什么必须改**：

1. `Where are those places?` 在第 2 章已答（极少数地方），是重复设问。
2. **`Most of those places` 指代不清，且可能被理解为「414 个中心占 1,026 个中心的多数」。** 这是错误的：414 与 1,026 是**两个不同的统计口径**（414 = 投影像素形心口径的走廊内中心；1,026 = 全国人口中心总数），**且 CA-14.3 §四.3 已记录 424 与 414 的差值归属未逐一列出，414 是否为 424 的子集都无法证明**，更谈不上「占 1,026 的多数」。
3. `sit far` 的措辞不够正式。

**V4（采用）**

> Those places run in a corridor: population centres strung across southern Ontario and Quebec, following the St. Lawrence. Inside the map we drew for that corridor, four hundred and fourteen population centres hold fifty-nine percent of the total. But three of the six largest are far to the west.

处理要点：

- ✅ **删除 `Most of those places`**，改为直接陈述走廊本身（`population centres strung across southern Ontario and Quebec`）。
- ✅ **不再出现任何「多数」暗示**。`Those places` 回指第 2 章的「极少数几个地方」，不是回指 414 或 1,026。
- ✅ **明确「六个最大中心中有三个在西部」**（`three of the six largest are far to the west`），依据见 §五。
- ✅ `sit far to the west` → `are far to the west`。

---

## 三、第 2 项｜经度带中位数表达的修正

### 3.1 分组口径核对（本次实际复算）

| 项 | Toronto 带 | 以西四带 |
|---|---:|---:|
| 分组依据 | 走廊 BOUNDS 内、`round(lon*2)/2` = −79.5 | 同法 = −81.5 / −81.0 / −80.5 / −80.0 |
| 中心数 | **31** | **109** |
| 人口 | 6,223,244 | 2,916,977 |
| 均值 | **200,750** | **26,761** |
| **中位数** | **6,507** | **4,227** |
| 中位数比值 | — | **1.5394 倍** |

**口径确认**：两组取自同一个 `inb` 列表、同一个 `pop2021` 字段、同一套 BOUNDS、同一个分箱函数；统计量均为**该带内 pop2021 的中位数**（非均值）。复算值与任务给定值一致：**6,507 ✅ / 4,227 ✅**。

### 3.2 V3 的表述问题

**V3（被替换的末句）**

> That gap comes from a few very large centres, not from every centre being bigger. The median centre in Toronto's band is small too.

**问题**：`The median centre in Toronto's band is small too` 只说了 Toronto 一侧，**没有给出中位数的量级差**，观众无法判断「小」是相对什么而言；而且两处中位数实际相差 1.54 倍，并非「都一样小」。

**V4（采用）**

> That average is pulled up by a few very large centres. The median population centre in Toronto's band is only about one and a half times the size of the median one to the west — small, in both places.

处理要点：

- ✅ **平均值与中位数分开表述**：先说明均值被拉高，再给中位数量级。
- ✅ **给出 1.5 倍这个已核验的比值**（1.5394 → 「about one and a half times」），而不是模糊的「小」。
- ✅ **保留「不是所有中心都更大」的限定**（`pulled up by a few very large centres`）。
- ✅ **保留 `small, in both places`**，说明两侧中位数都远低于各自均值（6,507 vs 200,750；4,227 vs 26,761）。
- ✅ 未推广到东西部；未新增指标（「中位数」是既有字段的直接统计量）；未添加成因。

---

## 四、第 3 项｜第 4 章北部口径的三处修正

| # | V3 | V4 | 理由 |
|---:|---|---|---|
| 1 | `Two ways of drawing the same line, and they do not give the same count.` | `Two different ways of defining the north give two different counts.` | 「画同一条线」不准确——两个口径不是同一条线的两种画法，而是**两种不同的定义方式**（行政区 vs 纬度线） |
| 2 | `spread across the northern third of the country` | `spread across Canada's far north` | 「北部的三分之一」是**未经核验的面积比例**（项目无任何省/地区陆地面积字段） |
| 3 | `Two-tenths of one percent of everyone...` | `about zero point two four percent of everyone...` | 0.2356% 的正确一位小数量级是 **0.24%**；`two-tenths`（0.2）**低估且与分母不符** |

**V4 第 4 章开头全文**

> Now fly north of the sixtieth parallel. Two different ways of defining the north give two different counts. The three northern territories hold twelve population centres and sixty-nine thousand people. North of the line, there are fourteen, with seventy-one thousand five hundred and ninety-two people — about zero point two four percent of everyone living in a population centre in Canada.

### 4.1 两套口径独立性的确认

| 口径 | 中心数 | 人口 | 占 1,026 中心人口 | 出处 |
|---|---:|---:|---:|---|
| 三个北方地区（Yukon / NWT / Nunavut，行政区） | **12** | **69,029** | 0.2271% | `CA04A_SPATIAL_STATISTICS.csv` 第 73–85 行（省级人口）与第 86–98 行（省级中心数）中的对应三行 |
| 北纬 60° 以北（纬度线） | **14** | **71,592** | **0.2356%** | 本次只读重算 |

- ✅ 两套数**并列陈述**，各自独立，未相加、未互相替代。
- ✅ 旁白明说 `two different counts`。
- ✅ **0.2356% 的分母是 1,026 个人口中心的人口**，旁白写为 `of everyone living in a population centre in Canada`，分母已限定；**未被说成占加拿大全国人口的比例**。
- ✅ 未出现 `two-tenths of one percent`（程序化检索 0 处）。

---

## 五、第 4 项｜1,400 km 的口径确认（本次实际复算）

### 5.1 原始计算口径的核验方式

用 `_ca04a_centres.csv`（1,026 行）取人口最大的 34 个中心，**自行计算全部 C(34,2) 两两组合**的 haversine 距离（R = 6371.0088），再与 `CA04A_SPATIAL_STATISTICS.csv` 第 123 行的报告值比对。

**阈值切分确认**：第 34 个 = Saint-Jérôme（100,859 人）；第 35 个 = Red Deer（99,846 人）→ 阈值确实切在第 34 / 35 之间 ✅

### 5.2 三种候选口径的对照（决定性问题）

| 口径 | 组合数 | 中位数 | 与报告值 1,392.5 的关系 |
|---|---:|---:|---|
| **全部两两组合 C(34,2)** | **561** | **1,392.4855 km** | ✅ **完全一致** |
| 最近邻距离 | 34 | 15.2800 km | ❌ 相差约 91 倍 |
| 沿人口排序相邻 | 33 | 1,223.4918 km | ❌ 相差 169 km |

**结论：报告使用的确实是全部 561 组两两组合**，既不是最近邻，也不是相邻配对，也不是抽样。（附加数据：最小值 19.5856 km，最大值 5,059.4951 km，平均值 1,743.4996 km）

### 5.3 V3 的表述问题与 V4 的修正

**V3（被替换）**

> And the opposite is also true. Take the thirty-four largest population centres, spread right across the country, and the distance between any two of them is still about one thousand four hundred kilometres.

**问题**：`the distance between any two of them is about one thousand four hundred kilometres` **字面意思是「任意两者之间都约 1,400 公里」**，而实际范围是 19.6 km 到 5,059.5 km。这是**明确的错误表述**。

**V4（采用）**

> And the opposite is also true. Take the thirty-four largest population centres, spread right across the country. Pair them up every possible way — five hundred and sixty-one pairs — and the median distance across all of them is still about one thousand four hundred kilometres. Not the nearest pairs. The middle one.

处理要点：

- ✅ **明确是「所有可能配对」**：`Pair them up every possible way`。
- ✅ **给出组合数 561**，观众可验证这是全部组合。
- ✅ **明确是中位数**：`the median distance across all of them`。
- ✅ **排除最近邻误读**：`Not the nearest pairs. The middle one.`（与第 1 章 15 组距离的表述方式保持一致）
- ✅ **删去 `the distance between any two of them`** 这一错误说法。

---

## 六、保持不变的内容（逐项确认）

| 项 | V4 状态 |
|---|---|
| 六个最大中心的 **15 组两两距离中位数约 2,698.1 km** | ✅ `fifteen distances` + `the median of those fifteen` + 2,700 公里；未改动 |
| 两个 200 km × 200 km 网格、**80,000 km²**、**43%** | ✅ 未改动，分母写明 |
| **414** 个走廊中心，旁白 **59%**，画面精确值 **58.7%** | ✅ 未改动；旁白未念精确值；**未再出现任何「多数」暗示** |
| 走廊主证据 **51.8 km / 21.1%**，段长 **232 km** | ✅ 未改动 |
| 省级百分比分母为 **1,026 个人口中心合计人口** | ✅ 未改动，`not of Canada` 保留 |
| 不恢复未经核验的面积类比 | ✅ **0 处**出现 Ireland；`northern third` 已删除 |
| 不添加气候/地形/历史/经济成因推测 | ✅ 0 处；第 3 章新增句亦为纯空间描述 |
| 接受当前长度，不为 379 秒填充或删减 | ✅ 本次修改顺序由事实准确性决定 |

---

## 七、剩余风险与未解决事项

### 7.1 仍然存在的方法论残留

1. **经度带比较的纬度带不完全相同**：Toronto 带纬度跨度 3.40°，以西四带 4.08°。因此「平均约 20 万 vs 2.7 万」只能在**这两个经度带之间**成立，不能外推。V4 未做任何外推。
2. **以西四带被 BOUNDS 西界截断**：lon −81.75 ~ −81.6 另有 8 个中心（41,188 人）落在走廊边界外未计入。V4 未使用「Toronto 以西全部」之类措辞。
3. **414 与 424 的成员关系仍无法证明**：人口上相容（差 30,365 人），但 10 个差值中心的归属未逐一列出。V4 旁白 0 处出现 424。
4. **中位数 6,507 / 4,227 的口径依赖分箱边界**：0.5° 经度箱的边界位置会影响结果。若要更强稳健性，需做**分箱边界敏感性检验**（本次未做）。**这是 V4 中唯一一个「已核验但未做敏感性检验」的数字。**

### 7.2 技术限制

1. **所有时长为按词数估算，无实测。** 无任何旁白被真正朗读过。
2. **英文为书面稿，未经英语母语者朗读测试。**
3. **`PCCLASS` 官方含义未确认**；V4 避开任何依赖该码值的表述，只说 `A population centre is where people are concentrated`。
4. **population centre 的官方定义文本本项目未取得**，V4 未宣称完整定义。

### 7.3 承接前几轮、仍未裁定的事项

| # | 事项 | 现状 |
|---:|---|---|
| 1 | 画面文字用 58.67% 还是 58.7% | 旁白念 59%；**58.77% 不得使用**（424 口径） |
| 2 | 是否恢复「爱尔兰岛」类比 | V4 未恢复；该项目从未核验 |
| 3 | 是否接受按 135 wpm 的 387 秒估算 | 任务已指示接受当前长度，本报告不再建议改动 |

---

## 八、程序化纪律自检结果

（对 V4 英文正文运行，非人工目视）

| 检查项 | 结果 |
|---|---|
| city / cities（人口中心称谓） | **0** ✅（Quebec City 作为地名 2 次，已剔除） |
| metropolitan / metro / CMA / urban area | **0** ✅ |
| built-up area | **0** ✅ |
| scattered / isolated / remote | **0** ✅ |
| **`Most of those places`** | **0** ✅（本次删除） |
| **`northern third`** | **0** ✅（本次删除） |
| **`two-tenths of one percent`** | **0** ✅（本次替换为 0.24%） |
| **`the distance between any two of them`** | **0** ✅（本次删除） |
| all in the east 类绝对表述 | **0** ✅ |
| 18.12 / Gini / 0.8843 / 0.80 | **0** ✅ |
| 424 / 226 km / 53.8 / 24.8 / 17,859,490 | **0** ✅ |
| island of Ireland | **0** ✅ |
| 0.2356 / 2,698.1（应口播取整而非原值） | **0** ✅ |
| 必需表述 23 项 | **全部在位** ✅ |

> **综合自检结果：通过。**

---

## 九、本次执行的只读计算

1. 取人口最大的 34 个中心，自行计算**全部 C(34,2) = 561 组** haversine 距离中位数 → **1,392.4855 km**，与 `CA04A_SPATIAL_STATISTICS.csv` 第 123 行一致；并用最近邻口径（15.2800 km）与相邻口径（1,223.4918 km）**反向确认**报告未使用这两种口径。
2. 确认 34 / 35 的阈值切分点（Saint-Jérôme 100,859 / Red Deer 99,846）。
3. 复算 Toronto 带与以西四带的**中位数** → **6,507 / 4,227**，比值 **1.5394**；并确认分组口径（同一 BOUNDS、同一分箱函数、同一 `pop2021` 字段）。
4. 复核 0.2356% 的一位小数量级 → **0.24%**，据此改写口播。

**未执行**：未重跑空间分析；未做多边形裁剪；未做分箱边界敏感性检验；未改任何已有文件；未生成分镜、图片、地图、音频或视频；未联网。


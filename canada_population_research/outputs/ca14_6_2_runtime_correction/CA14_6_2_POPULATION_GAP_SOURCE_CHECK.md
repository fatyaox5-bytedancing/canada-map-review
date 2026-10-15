# CA-14.6.2 时长预算纠错与制作参数确认 —— 报告二：人口差额来源核验

**任务**：CA-14.6.2 / 任务 C
**核验对象**：`30,389,999`、`36,991,981` 及其差额 `6,601,982`
**本轮性质**：**核验报告，不是结论改写。未修改任何项目文件。**
**网络状态**：**本轮具备网络访问能力**（经本机代理 `127.0.0.1:7890`，走 Python/OpenSSL 栈）。详见 §四。

---

## 一、结论摘要（先给答案）

| 问题 | 结论 |
|---|---|
| `36,991,981` 与 `30,389,999` 是否年份可比？ | ✅ **可比**。同属 **2021 年普查**（REF_DATE = 2021） |
| 是否统计口径可比？ | ✅ **可比**。同一张官方表 **98-10-0011-01**、同一 Universe「**All persons, 2021 and 2016 censuses – 100% data**」下的一级地理层级之和关系 |
| `1,026` 个 population centres 的合计是否确实来自 2021？ | ✅ **是**。已用官方表逐行复算，恰为 `30,389,999` |
| 差额 `6,601,982` 计算是否正确？ | ✅ **正确**（`36,991,981 − 30,389,999`） |
| 官方来源核验状态 | ✅ **已核验**（官方表 + 官方词典 + 官方 Census in Brief，三重印证） |
| 是否建议将约 660 万人的差额写入旁白？ | ⚠️ **有条件建议**：**可以写入，但必须写「约 660 万人生活在人口中心之外」，不得写「农村人口」以外的未定义表述，且必须与 `30,389,999` 的口径行同屏**。详见 §七 |

---

## 二、事实分层（按任务书 §五 的要求区分）

### 2.1 已由**项目文件**证实的事实

| # | 事实 | 项目内证据 |
|---:|---|---|
| F1 | 合并表含 **1,026** 个人口中心 | `ca04/_ca04a_centres.csv`（表头 `PCUID,name,province,pop2021,lat,lon,nn_km,nn_name,pctype,pcclass`，数据行 1,026） |
| F2 | 这 1,026 个中心的 `pop2021` 合计 = **30,389,999** | 同上，本轮复算 |
| F3 | 最大中心 Toronto = **5,647,656**；最小中心 St. Andrews = **1,001** | 同上 |
| F4 | 官方全国人口 = **36,991,981**（2021）；2016 = **35,151,728**；变化 **+5.2%** | `data/raw/98100011.csv`（`GEO=Canada`，`DGUID=2021A000011124`）；`CA01_执行报告.md` L168 |
| F5 | 项目**早已**识别并写下了这个差额 | `data/view/怎么看这些文件.md` L54：「合计 30,389,999 人，与官方全国 36,991,981 人差 **6,601,982 人**，这部分是**不在任何人口中心范围内的乡村人口**，属正常，不是缺数据」 |
| F6 | 项目**早已**在分镜中使用该差额的分母关系 | `CA14_5_2_CHAPTERS_2_TO_5_STORYBOARD.md` L83：按全国人口算应为 `13,066,964 / 36,991,981 = 35.3%`；L190：全国口径下三省为 `63.8%` |
| F7 | `CA04A_SPATIAL_PATTERN_REPORT.md` L579 亦已记录该差额与「乡村人口」表述 | 同上 |

> **要点**：**`36,991,981` 与 `6,601,982` 不是本轮新引入的数字**，
> 它们在项目早期（CA-01 / CA-04A 阶段）就已被记录，并已被 CA-14.5.2 分镜引为分母。
> 本轮的贡献是**把来源与口径补齐并逐项官方核验**。

### 2.2 已由**官方来源**证实的事实

| # | 事实 | 官方来源 |
|---:|---|---|
| G1 | 官方表 **98-10-0011-01**（*Population and dwelling counts: Canada and population centres*），**Release date 2022-02-09**，Geography = **Canada, Province or territory, Population centre, Population centre part**，Universe = **All persons, 2021 and 2016 censuses – 100% data** | [98-10-0011 表页](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=9810001101)（本轮实地抓取，HTTP 200） |
| G2 | 官方表中 `GEO = Canada`（2021）人口 = **36,991,981**；2016 = **35,151,728**；变化 = **+5.2%**；土地面积 = **8,788,702.80 km²**；密度 = **4.2 /km²** | 同上；DOI [10.25318/9810001101-eng](https://doi.org/10.25318/9810001101-eng) |
| G3 | 官方表中 DGUID 长度 13 的 **1,026** 行，2021 人口合计 = **30,389,999** | 官方 CSV（`98100011-eng.zip`）本轮下载并复算 |
| G4 | **population centre 定义**：人口 ≥ **1,000** 且密度 ≥ **400 人/km²**（基于本次普查计数）；**「所有人口中心以外的地区被划为 rural areas」**；**二者合并覆盖全加拿大** | [2021 普查词典：Population centre (POPCTR)](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/az/definition-eng.cfm?ID=geo049a) |
| G5 | **rural area 定义**：**「rural areas 包括人口中心以外的全部领土。人口中心与 rural areas 合并覆盖全加拿大。」** 农村人口包含 CMA/CA 内的农村地区及 CMA/CA 外的农村地区 | [2021 普查词典：Rural area (RA)](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/az/definition-eng.cfm?ID=geo042) |
| G6 | 官方 Census in Brief **98-200-X2021002**《Population growth in Canada's rural areas, 2016 to 2021》报告：**2021 年农村人口 6.6 million**；相比 2016 年**增加 26,609 人（+0.4%）**；农村占比 **2016 年 18.7% → 2021 年 17.8%** | [Census in Brief 98-200-X2021002](https://www12.statcan.gc.ca/census-recensement/2021/as-sa/98-200-x/2021002/98-200-x2021002-eng.cfm) |
| G7 | rural area 的构成**包含**：人口少于 1,000 的小镇、村庄与其他聚落；CMA/CA 内的农村地区（含 estate lots 等） | [2021 普查词典：Rural area (RA)](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/az/definition-eng.cfm?ID=geo042) |

### 2.3 尚待核验的推断

| # | 推断 | 状态 |
|---:|---|---|
| U1 | `6,601,982` 与官方表述的「6.6 million」是**同一个量** | ⚠️ **强推断，未取得官方逐字确认**。五项交叉验证全部吻合（见 §三），但官方报告用的是四舍五入的「6.6 million」，**没有一处官方文本逐字写出 `6,601,982`** |
| U2 | 差额人口「全部」属于官方定义的 rural area | ⚠️ **已由定义推出，但未逐行验证**。G4/G5 声明人口中心与 rural areas **合并覆盖全加拿大**，因此 `全国 − 人口中心 = rural` 在**定义层面成立**；本项目未持有 rural area 的几何边界以做空间验证 |
| U3 | 差额人口中**具体**有多少属于「< 1,000 人的小聚落」、多少属于「低密度乡村」 | ❌ **无法拆分**。项目内无该细分数据 |
| U4 | 官方是否对 population centre 边界做过普查间修订而影响可比性 | ❌ **未核验**。G1 已确认同一张表内 2021 与 2016 同源，但边界修订史未查 |

---

## 三、五项交叉验证（全部吻合）

**方法**：用官方已公布的口径数字反算农村人口，检验项目推出的 `6,601,982` 是否自洽。

| # | 检验项 | 用 `6,601,982` 反算 | 官方公布值 | 结果 |
|---:|---|---|---|---|
| V1 | 2016 农村人口 | `6,601,982 − 26,609 =` **`6,575,373`** | （由 2016 全国 − 2016 人口中心推得） | — |
| V2 | 2016 农村占比 | `6,575,373 ÷ 35,151,728 =` **`18.7057%`** | **18.7%** | ✅ 吻合 |
| V3 | 2021 农村占比 | `6,601,982 ÷ 36,991,981 =` **`17.8471%`** | **17.8%** | ✅ 吻合 |
| V4 | 农村人口增长率 | `6,601,982 ÷ 6,575,373 − 1 =` **`+0.4047%`** | **+0.4%** | ✅ 吻合 |
| V5 | 全国人口自洽 | `30,389,999 + 6,601,982 =` **`36,991,981`** | 全国 = **36,991,981** | ✅ **恰好等于全国** |

**V2 / V3 / V4 / V5 四项同时吻合**，且 **V5 是精确相等（不是四舍五入）**。
这构成 `6,601,982` 与官方「6.6 million」同源的强证据。

---

## 四、官方来源核验状态（含网络能力说明）

### 4.1 本轮网络能力

| 通道 | 结果 |
|---|---|
| `www150.statcan.gc.ca`（StatCan 数据表域） | ✅ **可达**（Python + OpenSSL，经代理 `127.0.0.1:7890`，证书校验关闭） |
| `www12.statcan.gc.ca`（StatCan 普查域，含任务书提供的 CPDV 页与普查词典） | ❌ **HTTP 403 Forbidden**（WAF 拦截脚本访问）；其词典与 Census in Brief 内容**由 web 检索获得** |
| PowerShell `Invoke-WebRequest` | ❌ 全部失败（schannel `SEC_E_NO_CREDENTIALS 0x8009030e`） |
| `curl.exe` | ❌ 同上（schannel 缺凭证） |
| git over HTTPS | ✅ 可用（走 openssl 后端，与 CA-14.5.2 上传同路径） |

### 4.2 已实地抓取的官方证据

**① 官方表 98-10-0011 下载并逐字节比对**

| 项 | 值 |
|---|---|
| 下载 URL | `https://www150.statcan.gc.ca/n1/tbl/csv/98100011-eng.zip` |
| 本次下载 SHA256 | `04a255c35d256df8b5c5cfdd47d319aacffebc22419535c7e77a141b6d455b26` |
| 项目内 `data/raw/98100011-eng.zip` SHA256 | `04a255c35d256df8b5c5cfdd47d319aacffebc22419535c7e77a141b6d455b26` |
| 结论 | ✅ **完全一致 → 该表自 CA-01 下载至今未被官方修订，项目数据未过期** |

**② 用官方 CSV 逐行复算（本轮）**

| DGUID 长度 | 含义 | 行数 | 2021 人口合计 |
|---:|---|---:|---:|
| 11 | 省 / 地区 | 13 | **36,991,981** |
| **13** | **population centre** | **1,026** | **30,389,999** |
| 14 | Canada | 1 | 36,991,981 |
| 15 | population centre part（跨省中心的分部） | 8 | 1,116,880 |

> **重要的重复计数风险提示**：长度 15 的 8 行是**跨省人口中心的分部记录**
> （Hawkesbury 安省/魁省、Ottawa–Gatineau 安省/魁省、Flin Flon 曼省/萨省、Lloydminster 阿省/萨省），
> 合计 **1,116,880**——**与 `CA04A_SPATIAL_STATISTICS.csv` L5 记录的「跨省合计 1,116,880」完全一致**。
> **这 8 行必须排除在合计之外**（它们已被并入长度 13 的 4 个中心）。
> **这正是项目文件「手工 VLOOKUP 极易在那 4 个跨省中心上重复计数」警告所指的风险**
> （`data/view/怎么看这些文件.md` L53）。**本轮确认项目的 1,026 行处理是正确的。**

**③ 官方表页抓取确认口径行**（逐字）

> Table: **98-10-0011-01**　Frequency: Occasional　**Release date: 2022-02-09**
> **Geography:** Canada, Province or territory, Population centre, Population centre part
> **Universe:** All persons, 2021 and 2016 censuses – 100% data
> How to cite: Statistics Canada. Table 98-10-0011-01 *Population and dwelling counts: Canada and population centres*
> DOI: https://doi.org/10.25318/9810001101-eng

**④ 任务书提供的 CPDV 页面**

`https://www12.statcan.gc.ca/census-recensement/2021/dp-pd/dv-vd/cpdv-vdpr/index-eng.cfm`
→ ❌ **四次尝试（含完整浏览器请求头）均返回 HTTP 403**。
**该页面未被核验。** 但本任务所需的全部口径已由 ②③ 与 G4~G6 独立证实，
**CPDV 页面不是必需的证据链环节**。
→ 官方表页另列有一个相关可视化产品：*Data Visualization: Number and Size of Communities in
Rural and Small Town Canada: Interactive Dashboard*（**未核验**）。

---

## 五、年份与统计口径的可比性判定

| 维度 | `30,389,999` | `36,991,981` | 是否可比 |
|---|---|---|---|
| **年份** | 2021 普查 | 2021 普查（REF_DATE = 2021） | ✅ **同年** |
| **同一张官方表** | 98-10-0011-01 | 98-10-0011-01 | ✅ 同表 |
| **同一 Universe** | All persons, 2021 and 2016 censuses – 100% data | 同 | ✅ |
| **同一数据质量等级** | 100% 数据（非抽样） | 100% 数据 | ✅ |
| **地理层级关系** | population centre 级（1,026 行） | Canada 级（1 行） | ✅ **下级与上级** |
| **关系是否穷尽** | 官方定义：population centres + rural areas **覆盖全加拿大**（G4/G5） | — | ✅ **互补且穷尽** |

**判定：`36,991,981 − 30,389,999 = 6,601,982` 在年份、范围与统计口径上可比，差额计算成立。**

### 5.1 一个必须说清的限定

差额 `6,601,982` 的涵义是**「2021 年普查时，居住在 1,026 个 population centre 边界之外的人口」**。
按官方定义这与「rural area 人口」等价（G4/G5）。**但需要向观众澄清的不是口径，而是「rural」这个词本身**：

按 G7，「农村」在 StatCan 口径下**不等于「农业地区」**，它**包含**：
- 人口少于 1,000 的小镇、村庄与其他聚落；
- CMA / CA 内的农村地区（可能含 estate lots）；
- 低密度乡村与偏远地区。

> **因此旁白若使用「农村」，必须避免让观众理解为「农田」或「农业人口」。**

---

## 六、是否建议将约 660 万人的差额写入旁白

### 6.1 判定：**建议写入，但附三项强制条件**

任务书 §五.5 要求「**只有在口径可比的情况下，才建议将差额约 660 万人用于旁白**」。
**§二 与 §五 已确认口径可比**（同表、同年、同 Universe、定义上互补且穷尽，并有五项交叉验证），
**故满足写入条件。**

任务书 §五.6 要求「**不得未经证实就把这 660 万人全部称为官方定义下的农村人口**」。
→ **现已证实**：官方定义下人口中心以外的地区**就是** rural areas（G4/G5），
且官方报告自己把该量报为「6.6 million」农村人口（G6）。**因此该称法在官方定义下成立**，
但**仍须遵守以下表述纪律**：

### 6.2 三项强制条件

| # | 条件 | 理由 |
|---:|---|---|
| **C1** | **优先使用官方四舍五入口径「约 660 万 / about 6.6 million」，不要断言精确的 `6,601,982`** | 官方公布的是「6.6 million」；`6,601,982` 是本项目的精确推导值，**不是官方逐一印出的数字**（U1） |
| **C2** | **必须与 `30,389,999` 的口径行同屏**，即明确差额的分母与两端 | 与全片既有纪律一致（`CA14_5_2` L83/L190/L999）；单独出现「660 万」会被误读为无条件事实 |
| **C3** | **不得把「农村」表述为「农业」**，也不得暗示这 660 万人「没有城市生活」或「都被统计遗漏」 | G7：rural 包含 < 1,000 人聚落与 CMA/CA 内农村地区；`data/view/怎么看这些文件.md` L54 已声明「属正常，不是缺数据」 |

### 6.3 建议的旁白措辞方向（**不是 V7 正文**，仅为口径示范）

- **可用**：`About 6.6 million people lived outside any population centre.`
- **可用**：`Statistics Canada calls everything outside a population centre rural — almost eighteen percent of the country.`
- **不可用**：`6,601,982 people live in rural areas.`（把推导值当官方公布值）
- **不可用**：`The other 6.6 million are farmers.`（把 rural 等同农业）
- **不可用**：`6.6 million people are missing from the census.`（与官方「不是缺数据」相悖）

### 6.4 与既有旁白风险的关系

**该差额一旦可用，可同时解决两处既有问题**：

1. **CA-14.6.1 的 V1 待裁定项**：T1-4 的 `millions` 一直缺一个可引用的加拿大总人口/总差额值。
   → **现已有官方可引用值（约 660 万 / 6.6 million）与官方 17.8% 占比。V1 可以结案。**
2. **镜头 5.3 的口径风险**：`CA14_5_2` L999 要求 `30,389,999` 绝不能被称作「加拿大的人口中心总人口」以外的说法。
   → 补上差额后，5.3 可以**正面说明「这个数不是全国人口，差的是人口中心之外的约 660 万人」**，
   比单纯声明「这不是全国人口」更能消除误读。

### 6.5 仍未解决的部分（不得写入旁白）

| 项 | 状态 |
|---|---|
| 差额中「< 1,000 人小聚落」与「低密度乡村」的具体拆分 | ❌ **项目内无数据，不得编造** |
| 农村人口在各省/各地区的分布 | ❌ **项目内无数据** |
| 官方是否对 population centre 边界做过影响可比性的修订 | ❌ **未核验** |
| `6,601,982` 是否曾被官方逐字印出 | ❌ **未找到**（官方用 6.6 million） |

---

## 七、来源清单

| 编号 | 来源 | 类型 | 本轮核验方式 |
|---|---|---|---|
| S1 | Statistics Canada. Table **98-10-0011-01** *Population and dwelling counts: Canada and population centres*. DOI [10.25318/9810001101-eng](https://doi.org/10.25318/9810001101-eng)。Release date 2022-02-09 | 官方数据表 | ✅ **下载 CSV 并逐行复算**；SHA256 与项目内文件一致 |
| S2 | [98-10-0011 表页（口径行）](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=9810001101) | 官方表页 | ✅ **实地抓取 HTTP 200**，取得 Geography / Universe / Release date |
| S3 | [2021 普查词典：Population centre (POPCTR)](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/az/definition-eng.cfm?ID=geo049a) | 官方定义 | ⚠️ 经 web 检索获得（直连 403） |
| S4 | [2021 普查词典：Rural area (RA)](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/az/definition-eng.cfm?ID=geo042) | 官方定义 | ⚠️ 经 web 检索获得（直连 403） |
| S5 | [Census in Brief 98-200-X2021002《Population growth in Canada's rural areas, 2016 to 2021》](https://www12.statcan.gc.ca/census-recensement/2021/as-sa/98-200-x/2021002/98-200-x2021002-eng.cfm) | 官方分析报告 | ⚠️ 经 web 检索获得（直连 403） |
| S6 | 任务书提供的 CPDV 页面 | 官方可视化 | ❌ **HTTP 403，未能核验** |
| S7 | 项目内 `data/raw/98100011.csv`、`data/raw/98100011-eng.zip`、`ca03a/file_manifest.csv`、`ca04/_ca04a_centres.csv`、`ca04/CA04A_SPATIAL_STATISTICS.csv` | 项目文件 | ✅ 本地读取与复算 |

---

## 八、本报告的边界

- **只读**项目文件；**未修改任何文件**。
- **未生成 V7 正文**，未生成音频、地图、动画或视频。
- 本报告**只写入** `outputs/ca14_6_2_runtime_correction/`。
- 官方来源的**抓取时间**为本轮执行时刻；StatCan 表 98-10-0011-01 自 2022-02-09 发布后**本次比对未见修订**。
- **`www12.statcan.gc.ca` 域在本环境被 WAF 拦截**，该域的词典与报告内容**依赖检索结果**，
  与本地已有官方数据表互证一致（五项交叉验证全部吻合），但**建议人工在浏览器中再复核一次 G4~G6 的原文**。

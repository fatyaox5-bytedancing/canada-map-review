# 09 · TRICOLOR-REVISION-01 · 最小修订提案的只读材料提取

> **文件性质**：**只读材料提取**（为人工审查"Tricolor 英文旁白最小修订提案"提供输入）。
> **不是**修订提案本身，**不是**新的事实来源，**不是**规范文件。任何数字与法律状态口径仍以 [`06_TRICOLOR_FACT_CHECK_BATCH_1.md`](06_TRICOLOR_FACT_CHECK_BATCH_1.md) 与 [`03_TRICOLOR_CASE_NOTES.md`](03_TRICOLOR_CASE_NOTES.md) 为准。
> **生成日期**：2026-10-13（周二，UTC+8）
> **上游材料截止日期**：2026-10-12（`04`／`06`／`07` 的最后修改日；本文件不更新上游材料的内容）
> **任务编号**：TRICOLOR-REVISION-01
> **上游文件**：[`04_TRICOLOR_SCRIPT_V1.md`](04_TRICOLOR_SCRIPT_V1.md) ｜ [`06_TRICOLOR_FACT_CHECK_BATCH_1.md`](06_TRICOLOR_FACT_CHECK_BATCH_1.md) ｜ [`07_TRICOLOR_SCRIPT_RISK_REVIEW.md`](07_TRICOLOR_SCRIPT_RISK_REVIEW.md)
> **本文件产出方式**：全部内容来自上述三个文件的**实际读取**，未开展新一轮网络调查，未修改任何现有文件。

---

## 任务目标

为人工审查 Tricolor 英文旁白的最小修订提案，读取以下三个现有文件：

1. `docs/04_TRICOLOR_SCRIPT_V1.md`
2. `docs/06_TRICOLOR_FACT_CHECK_BATCH_1.md`
3. `docs/07_TRICOLOR_SCRIPT_RISK_REVIEW.md`

项目根目录以实际检查结果为准，不得假设固定路径。

### 本任务只读约束

- 不修改任何现有文件。
- 不修改英文旁白、中文翻译、分镜或事实核验报告。
- 不新增项目文件（本文件是用户随后明确要求本地存储的结果）。
- 不开展新一轮大规模网络调查。
- 不自行补写缺失的原句、时间码、证据或法院进展。

### 输出格式要求

按"问题编号 → 章节与时间码 → 英文原句 → 中文翻译 → 事实核验记录 → 风险审查记录"的顺序组织。没有证据支持的字段标记"未确认"，不得补造。

---

## 〇、文件存在性与读取完整性

**项目根目录（实际检查结果）**：`E:\Deepseek Harness工作区\YouTube金融案例视频\Tricolor破产案`

根下实际只有两项：`BehindTheBreakdown\`（生产目录，2026-10-12 17:18:02）与 `_dsh-watch\`（临时诊断工具，21:56:24）。本任务文件全部位于 `BehindTheBreakdown\docs\`。

| 文件 | 存在 | 读取完整性 | 字节 | 行数 | SHA256（前16） |
|---|---|---|---|---|---|
| `docs/04_TRICOLOR_SCRIPT_V1.md` | 是 | **完整**（第 1–321 行全部读过，含归档元信息与归档说明） | 23,392 | **321** | `40D1E0EDB4812014` |
| `docs/06_TRICOLOR_FACT_CHECK_BATCH_1.md` | 是 | **完整**（第 1–486 行全部读过，含第 0 节方法边界、6 项核验、汇总、附录 A/B/C） | 41,705 | **486** | `1D8632E7578D7D5D` |
| `docs/07_TRICOLOR_SCRIPT_RISK_REVIEW.md` | 是 | **完整**（第 1–457 行全部读过，含 23 个条目与汇总五节） | 37,955 | **457** | `0EFFD015147A24B7` |

**工具级勘误（如实报告）**：本机 PowerShell 5.1 的 `Get-Content` 默认按 ANSI 读取 UTF-8 文件，会把多字节中文序列误判成额外换行，因此它报告的 `04`＝257 行、`06`＝395 行**不可靠**。上表行数以 `read` 工具（按 UTF-8 正确解码）为准。字节数与 SHA256 按原始字节计算，不受影响。**此勘误也意味着 2026-10-12 工作日志中 `06`「457 行」的记录偏低，属同一原因；本任务未修改该文件。**

**只读确认**：除本文件本身（用户随后要求存储）外，未创建、未修改、未删除任何文件（详见文末边界确认）。

---

## 一、问题编号 → 章节与时间码 → 英文原句 → 中文翻译 → 事实核验记录 → 风险审查记录

> 定位格式：`04:L行号` 指 `04_TRICOLOR_SCRIPT_V1.md` 第 N 行；`07:条目号` 指风险审查报告中的条目编号。
> 「未确认」＝ 现有材料不支持该字段，按任务要求不补造。

---

### 问题 1 ｜ 2025 年 9 月 10 日及 Chapter 7 申请日期

原稿**有两处**涉及，一处省日期、一处写全日期。

**1a. 章节与时间码**：Chapter 1 — The Business Behind the Collapse ／ 第一章：倒闭背后的生意 ／ **00:00–01:30**

- **英文原句**（`04:L47`，该段前一句）：
  > Tricolor filed for Chapter 7 bankruptcy in September 2025.
- **中文翻译**（`04:L61`）：
  > 2025 年 9 月，Tricolor 申请了美国《破产法》第七章破产保护。

**1b. 章节与时间码**：Chapter 5 — When Funding Dries Up ／ 第五章 ／ **05:55–07:00**

- **英文原句**（`04:L197`）：
  > Tricolor filed for Chapter 7 bankruptcy on September 10, 2025.
- **中文翻译**（`04:L211`）：
  > 2025 年 9 月 10 日，Tricolor 申请了美国《破产法》第七章破产保护。

**事实核验记录**（来源：`06` 第 2 项）

- **核验结论**：`VERIFIED`
- **来源**：① U.S. Attorney's Office, S.D.N.Y.《CEO, CFO, COO Charged In Connection With Billion-Dollar Collapse Of Tricolor Auto》，2025-12-17，`https://www.justice.gov/usao-sdny/pr/ceo-cfo-coo-charged-connection-billion-dollar-collapse-tricolor-auto`（**官方原始文件**）；② ABA Business Law Today（**媒体/机构分析**）；③ Reuters（**媒体**）；④ Charltons Quantum、Yahoo Finance、Investment News（**二手转述**）
- **原始来源是否实际打开并检查**：**否**。SEC/DOJ 域在本机经全部可用通道均不可直接访问（`06` 附录 A.3：justice.gov `fetch failed` 且 DNS 解析为 `157.240.16.50`）。材料性质为**检索索引摘要中转述的官方文件引句（A 级）**，非直连原件。
- **数字口径**：破产程序性质＝**Chapter 7 清算**（ABA 原文 "chapter 7 petition will result in a liquidation"）；日期＝**2025-09-10**；法院＝仅知"得克萨斯州某法院"。
- **已知证据缺口**：**破产法院与庭别无任何来源**（`06` 第四节）；`2026-08-21` 之后的进展未覆盖。
- **报告明确的限制**：`06` 第 0.2 节「我无法获取原始文档正文……引号内英文语句来自模型对检索结果的转述，不是我校验过的页面原文」；反向检索未发现任何来源称 Chapter 11 或给出不同日期。

**风险审查记录**（来源：`07`）

- `07:1-1`｜**LOW**｜数字口径（时间精度）｜"in September 2025" 与 `04:L197` 的完整日期不一致，造成全篇内部不统一｜**建议修改**为 `Tricolor filed for Chapter 7 bankruptcy on September 10, 2025.`
- `07:1-2`｜**LOW**｜其他（程序性质）｜**仅中文侧问题**：`04:L61` 与 `04:L211` 的"第七章**破产保护**"承载 Chapter 11 语义，与 A 级来源对 Chapter 7 的"清算"界定不符｜**建议修改**中文为"第七章**破产清算**"（两处）

---

### 问题 2 ｜ 超过 19 亿美元的 ABS 发行或融资规模

**章节与时间码**：Chapter 4 — What Investigators Allege Happened ／ 第四章 ／ **04:20–05:55**

- **英文原句**（`04:L155`）：
  > According to the Securities and Exchange Commission, Tricolor raised more than $1.9 billion through asset-backed securities offerings between at least 2020 and September 2025.
- **中文翻译**（`04:L171`）：
  > 根据美国证券交易委员会（SEC）的说法，Tricolor 在至少从 2020 年到 2025 年 9 月期间，通过资产支持证券（ABS）发行筹集了超过 19 亿美元。

**事实核验记录**（来源：`06` 第 3 项）

- **核验结论**：`PARTIALLY_VERIFIED`
- **来源**：① SEC Press Release 2026-77，2026-08-18，`https://www.sec.gov/newsroom/press-releases/2026-77-sec-charges-former-executives-fraud-connection-19-billion-collapse-subprime-auto-lender-tricolor`（**官方原始文件**）；② SEC Litigation Release No. 26612，2026-08-18，`https://www.sec.gov/enforcement-litigation/litigation-releases/lr-26612`（**官方原始文件**）；③ Charltons Quantum（**二手转述**）；④ Investment Executive、BankersOnline、Investment News（**媒体/二手**）
- **原始来源是否实际打开并检查**：**否**。sec.gov 直抓返回 **HTTP 403**（反爬）。取得的 A 级证据为 **SEC 新闻稿 P2 句 1**（LR-26612 逐字重复，构成双重确认）。
- **数字口径**：`$1.9 billion` ＝ 19 亿美元；口径为**通过 ABS 发行所募集的资金总额（融资规模）**；统计期间为**"至少自 2020 年至 2025 年 9 月破产"**。**不是诈骗金额、不是投资者损失、不是期末余额。**
- **已知证据缺口**：ABS 发行**起算期间存在冲突**——`06` 记 Charltons Quantum（**C 级单一来源**）称 "Between **2013** and 2025 … through **14** subprime asset-backed securities offerings"，与 SEC 的 "at least 2020" 不一致。`06` 判定**以 SEC 为准**。
- **报告明确的限制**：① `06` 指出 SEC 该新闻稿的 **URL slug 自身写作 `…19-billion-collapse…`**，而标题正文为 `$1.9 Billion`，来源未解释该不一致；② `06` 第 0.2 节对引句性质的限制同上。

**风险审查记录**（来源：`07`）

- `07:4-2`｜**LOW**｜数字口径（期间表述与口径缺失）｜"between at least 2020" 语法生硬；"and September 2025" 可能被读作"截至破产时仍持有"，而 A 级原句为"**期间内累计募集**"｜**建议微调**（可选）为 `…between at least 2020 and its September 2025 bankruptcy.`，**不改变任何数字**
- 另 `07` 第 5 节第 3 项将"自 2013 年起／共 14 次发行"列入**不得写入清单**（C 级单一来源且与 A 级冲突）。

---

### 问题 3 ｜ 22 亿、14 亿、8 亿美元及其上下文

**章节与时间码**：Chapter 4 — What Investigators Allege Happened ／ 第四章 ／ **04:20–05:55**

- **英文原句**（`04:L159`）：
  > A separate criminal indictment alleged that, by August 2025, Tricolor had pledged about $2.2 billion in collateral to lenders and investors while holding only about $1.4 billion in actual collateral—a gap of roughly $800 million.
- **中文翻译**（`04:L175`）：
  > 另一份刑事起诉书指控称，截至 2025 年 8 月，Tricolor 向贷款机构和投资者质押了约 22 亿美元抵押品，而实际持有的抵押品只有约 14 亿美元——差额约为 8 亿美元。

**紧接其后的口径说明段（与本组数字直接相关，需一并保留上下文）**

- **英文原句**（`04:L161`）：
  > Those numbers describe different aspects of the case. The $1.9 billion refers to funds raised through securities offerings. The roughly $800 million figure is an alleged gap between collateral pledged and collateral available. Neither number, on its own, establishes the final losses suffered by investors.
- **中文翻译**（`04:L177`）：
  > 这些数字描述的是案件的不同方面。19 亿美元指的是通过证券发行筹集的资金。约 8 亿美元则是指控中抵押品被质押的金额与可用抵押品之间的差额。单凭其中任何一个数字，都无法确定投资者最终遭受的损失。

- **英文原句**（`04:L163`，本章收束句）：
  > These are allegations made in legal proceedings, not a blanket statement that every transaction was fraudulent or that every investor lost the same amount.
- **中文翻译**（`04:L179`）：
  > 这些都是在法律程序中提出的指控，并不等于说每一笔交易都是欺诈，也不等于说每一位投资者的损失金额都相同。

- **同章相关的指控归属句**（`04:L157` ／ 中文 `04:L173`）：
  > The SEC alleges that hundreds of millions of dollars in auto loans were pledged more than once. It also alleges that loan information was manipulated, making delinquent or defaulted loans appear current or eligible for financing.
  >
  > 美国证券交易委员会（SEC）指控称，数亿美元的汽车贷款被重复质押。起诉还称，贷款信息遭到了操纵，使逾期或违约的贷款看起来仍在正常还款，或者符合融资条件。

**事实核验记录**（来源：`06` 第 4 项）

- **核验结论**：`PARTIALLY_VERIFIED`
- **来源**：① U.S. Attorney's Office, S.D.N.Y. 同题新闻稿（**官方原始文件**，2025-12-17）；② FDIC-OIG 同题新闻稿，Report No. PR-12-17-25（**官方原始文件**）；③ Business Insider、Alternative Credit Investor（2025-12-18）、Texas Lawbook、Cadwalader/Hogan Lovells（2026-01-06）（**媒体/机构分析**）
- **原始来源是否实际打开并检查**：**否**。DOJ 域不可达；**FDIC-OIG 仅取回 oversight.gov 索引条目，未取回正文**。
- **数字口径**：三个数字**口径一致、时点一致**（`06` 明确回答任务书"是否采用相同资产口径、统计时点和计算方法"之问：**是**）。计算关系为减法：`约 22 亿（已质押给贷款人与投资者的抵押品）− 约 14 亿（真实存在的抵押品）= 约 8 亿（被指控为虚假的抵押品）`。统计时点＝**"in or about August 2025"**。
- **已知证据缺口**：**文书出处未闭环** —— `06` 记 DOJ 新闻稿第 7 段位于引导句 "**According to the allegations contained in the Indictment** unsealed today in Manhattan federal court:" **之后**，即公告系**转述**起诉书；**起诉书原件本次未取得**，故该字段标 `PENDING_PRIMARY_SOURCE`。另：DOJ 新闻稿**charges-by-count 段落未取回**（可取回文本止于第 8 段中途）。
- **报告明确的限制**：`06` 第 4 项第 7 点：「是否可写"起诉书载明"，需以一手起诉书文本核实后决定 → `PENDING_PRIMARY_SOURCE`」；并明确「**不得称损失**」「**不得作为法院认定**」。

**风险审查记录**（来源：`07`）

- `07:4-1`｜**MEDIUM**｜指控归属（文书归属精确性）｜"a separate criminal indictment alleged" 的归属**高于**现有证据：`06` 只直接取得 DOJ 新闻稿文本，且该文本自身即用 "According to the allegations contained in the Indictment" 转述｜**建议修改**为 `Federal prosecutors alleged that, by August 2025, …`；**三个数字、减法关系与 "August 2025" 时点全部保留不动**。待一手起诉书取得后可恢复 `indictment alleged`。
- `07:4-4`｜**LOW**｜数字口径｜`04:L161` 与 `06` 口径纪律逐点一致｜**可保留，建议一字不动**（全稿防混淆核心）
- `07:4-5`｜**LOW**｜指控归属｜`04:L163` 明示指控属性并主动排除两种过度推断｜**可保留**
- `07:4-3`｜**LOW**｜其他（量级措辞）｜`04:L157` 的 "hundreds of millions of dollars" 与 SEC 新闻稿 P1 措辞**逐字同调**（A 级）｜**可保留**；**不得**替换为 C 级的 3.655 亿美元具体数

---

### 问题 4 ｜ 9.45 亿美元未偿本金

**章节与时间码**：Chapter 5 — When Funding Dries Up ／ 第五章 ／ **05:55–07:00**

- **英文原句**（`04:L199`）：
  > In an SEC filing announced in August 2026, the agency said that more than $945 million in principal associated with Tricolor's asset-backed securities offerings remained outstanding and payable when the company entered bankruptcy.
- **中文翻译**（`04:L213`）：
  > 美国证券交易委员会在 2026 年 8 月公布的一份诉讼文件中表示，Tricolor 进入破产程序时，与其资产支持证券发行相关、尚未偿还的本金超过 9.45 亿美元。

**紧接其后的口径界定句（与本数字直接相关）**

- **英文原句**（`04:L201`）：
  > That is an outstanding principal figure, not a confirmed estimate of investor losses. The amount ultimately recovered depends on the assets available, the rights of different creditors, and the outcome of the bankruptcy process.
- **中文翻译**（`04:L215`，摘录对应句）：
  > 这是一个未偿本金的数字，并不是对投资者损失的确认估计。最终能够收回多少，取决于可用资产、不同债权人的权利，以及破产程序的结果。

**事实核验记录**（来源：`06` 第 5 项）

- **核验结论**：`VERIFIED`
- **来源**：① SEC Press Release 2026-77（**官方原始文件**，2026-08-18）；② SEC Litigation Release No. 26612（**官方原始文件**，载案号 **No. 26-civ-7041, S.D.N.Y., filed Aug. 18, 2026**）；③ Charltons Quantum（**二手转述**）；④ American Banker（2026-08-20）、Yahoo Finance、generationimpact（**媒体/二手**）
- **原始来源是否实际打开并检查**：**否**（sec.gov 403）。
- **数字口径**：**"与 ABS 发行相关的、在破产时仍未偿付且应付给投资者的本金"**（A 级引句位置：SEC 2026-77 **P2 句 5**；LR-26612 **P2 句 5 逐字相同**）。统计时点＝**"at the time of Tricolor's bankruptcy"**（2025 年 9 月）。适用范围＝ **"the ABS offerings"**（SEC 公告未细分是哪几档）。**不是最终投资者损失，也不是贷款人债权。**
- **已知证据缺口**：**精确数值与发行笔数不充分** —— SEC 写 "more than $945 million"；"approximately **US$945.4 million** … across **seven** ABS offerings" 仅 **C 级单一来源**（Charltons Quantum）。`06` 第五节另记 4 组**易混口径**：DOJ/AP 的"超过 9 亿美元（欠贷款人）"、Cadwalader 的"约 9.23 亿美元"（C 级）、American Banker 的"约 3.655 亿美元（单一贷款人测算重复质押本金）"（C 级）。
- **报告明确的限制**：`06` 第 5 项第 6 点「极易与其他四组数字混淆」；第 0.2 节引句性质限制同上。

**风险审查记录**（来源：`07`）

- `07:5-1`｜**MEDIUM**｜数字口径／其他（文书性质、日期精度、适用范围）｜三处问题：① "SEC filing" 定位不准——A 级载体是 **SEC 新闻稿 2026-77 与 LR-26612**，数字本身出自 SEC **起诉状（complaint）**，新闻稿系转述；② "in August 2026" 精度不足（A 级为 **2026-08-18**）；③ 缺 "to investors"，可能被理解为泛指债务｜**建议修改**为 `In an SEC litigation release dated August 18, 2026, the agency said that more than $945 million in principal associated with Tricolor's asset-backed securities offerings remained outstanding and payable to investors when the company entered bankruptcy.`（中文 `04:L213` 的"一份诉讼文件"应同步调整）。**"more than $945 million" 的取值边界正确，不得换成 about / approximately，也不得加入 "seven offerings"（C 级）。**
- `07:5-2`｜**LOW**｜数字口径｜`04:L201` 准确界定口径｜**可保留，建议一字不动**

---

### 问题 5 ｜ Daniel Chu 的审判日期及法律状态

**章节与时间码**：Chapter 6 — The Legal Cases ／ 第六章 ／ **07:00–08:00**

- **英文原句**（`04:L233`）：
  > Former CEO Daniel Chu has pleaded not guilty to the criminal charges. As of October 2026, his criminal trial is scheduled for January 2027.
- **中文翻译**（`04:L245`）：
  > 前首席执行官 Daniel Chu 对刑事指控表示不认罪。截至 2026 年 10 月，他的刑事审判定于 2027 年 1 月进行。

**事实核验记录**（来源：`06` 第 6.4 项）

- **核验结论**：**`CONTRADICTED`**（第 6 项整体结论为 `CONTRADICTED`，依据即 Chu 审判部分）
- **来源**：① U.S. Attorney's Office, S.D.N.Y. 新闻稿 P1（**官方原始文件**，Chu 的职务与逮捕/过堂，A 级）；② SEC 2026-77 P5（**官方原始文件**，control person liability 与 officer and director bars，A 级）；③ Reuters（**媒体**，原排期 2026-10-19）；④ National Law Review（2026-07/08，**机构分析**，延期申请与 2027-02-01 备选）；⑤ Octus（**二手**，2027-01-25）；⑥ CourtListener 案卷（**法院文书的第三方索引**，U.S. v. Chu, No. 1:25-cr-00579 (S.D.N.Y.)）；⑦ Dealership Guy、Finance News Network（**媒体**）
- **原始来源是否实际打开并检查**：**否**。justice.gov 不可达；CourtListener 直抓 **HTTP 403**（CloudFront）；**法院文书本体本次未取得**。
- **数字口径／事实口径**：Chu **对所有指控不认罪**（B 级，多源）；面临**八项追加起诉书**（含 CFCE，18 U.S.C. § 225，Count One）；法院 S.D.N.Y.，法官 Kevin Castel。**审判日期存在三个版本**：**2026-10-19（原定，B 级）／2027-01-25（C 级）／2027-02-01（备选，C 级）**。
- **已知证据缺口**：**Chu 案件最新排期未取得**（`06` 第四节列 `PARTIALLY_VERIFIED`）；`2026-08-21` 之后的进展未覆盖；`06` 第六节将"Chu 审判日期最终确定值"列为**第 1 优先**复查项。
- **报告明确的限制**：`06` 第 6.4 项「**不得写死"2027 年 1 月"**」，并给出「原排期 **2026-10-19**……辩方申请延期……另有来源称 **2027-01-25**」。

**风险审查记录**（来源：`07`）

- `07:6-1`｜**HIGH**（**全稿唯一 HIGH**）｜法律状态（审判安排）｜"is scheduled for January 2027" 把**三选一且未定**的日期写成确定事实，与 `06` 的 `CONTRADICTED` 直接冲突；且底稿完全未提原定 2026-10-19｜**建议修改（正式发布前必须改）**为：
  > `Former CEO Daniel Chu has pleaded not guilty to the criminal charges. His trial was originally set for October 2026 and has since been adjourned, with a date in early 2027 now under discussion.`
- `07` 汇总第 2 节将其列为 **P0 必改第 1 条**；第 3 节将"任何具体审判日期（2027-01-25 / 2027-02-01）"列入**不得写入清单**；第 5 节将其列为**第 1 优先待补一手证据**。

---

### 问题 6 ｜ SEC 民事诉讼与刑事案件的相关表述

**章节与时间码**：Chapter 6 — The Legal Cases ／ 第六章 ／ **07:00–08:00**

**6a. 三人认罪段（刑事）**

- **英文原句**（`04:L231`）：
  > Former CFO Jerome Kollar and finance executive Ameryn Seibold pleaded guilty in December 2025. Former COO David Goodgame, who was also charged, pleaded guilty in June 2026.
- **中文翻译**（`04:L243`）：
  > 前首席财务官 Jerome Kollar 和财务高管 Ameryn Seibold 于 2025 年 12 月认罪。同样被起诉的前首席运营官 David Goodgame 于 2026 年 6 月认罪。

**6b. SEC 民事诉讼段**

- **英文原句**（`04:L235`）：
  > Separately, in August 2026, the SEC filed a civil lawsuit against Chu, Kollar, and Seibold, alleging securities fraud.
- **中文翻译**（`04:L247`）：
  > 另外，2026 年 8 月，SEC 对 Chu、Kollar 和 Seibold 提起了民事诉讼，指控证券欺诈。

**6c. 法律状态分层说明段**

- **英文原句**（`04:L237`）：
  > The legal process will determine which allegations are established, against whom, and under which laws. Until then, it is important to distinguish between allegations in a complaint or indictment, guilty pleas, and findings made by a court.
- **中文翻译**（`04:L249`）：
  > 法律程序将决定哪些指控能够成立、针对谁、以及依据哪些法律。在此之前，重要的是区分起诉状或起诉书中的指控、认罪陈述，以及法院作出的认定。

**6d. 本章两案关系的过渡句**（`04:L229`）：

> The criminal case and the civil case are not the same thing. They are related, but they are not the same case, and they do not involve exactly the same people.

**事实核验记录**（来源：`06` 第 6.1–6.3、6.5 项）

- **核验结论**：认罪事实以 `VERIFIED`／`PARTIALLY_VERIFIED` 记录；**民事被告名单为 A 级反向确认**；第 6 项整体结论 `CONTRADICTED`（因 Chu 审判部分）
- **来源**：① U.S. Attorney's Office, S.D.N.Y. 新闻稿 **P1、P2**（**官方原始文件**，A 级：P2 原文 "KOLLAR and SEIBOLD pled guilty to fraud charges before U.S. District Judge Lewis J. Liman on **December 16, 2025**. Both are cooperating with the Government."）；② SEC 2026-77 **P5** 与 LR-26612（**官方原始文件**，A 级，民事被告仅 **Chu、Kollar、Seibold**）；③ Reuters（**媒体**，Goodgame **2026-06-24** 认罪、法官 Kevin Castel、six counts、同意配合检方）；④ American Banker（**媒体**，Kollar/Seibold "seven charges"）；⑤ Cadwalader（**机构分析**）
- **原始来源是否实际打开并检查**：**否**（同上，两个官方域均不可达）
- **数字口径／事实口径（四人程序地位，`06` 第 6.5 项）**：

  | 人 | 刑事 | SEC 民事 | 认罪 | 审判 |
  |---|---|---|---|---|
  | Kollar（前 CFO） | 已起诉 | **被告** | **2025-12-16**（七项），配合检方 | 无（已认罪），量刑待定 |
  | Seibold（财务高管） | 已起诉 | **被告** | **2025-12-16**（七项），配合检方 | 无（已认罪），量刑待定 |
  | Goodgame（前 COO） | 已起诉 | **非被告** | **2026-06-24**（六项），配合检方 | 无（已认罪），量刑 "Dec. 4"（**年份未明**） |
  | Chu（前 CEO） | 已起诉（八项，含 CFCE） | **被告** | **不认罪** | 见问题 5 |

- **已知证据缺口**：Kollar／Seibold／Goodgame 的**量刑结果均未取得**；Goodgame 量刑日期仅 C 级且年份未明；**未见任何法院对重复质押或欺诈实体问题的裁判**（`06` 第三节第 11 项）
- **报告明确的限制**：`06` 第 6.3 项写「**SEC 民事诉讼：NOT FOUND —— Goodgame 未被列入 SEC 民事被告**」并标"反向确认"；第 6.5 项"法律状态分层纪律"要求五层分开、认罪只对其本人成立。

**风险审查记录**（来源：`07`）

- `07:6-3`｜**LOW**｜法律状态／指控归属｜`04:L235` 的**被告名单完全正确**（SEC 民事被告**只有这三人**），"alleging" 保持指控口径正确；日期精度略低（A 级为 8 月 18 日）属可选优化｜**可保留**。`07` 特别标注：**三人名单是全稿最容易被顺手改错的一句，务必保留**
- `07:6-2`｜**MEDIUM**｜法律状态（日期精度）｜`04:L231` 月份与年份均正确（A/B 级支持），口播**无需改动**｜**可保留 + 字幕标注建议**：Kollar & Seibold — Dec. 16, 2025；Goodgame — June 24, 2026。**注意不得写成"认罪并被判刑"**
- `07:6-4`｜**LOW**｜指控归属｜`04:L237` 与任务书"四种法律状态不得混淆"完全对应｜**可保留，建议一字不动**
- `07:6-5`｜**MEDIUM**｜法律状态（**漏述导致的可推断错误**）｜`04:L231` 并列"三人均认罪"、`04:L235` 紧接着只列三名民事被告，**两份名单并列时观众极易推断 Goodgame 也在民事被告中**；`04:L229` 的 "they do not involve exactly the same people" 不足以澄清具体人员范围｜**建议修改**：在 `04:L235` 之后增补一句 `Goodgame was not named in the SEC's civil suit.`
- `07` 汇总第 2 节：`6-1` 列 **P0**，`6-5` 列 **P1**

---

### 问题 7 ｜ 其他可能把指控写成已证实事实的句子

**7a.** Chapter 1 ／ 00:00–01:30 ／ `04:L47`（后半句）／ 中文 `04:L61`

> The subsequent investigations raised serious questions about whether the auto loans backing its financing arrangements had been accurately reported—and whether some of the same loans had been used to support more than one claim for funding.
>
> 此后的调查提出了几个严重问题：为其融资安排提供支持的汽车贷款，是否得到了准确披露？是否有一部分贷款，被重复用于支持不止一笔融资？

- **核验记录**：`06` 第 1 项 A 级（SEC P1 "double pledging hundreds of millions of dollars"）＋第 3 项 A 级（P2 句 2 "…when the defendants knew that many had been or would soon be double pledged"）
- **风险审查记录**：`07:1-3`｜**LOW**｜指控归属｜措辞**弱于**现有证据（"raised serious questions about whether"），不构成把指控写成事实｜**可保留**

**7b.** Chapter 3 ／ 03:10–04:20 ／ `04:L125` ／ 中文 `04:L141`

> That distinction is central to the allegations in the Tricolor case.
>
> 这正是理解 Tricolor 案件指控的关键之一。

- **核验记录**：`06` 第 1、4 项——SEC 与联邦检察官均以 double-pledge 为核心指控（A 级）
- **风险审查记录**：`07:3-1`｜**LOW**｜指控归属｜使用 "allegations" 明示指控属性｜**可保留**

**7c.** Chapter 4 ／ 04:20–05:55 ／ `04:L163` ／ 中文 `04:L179`（原文见问题 3）

- **风险审查记录**：`07:4-5`｜**LOW**｜明示"These are allegations made in legal proceedings"，主动排除"所有交易皆欺诈""所有投资者损失相同"两种过度推断｜**可保留**

**7d.** Chapter 6 ／ 07:00–08:00 ／ `04:L237` ／ 中文 `04:L249`（原文见问题 6c）

- **风险审查记录**：`07:6-4`｜**LOW**｜要求区分 complaint/indictment 指控、认罪、法院认定三层｜**可保留，建议一字不动**

**7e.** Chapter 7 ／ 08:00–09:10 ／ `04:L267`、`04:L269`；Chapter 8 ／ 09:10–10:00 ／ `04:L293`、`04:L295`

> The 2008 mortgage crisis and the Tricolor collapse were very different in scale and in their wider consequences…
>
> A security can have a complex structure and still be sound. But complexity cannot make an asset more real…
>
> Tricolor was not the 2008 financial crisis all over again. It was a much smaller collapse in a different part of the credit market.
>
> But its failure raises a question that applies well beyond one used-car lender: when a financial institution says its loans support **billions of dollars** in funding, how can the people providing that money verify the claim?

- **核验记录**：不涉及 `06` 的 Tricolor 事实核验项；`06` 第 3 项 A 级（Tricolor "more than $1.9 billion"）与第 4 项 A 级（DOJ P7 "extended **billions in loans**"）为 `04:L295` 的 "billions" 量级提供支撑
- **风险审查记录**：`07:7-1` **LOW 可保留**；`07:7-2` **LOW 可保留**；`07:8-1` **LOW 可保留**；`07:8-2`｜**LOW**｜数字口径（量级措辞）｜该句为**一般性设问**、非陈述 Tricolor 具体金额；**注意**：若后续改为直接描述 Tricolor，"billions" 将与已确认的 19 亿（$1.9B）口径不一致｜**可保留（当前写法）**

---

## 二、Chu 审判日期 与 民事/刑事被告区分（专项检查结果）

按任务要求特别检查两项，结论如下。

### A. Daniel Chu 的审判日期

| 项目 | 内容 | 出处 |
|---|---|---|
| 原稿表述 | "As of October 2026, his criminal trial is scheduled for January 2027." | `04:L233` ／ 中文 `04:L245` |
| `06` 核验结论 | **`CONTRADICTED`** | `06` 第 6.4 项 |
| 已取得的日期版本 | **2026-10-19（原定，B 级 Reuters）**；2027-01-25（C 级 Octus）；2027-02-01（备选，C 级 National Law Review） | `06` 第 6.4 项 |
| 延期程序 | 法官 Kevin Castel 暂时维持原日期，要求双方预留 2027-02-01 | 同上 |
| 是否已确认 | **未确认**——`06` 明示"不得写死'2027 年 1 月'"；`06` 第六节列为第 1 优先复查项 | `06` 第 6.4、六节 |
| `07` 处置 | `07:6-1` **HIGH**，`07` 汇总 P0 必改第 1 条 | `07` |

### B. SEC 民事被告 与 刑事被告的区分

| 维度 | 人员 | 依据与等级 |
|---|---|---|
| **SEC 民事被告（3 人）** | **Chu、Kollar、Seibold** | SEC 2026-77 **P5** + LR-26612：**A 级**；`06` 第 6 项"反向确认" |
| **刑事被告（4 人）** | **Chu、Goodgame、Kollar、Seibold** | DOJ/SDNY 新闻稿 **P1**（Chu、Goodgame）＋**P2**（Kollar、Seibold）：**A 级** |
| **不在民事被告之列** | **Goodgame** | `06` 第 6.3 项标 "NOT FOUND"（A 级反向确认） |
| 原稿是否已正确区分 | **部分正确**：`04:L235` 的三人名单**正确**；`04:L229` 有"不完全是同一批人"的过渡句 | `07:6-3` 可保留 |
| 原稿是否仍可能致误 | **是**：`04:L231` 与 `04:L235` 两份名单并列，未点明 Goodgame 不在民事被告中 | `07:6-5` **MEDIUM**，`07` 汇总 **P1** |

---

## 三、本任务边界确认

- **未修改任何现有文件**：三个目标文件 SHA256 与前一日记录完全一致（`04`＝`40D1E0EDB4812014`、`06`＝`1D8632E7578D7D5D`、`07`＝`0EFFD015147A24B7`）；未触碰 `01`、`02`、`03`、`05`、`08`、`_incoming/`、`_SOURCE_SCRIPT_SEARCH_LOG.md`。
- **未新增项目文件**（提取阶段）：本提取结果在提取阶段直接输出于对话；**用户随后明确要求本地存储，故生成本文件 `09_TRICOLOR_REVISION_01_EXTRACT.md`**，内容与原对话输出一致。
- **未补造**：凡现有材料未支持者（Chu 的最终审判日期、破产法院名称、量刑结果、9.45 亿精确值、起诉书原文）一律标「未确认」或引用 `06` 的 `UNVERIFIED`／`C 级`／`PENDING_PRIMARY_SOURCE`，未作推断。
- **未把检索索引摘要冒充完整原始文件**：`06` 的 A 级引句已如实标注为"经检索通道取回的原件被索引片段"，且 `06` 附录 A.3 记录了 7 条原件不可访问的尝试；本提取沿用该标注，未升级任何证据等级。
- **未开展新一轮网络调查**：本提取全部内容来自 `04`、`06`、`07` 三个已存在文件。
- **未复述整个项目**：仅覆盖上述 7 个问题及其核验与风险记录。

**提请注意**：旁白修订须**新建 `04_TRICOLOR_SCRIPT_V2.md`**，不得静默覆盖 V1（`04:L317` 版本规则）；本任务未执行该修订，也未就修订方案作任何决定。

---

## 四、下一步（本文件的使用方式）

本文件是"最小修订提案"的**输入材料**，不是提案。若要形成提案，尚需：

1. **P0 两项**（`07:6-1` Chu 审判日期、`07:4-1` 22/14/8 亿归属）可直接依本文件的建议表述起草；
2. **P1 两项**（`07:5-1` 9.45 亿文书定位、`07:6-5` 增补 Goodgame 未列民事被告一句）可直接起草；
3. **P2 两项**（`07:1-1` 补全日期、`07:1-2` 中文"破产清算"）可直接起草；
4. **`07:4-2`（可选微调）** 与 **`07:6-2`（字幕层补精确日期）** 需人工决定是否纳入最小改动范围；
5. 其余 16 条**可保留**，提案不宜改动——尤其 `04:L161`、`04:L163`、`04:L201`、`04:L237` 与 `04:L235` 的三人名单。

**仍未解决、可能影响提案的一手证据缺口**（来自 `06` 第五节、`07` 第五节）：

| # | 缺口 | 影响 |
|---|---|---|
| 1 | Chu 案件最新排期 | 决定 `07:6-1` 能否收口为确定表述 |
| 2 | 刑事起诉书原文 | 决定 `07:4-1` 能否恢复 `indictment alleged` |
| 3 | SEC 起诉状原文 | 决定 `07:5-1` 的文书定位 |
| 4 | SEC 2026-77 与 DOJ/SDNY 新闻稿页面本体 | 全稿 A 级引句复核 |
| 5 | 2026-08-21 之后的案件进展 | 影响第 6 章全部法律状态表述 |

---

**文件结束。**

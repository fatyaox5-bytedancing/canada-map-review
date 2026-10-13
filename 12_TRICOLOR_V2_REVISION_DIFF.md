# 12 · TRICOLOR V2 修订差异（待确认稿）

> **文件性质**：**待确认的修订差异清单**（六项授权修改的逐条 diff）。属审查过程材料，**不是**正式修改差异报告，**不是** V2 稿件。
> **状态**：`AWAITING_APPROVAL` —— 等待人工确认后方可据此生成 V2 与正式报告。
> **生成日期**：2026-10-13（周二，UTC+8）10:42
> **任务编号**：TRICOLOR-REVISION-01（V2 生成阶段）
> **依据文件**：[`04_TRICOLOR_SCRIPT_V1.md`](04_TRICOLOR_SCRIPT_V1.md) ｜ [`06_TRICOLOR_FACT_CHECK_BATCH_1.md`](06_TRICOLOR_FACT_CHECK_BATCH_1.md) ｜ [`07_TRICOLOR_SCRIPT_RISK_REVIEW.md`](07_TRICOLOR_SCRIPT_RISK_REVIEW.md) ｜ [`09_TRICOLOR_REVISION_01_EXTRACT.md`](09_TRICOLOR_REVISION_01_EXTRACT.md)
> **本轮执行范围**：**只读**。未创建 V2，未创建正式报告，未修改任何现有文件。
> **常驻约束**：本工作区基本配置见 [`../../_dsh-watch/RUN-CONFIG.md`](../../_dsh-watch/RUN-CONFIG.md)（模型访问频率 ≤ 1,000,000 TPM）。

---

## 〇、命名决议与文件编号

任务书原指定输出为 `08_TRICOLOR_SCRIPT_V2.md`、`09_TRICOLOR_V2_CHANGELOG.md`、`10_TRICOLOR_PREPUBLICATION_CHECK.md`。核对后发现两处冲突：

| 任务书指定名 | 冲突情况 |
| --- | --- |
| `08_TRICOLOR_SCRIPT_V2.md` | 空闲，但 `08_` 编号已被 [`08_WORK_LOG.md`](08_WORK_LOG.md) 占用；且 README 第 67 行与 V1 归档说明第 3 条均**强制**规定 V2 应命名为 `04_TRICOLOR_SCRIPT_V2.md` |
| `09_TRICOLOR_V2_CHANGELOG.md` | 空闲，但 `09_` 编号已被 [`09_TRICOLOR_REVISION_01_EXTRACT.md`](09_TRICOLOR_REVISION_01_EXTRACT.md) 占用 |

**用户裁定结果**：

| 用途 | 最终文件名 |
| --- | --- |
| 正式修订稿（V2） | `04_TRICOLOR_SCRIPT_V2.md`（遵循项目强制规则，与 V1 构成版本对） |
| 修改差异报告 | `10_TRICOLOR_V2_CHANGELOG.md` |
| 发布前风险清单 | `11_TRICOLOR_PREPUBLICATION_CHECK.md` |
| 本文件（待确认稿） | `12_TRICOLOR_V2_REVISION_DIFF.md`（新增，用于承载本轮 diff，不与上述三个文件争号） |

**用户同时裁定**：本轮**先在对话中输出六项 diff，确认后再落盘**三个文件。理由是脚本涉及金融数字、刑事指控与 SEC 民事诉讼，且 RUN-CONFIG **C-2.7** 要求改动生产文件前先给 diff —— 不因"新建而非覆盖"而绕过。

---

## 一、核对基准（当前版本）

| 文件 | 行数 | SHA256（前16） |
| --- | --- | --- |
| `04_TRICOLOR_SCRIPT_V1.md` | 321 | `40D1E0EDB4812014` |
| `06_TRICOLOR_FACT_CHECK_BATCH_1.md` | 486 | `1D8632E7578D7D5D` |
| `07_TRICOLOR_SCRIPT_RISK_REVIEW.md` | 489 | `0EFFD015147A24B7` |
| `09_TRICOLOR_REVISION_01_EXTRACT.md` | — | `5BC5B1750D6A087D` |

**读取完整性**：`04` 已全文读过（第 1–321 行）；`06`、`07` 在本轮开始前内容有变（我方上次编辑后行数由 395／457 变为 486／489），已重新读取相关部分并以上表哈希为准；`09` 自创建后未变。

**一处与任务书描述不符的实情（如实报告，未自行更改路径）**：修改 2 的任务书表述为"第一章或相关章节"，该句实际位于 **第 4 章（04:20–05:55）第 159 行**，不在第一章。本文件按实际位置处理。

---

## 二、修改 1 ｜ 第一章破产日期及 Chapter 7 中文表述

**位置**：Chapter 1 — The Business Behind the Collapse ／ 00:00–01:30 ／ 英文 `04:L47`（段首句）、中文 `04:L61`（段首句）

### 英文

| | 内容 |
| --- | --- |
| V1 原文 | `Tricolor filed for Chapter 7 bankruptcy in September 2025.` |
| V2 修改稿 | `Tricolor filed for Chapter 7 bankruptcy on September 10, 2025.` |

### 中文

| | 内容 |
| --- | --- |
| V1 原文 | `2025 年 9 月，Tricolor 申请了美国《破产法》第七章破产保护。` |
| V2 修改稿 | `2025 年 9 月 10 日，Tricolor 申请了美国《破产法》第七章破产清算。` |

**修改理由**：① 日期精度——V1 第 5 章 `04:L197` 已写全日期，第 1 章省略造成全篇内部不一致（`07:1-1` LOW）；② Chapter 7 是**清算**程序，"破产保护"承载的是 Chapter 11 重整语义（`06` 第 2 项 A 级引句 + ABA Business Law Today "chapter 7 petition will result in a liquidation"；`07:1-2` LOW）。

**边界**：不改 Chapter 7 为 Chapter 11；不写法院已批准、已开始资产分配或清算完成；不补破产法院名称（`06`：无任何来源给出）。

---

## 三、修改 2 ｜ 22 亿／14 亿／8 亿美元的指控归属

**位置**：Chapter 4 — What Investigators Allege Happened ／ 04:20–05:55 ／ 英文 `04:L159`、中文 `04:L175`

### 英文

| | 内容 |
| --- | --- |
| V1 原文 | `A separate criminal indictment alleged that, by August 2025, Tricolor had pledged about $2.2 billion in collateral to lenders and investors while holding only about $1.4 billion in actual collateral—a gap of roughly $800 million.` |
| V2 修改稿 | `Federal prosecutors alleged that, by August 2025, Tricolor had pledged about $2.2 billion in collateral to lenders and investors while holding only about $1.4 billion in actual collateral—a gap of roughly $800 million.` |

### 中文

| | 内容 |
| --- | --- |
| V1 原文 | `另一份刑事起诉书则指控，截至 2025 年 8 月，Tricolor 向贷款机构和投资者质押的抵押品价值约为 22 亿美元，但实际拥有的抵押品只有约 14 亿美元，两者之间存在大约 8 亿美元的缺口。` |
| V2 修改稿 | `联邦检察官指控称，截至 2025 年 8 月，Tricolor 向贷款机构和投资者质押了约 22 亿美元的抵押品，但实际持有的抵押品仅约 14 亿美元，两者相差约 8 亿美元。` |

**修改理由**：归属层级过高。`06` 第 4 项记录：DOJ/SDNY 新闻稿第 7 段位于引导句 "According to the allegations contained in the Indictment unsealed today in Manhattan federal court:" **之后**，即公告系**转述**起诉书；**起诉书正文本轮未取得**，故该字段标 `PENDING_PRIMARY_SOURCE`（`07:4-1` MEDIUM）。

**边界**：三个数字、数量级、`about`／`roughly` 近似量词、时点（by August 2025）**全部不动**；不称其为已确认损失、诈骗所得或投资者最终损失；**未**声称已取得并逐字核验完整起诉书。

---

## 四、修改 3 ｜ 19 亿美元 ABS 融资规模的英文优化

**位置**：Chapter 4 ／ 04:20–05:55 ／ 英文 `04:L155`、中文 `04:L171`

### 英文

| | 内容 |
| --- | --- |
| V1 原文 | `According to the Securities and Exchange Commission, Tricolor raised more than $1.9 billion through asset-backed securities offerings between at least 2020 and September 2025.` |
| V2 修改稿 | `According to the Securities and Exchange Commission, Tricolor raised more than $1.9 billion through asset-backed securities offerings from at least 2020 until its September 2025 bankruptcy.` |

### 中文

| | 内容 |
| --- | --- |
| V1 原文 | `根据美国证券交易委员会（SEC）的说法，至少从 2020 年到 2025 年 9 月，Tricolor 通过资产支持证券发行筹集了超过 19 亿美元。` |
| V2 修改稿 | `根据美国证券交易委员会（SEC）的说法，Tricolor 至少从 2020 年起，直至 2025 年 9 月破产期间，通过发行资产支持证券（ABS）累计筹集了超过 19 亿美元。` |

**修改理由**：V1 的 "between at least 2020" 语法生硬，且 "and September 2025" 可能被读作"截至破产时仍持有"；A 级原句语义是"**期间内累计募集**"（`07:4-2` LOW）。

**上下文口径检查（任务书要求项）**：**已明确，无需添加**。`04:L161` 与中文 `04:L177` 已经区分融资规模与抵押品缺口，并否定"等于最终损失"。按任务书要求**不重复添加解释段落**。

**边界**：保留 `more than $1.9 billion`；不补发行次数、最早发行年份、交易清单；不写成诈骗金额、投资者最终损失或破产时未偿本金；`PARTIALLY_VERIFIED` **不升级**。

---

## 五、修改 4 ｜ 9.45 亿美元未偿本金的日期与语义精确化

**位置**：Chapter 5 — When Funding Dries Up ／ 05:55–07:00 ／ 英文 `04:L199`、中文 `04:L213`

### 英文

| | 内容 |
| --- | --- |
| V1 原文 | `In an SEC filing announced in August 2026, the agency said that more than $945 million in principal associated with Tricolor's asset-backed securities offerings remained outstanding and payable when the company entered bankruptcy.` |
| V2 修改稿 | `In an SEC litigation release dated August 18, 2026, the agency said that more than $945 million in principal associated with Tricolor's asset-backed securities offerings remained outstanding and payable to investors when the company entered bankruptcy.` |

### 中文

| | 内容 |
| --- | --- |
| V1 原文 | `美国证券交易委员会在 2026 年 8 月公布的一份诉讼文件中表示，Tricolor 进入破产程序时，与其资产支持证券发行相关、尚未偿还的本金超过 9.45 亿美元。` |
| V2 修改稿 | `美国证券交易委员会在 2026 年 8 月 18 日发布的诉讼公告中表示，Tricolor 进入破产程序时，与其资产支持证券发行相关、仍未偿付且应付给投资者的本金超过 9.45 亿美元。` |

**修改理由**：① "SEC filing" 定位不准——A 级载体是 SEC **新闻稿 2026-77** 与 **Litigation Release 26612**（均 2026-08-18），数字本身出自 **SEC 起诉状（complaint）**，新闻稿系转述；② 日期精度不足（A 级为 2026-08-18）；③ 补 `to investors` 复现 A 级原句的适用范围（`07:5-1` MEDIUM）。

**边界**：保留 `more than $945 million`，**不得**改为 `$945.4 million`；不写 `seven offerings`；不写成已确认投资者损失；不与贷款人债权（9 亿多／9.23 亿）或重复质押本金（3.655 亿）混用。

### 5.1 任务书第 4 条要求核查项：保护性表述**已经存在**，不需要新增

| 语言 | 位置 | 原文 | 结论 |
| --- | --- | --- | --- |
| 英文 | `04:L201` | `That is an outstanding principal figure, not a confirmed estimate of investor losses. The amount ultimately recovered depends on the assets available, the rights of different creditors, and the outcome of the bankruptcy process.` | **已存在**，与任务书要求逐字一致 |
| 中文 | `04:L215` | `这是一个未偿本金的数字，并不是对投资者损失的确认估计。最终能够收回多少，取决于可用资产、不同债权人的权利，以及破产程序的结果。` | **已存在**，含义与英文一致 |

**结论**：按任务书指令，**不增加整段新内容**。建议该句在 V2 中**一字不动**（`07:5-2` LOW：可保留）。

**待确认项**：若需把中文措辞改得更硬（如"并不是对投资者损失的确认估计"→"并非已确认的投资者损失"），属**新增授权**，本轮未自行改动，已列入第六节决策点。

---

## 六、修改 5 ｜ 删除 Daniel Chu 刑事审判的未确认日期

**位置**：Chapter 6 — The Legal Cases ／ 07:00–08:00 ／ 英文 `04:L233`、中文 `04:L245`

### 英文

| | 内容 |
| --- | --- |
| V1 原文 | `Former CEO Daniel Chu has pleaded not guilty to the criminal charges. As of October 2026, his criminal trial is scheduled for January 2027.` |
| V2 修改稿 | `Former CEO Daniel Chu has pleaded not guilty to the criminal charges.` |

### 中文

| | 内容 |
| --- | --- |
| V1 原文 | `前首席执行官 Daniel Chu 对刑事指控表示不认罪。截至 2026 年 10 月，他的刑事审判定于 2027 年 1 月进行。` |
| V2 修改稿 | `前首席执行官 Daniel Chu 对刑事指控表示不认罪。` |

**修改理由**：`06` 第 6.4 项结论为 **`CONTRADICTED`** —— 三个日期并存（原定 2026-10-19，B 级；2027-01-25，C 级；备选 2027-02-01，C 级），`06` 明示"**不得写死'2027 年 1 月'**"；`07:6-1` 为**全稿唯一 HIGH**。

**与任务书建议存在一处差异（需人工确认）**：任务书指定**只保留前半句（纯删除）**；而 `07:6-1` 曾建议补写"原定 2026 年 10 月、已延期、2027 年初"。两者不同：

- 任务书版本（**纯删除**）最保守，符合"不自行添加'审判已经延期'等新事实"的要求 → **默认按任务书版本执行**；
- 若希望保留"案件仍在推进"的信息量，需明确授权采用 `07` 的表述（会引入 `adjourned` 这一新事实，其依据为 C 级单一来源）。

**边界**：不用其他未核实日期替代；不改"不认罪"为"无罪"或"已被法院判定无罪"；不改写本章法律背景。

### 6.1 其他章节同类旧表述的扫描结果（仅报告，未修改）

| 检索项 | V1 中的出现 | 处理 |
| --- | --- | --- |
| `January 2027` | **仅** `04:L233`（英文） | 本项修改覆盖 |
| `October 2026` | **仅** `04:L233`（英文） | 本项修改覆盖 |
| 中文"2027 年 1 月" | `04:L245` | 同步删除 |
| 同一日期是否出现在 [`05_TRICOLOR_STORYBOARD_V1.md`](05_TRICOLOR_STORYBOARD_V1.md) | **未出现**（该表 13 镜头的旁白与时间码字段仍为"待补充"，状态 `PENDING_ALIGNMENT`） | 无需处理 |
| 分镜表是否含法律状态表述 | 仅第 51 行备注"**重复质押须保持'指控'口径**" | 与本轮六项无冲突，无需修改 |

---

## 七、修改 6 ｜ 明确 Goodgame 不在 SEC 民事诉讼被告名单中

**位置**：Chapter 6 ／ 07:00–08:00 ／ 英文 **在 `04:L235` 之后新增**、中文 **在 `04:L247` 之后新增**

### 英文

| | 内容 |
| --- | --- |
| V1 原文 | （无此句） |
| V2 新增 | `Goodgame was not named in the SEC's civil suit.` |

### 中文

| | 内容 |
| --- | --- |
| V1 原文 | （无此句） |
| V2 新增 | `Goodgame 并未被列为 SEC 这起民事诉讼的被告。` |

**修改理由**：`04:L231` 先并列"Kollar、Seibold、Goodgame 三人均认罪"，`04:L235` 紧接着只列三名 SEC 民事被告（Chu、Kollar、Seibold）—— 两份名单并列时观众极易推断 Goodgame 也在民事被告中。`06` 第 6.3 项以 A 级**反向确认**"Goodgame 未被列入 SEC 民事被告"（`07:6-5` MEDIUM）。

**上下文确认（任务书要求"仅在确实容易混淆时添加"）**：**成立**。`04:L229` 的过渡句为：

> `The criminal case and the civil case are not the same thing. They are related, but they are not the same case, and they do not involve exactly the same people.`
> 中文 `04:L241`：`这起倒闭事件已经引发刑事诉讼，以及 SEC 另行提起的民事诉讼。两者相互关联，但并不是同一个案件，而且每名被告的法律状态也有所不同。`

该句只说"不完全是同一批人"，**未点名**，不足以澄清 Goodgame 的具体位置。

**边界**：不暗示 Goodgame 未涉任何刑事案件（`04:L231` 已写其 "also charged" 且已认罪，须保留）；不扩大为"未受任何监管指控"；不扩展其他被告的法律状态；**不**改动 `04:L235` 现有三人名单。

---

## 八、附加项 ｜ 修改 1 对第五章同一事件中文措辞的同步处理（单独列出）

**位置**：Chapter 5 ／ 05:55–07:00 ／ **仅中文 `04:L211`；英文 `04:L197` 保持不变**

| | 内容 |
| --- | --- |
| V1 中文原文 | `2025 年 9 月 10 日，Tricolor 申请了美国《破产法》第七章破产保护。` |
| V2 中文修改稿 | `2025 年 9 月 10 日，Tricolor 申请了美国《破产法》第七章破产清算。` |
| V1 英文（**不动**） | `Tricolor filed for Chapter 7 bankruptcy on September 10, 2025.` |

**理由**：与该章英文及修改 1 的中文口径统一（`06` 第 2 项；`07` 第 250 行明确"第 211 行中文'第七章破产保护'见 1-2 的修改建议"）。**英文一字不动**，因 `04:L197` 已含准确日期、无措辞问题。

---

## 九、未授权变化自查结果

按任务书"第五节"的十项禁止清单与"第六节 A"的要求逐一比对，**确认本轮拟改动共 13 处文本片段**（清点口径：一句内多词改动算一处）：

| # | 位置 | 类型 | 归属 |
| --- | --- | --- | --- |
| 1 | `04:L47` 英文 | 改写（补日期） | 修改 1 |
| 2 | `04:L61` 中文 | 改写（补日期＋清算） | 修改 1 |
| 3 | `04:L155` 英文 | 改写（期间表述） | 修改 3 |
| 4 | `04:L159` 英文 | 改写（归属） | 修改 2 |
| 5 | `04:L171` 中文 | 改写（期间表述） | 修改 3 |
| 6 | `04:L175` 中文 | 改写（归属） | 修改 2 |
| 7 | `04:L199` 英文 | 改写（文书＋日期＋适用范围） | 修改 4 |
| 8 | `04:L211` 中文 | 改写（清算） | 附加项（修改 1 的 Ch5 同步） |
| 9 | `04:L213` 中文 | 改写（文书＋日期＋适用范围） | 修改 4 |
| 10 | `04:L233` 英文 | 删除第二句 | 修改 5 |
| 11 | `04:L235` 后 英文 | 新增一句 | 修改 6 |
| 12 | `04:L245` 中文 | 删除第二句 | 修改 5 |
| 13 | `04:L247` 后 中文 | 新增一句 | 修改 6 |

**除此之外，V1 其余全部内容拟一字不动**，包括：

- 八章结构、章节顺序、章节标题、时间码；
- 四处口径保护句：`04:L161`、`04:L163`、`04:L201`、`04:L237`（及对应中文 `L177`、`L179`、`L215`、`L249`）；
- `04:L235` 的三人名单 `Chu, Kollar, and Seibold`（`07` 标注为"全稿最容易顺手改错的一句"）；
- 归档元信息与归档说明（`04:L1–25`、`04:L313–321`）。

**未发现未授权改动**。本轮亦**未修改** `05`（分镜）、视频标题、缩略图文案、画面素材或时间码。

---

## 十、需人工确认的 4 个决策点

| # | 决策点 | 默认方案 | 备选 |
| --- | --- | --- | --- |
| 1 | 修改 5 的删法 | **纯删除**（按任务书） | 采用 `07:6-1` 的"原定 2026 年 10 月、已延期、2027 年初"（需明确授权） |
| 2 | 修改 4 中文"仍未偿付且应付给投资者的本金" | **接受**（对应英文 `payable to investors`） | 保持 V1"尚未偿还的本金" |
| 3 | `04:L61` 是否补日期 | **补为 2025 年 9 月 10 日**（与英文 `on September 10, 2025` 对齐） | 仅改"清算"不补日期 |
| 4 | 文件命名 | **`04_TRICOLOR_SCRIPT_V2.md`、`10_TRICOLOR_V2_CHANGELOG.md`、`11_TRICOLOR_PREPUBLICATION_CHECK.md`** | —（已由用户裁定） |

---

## 十一、本轮执行状态

| 项 | 结果 |
| --- | --- |
| 新建文件 | **仅本文件**（`12_TRICOLOR_V2_REVISION_DIFF.md`）；未生成 V2，未生成两个正式报告 |
| 修改现有文件 | **无**。`04`、`06`、`07`、`09` 哈希与本轮开始时一致；`01`、`02`、`03`、`05`、`08` 未触碰 |
| 模型请求 | 本会话本轮 **1 次**（会话自身）+ 若干只读文件工具调用 |
| 服务端检索请求 | **0 次**——未发起任何 `web_search` 或检索脚本调用 |
| RUN-CONFIG C-1 阈值 | **未触及**（离 1,000,000 TPM 极远） |
| RUN-CONFIG C-2.7 遵循 | **是**——先给 diff、待确认后再落盘 |

---

## 十二、确认后的下一步

人工确认（或指出需调整条目）后，一次性生成三个文件：

1. `04_TRICOLOR_SCRIPT_V2.md` —— 以 V1 为底稿，仅应用本文档第二节至第八节的 13 处改动；
2. `10_TRICOLOR_V2_CHANGELOG.md` —— 逐项记录修改编号、章节与定位、V1/V2 原文、修改原因、对应 06/07 依据、双语是否同步、未解决证据限制，并说明哪些法律与金融口径被明确保留；
3. `11_TRICOLOR_PREPUBLICATION_CHECK.md` —— 按 `PASS`／`NEEDS SOURCE CHECK`／`BLOCKER` 分类，逐项注明问题、当前证据状态、建议动作与责任边界。

随后执行任务书第六节 A–E 五项质量检查（文本差异／双语一致性／关键词全文检索／章节与篇幅／证据与风险分级），并在终端报告：三个文件路径、六项修改的 PASS／PARTIAL／BLOCKED 判定、V1 与 V2 英文词数及差值、是否存在未授权改动、双语一致性结果、发布前仍需核实的原始来源、是否存在 `BLOCKER`、下一步建议。

---

**文件结束。**

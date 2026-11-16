# 美国对全球AI产业链控制力分析——第三轮补充审计与勘误

**研究截止时间**：2026 年 11 月 16 日
**审计性质**：小范围补充审计。只处理三个具体问题，不扩展研究范围，不修改六节点框架。
**审计对象**：
1. 《美国对全球AI产业链六个关键节点的控制力分析》
2. 《美国对全球AI产业链控制力分析——四项关键论据原始来源审计》

**本次核查使用的原始文件**（全部为法规原文或公司正式披露，媒体报道仅作旁证）：

| 编号 | 文件 | 发布机构 | 日期 | 链接 |
|---|---|---|---|---|
| R1 | *Foreign-Produced Direct Product Rule Additions, and Refinements to Controls for Advanced Computing and Semiconductor Manufacturing Items*（89 FR 96790，FR Doc 2024-28270） | BIS | 2024-12-05 | https://www.govinfo.gov/content/pkg/FR-2024-12-05/html/2024-28270.htm |
| R2 | *Implementation of Additional Due Diligence Measures for Advanced Computing Integrated Circuits*（90 FR 5298，FR Doc 2025-00711） | BIS | 2025-01-16 | https://www.govinfo.gov/content/pkg/FR-2025-01-16/html/2025-00711.htm |
| R3 | FDD 规则更正案（FR Doc 2025-02655） | BIS | 2025-02-14 | https://www.federalregister.gov/documents/2025/02/14/2025-02655/implementation-of-additional-due-diligence-measures-for-advanced-computing-integrated-circuits |
| R4 | EAR §734.9(h)、§734.9(a)(3)（eCFR 现行文本，2026-11-12 刊期） | eCFR | 2026-11-12 | https://www.ecfr.gov/current/title-15/section-734.9 |
| R5 | EAR §742.6(a)(6)(i)(B)、(b)(10)(ii)、(b)(10)(iii)（现行） | eCFR | 2026-11-12 | https://www.ecfr.gov/current/title-15/section-742.6 |
| R6 | EAR §740.25（License Exception HBM）、§740.28（License Exception ACM）（现行） | eCFR | 2026-11-12 | https://www.ecfr.gov/current/title-15/section-740.25 、…/section-740.28 |
| R7 | EAR §744.23(a)(3)(i)(B)（现行） | eCFR | 2026-11-12 | https://www.ecfr.gov/current/title-15/section-744.23 |
| R8 | CCL ECCN 3A090 现行条目（含 Note 1、Technical Note 1） | eCFR（15 CFR Part 774 Supp. 1） | 2026-11-12 | https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-774 |
| R9 | EAR §772.1 定义（"applicable advanced logic integrated circuits"、"front-end fabricator"、"OSAT"、"direct product"） | eCFR | 2026-11-12 | https://www.ecfr.gov/current/title-15/section-772.1 |
| R10 | Synopsys Form 8-K（2025-07-02 事件、2025-07-03 提交） | SEC | 2025-07-03 | https://d18rn0p25nwr6d.cloudfront.net/CIK-0000883241/ae517864-0ecf-445d-9e2d-fdecbb77fcf6.pdf |
| R11 | Synopsys 官方声明 | Synopsys IR | 2025-07-02 | https://news.synopsys.com/2025-07-02-Synopsys-Issues-Statement-in-Connection-to-the-Lifting-of-Recent-U-S-Export-Restrictions-Related-to-China |
| R12 | 西门子对中国媒体正式回应（Global Times 转述，西门子中国声明） | Siemens | 2025-07-03 | https://www.globaltimes.cn/page/202507/1337536.shtml |
| R13 | Mentor Graphics 2017 财年 Q4 财报新闻稿（载明西门子收购协议、Wilsonville 总部） | Mentor Graphics | 2017-03-02 | http://s3.mentor.com/public_documents/misc/company/investor_relations/news/2017_q4_fy/Q4FY2017-earnings.pdf |
| R14 | Mentor Graphics 企业沿革（收购完成时间、2021 年更名、研发地点分布） | Wikipedia/Wikiwand（C 级，仅作沿革旁证） | 2025 年版本 | https://wikiwand.com/en/Mentor_Graphics |

**本次仍无法取得的原始证据**（必须在写作中如实标注）：
- 2025 年 5 月 BIS 致三家 EDA 企业的通知函原文——从未公开，只能以企业 8-K 与官方声明还原；
- 韩国三星、SK 海力士任一具体 HBM 产品是否符合 §734.9(h) FDPR"直接产品"条件的判定——依赖逐产品、逐设备的技术事实，无公开裁定；
- 各 EDA 具体产品的官方商品分类裁定（commodity classification）——不公开。

---

## 1. 三项问题审计总览

| 问题 | 前两轮报告的判断 | 本次核查结果 | 是否需要修正 |
|---|---|---|---|
| 一：HBM 的许可证触发条件与审查政策 | "许可要求只覆盖澳门／D:5 目的地与总部在该地的买方；审查政策是推定批准（除非买方总部在 D:5）" | 方向正确，但**三层结构没有分开**（是否受 EAR 管辖 → 是否触发许可 → 适用什么审查政策），且**遗漏了第二个许可触发器**（§744.23(a)(3)(i)(B) 知情条款，目的地不限），FDPR 两条路径的条件也有一处错误（只有第二条要求"美国原产"） | **需要修正＋补充** |
| 二：3A090.a Note 1 三种推翻推定路径 | 列出了三条路径，但把"300 亿晶体管"与"不含 HBM"写成同一组并列条件；未说明推定只约束前端厂与 OSAT；未说明许可例外 ACM 对合法芯片流量的疏导作用 | 三条路径的**主体、证明要求各不相同**，300 亿／350 亿／400 亿门槛的适用方式需按原文拆开 | **需要修正＋补充** |
| 三：西门子 EDA 的原产地与 EAR 管辖 | "西门子 EDA 是美国实体、德国股权、美国原产软件；EAR 管辖附着于软件原产地" | **"所有产品都是美国原产"是过度概括**：旗舰产品在美国开发有据，但 Mentor 的研发点分布全球十余国，逐项产品的原产地无公开数据；2025 年 5 月函件对西门子的证据链已由"媒体报道"升级为"公司自证"（西门子确认收到 5 月 23 日函，涉 3D991/3E991，7 月初撤销） | **需要降级表述＋证据升级** |

一句话结论：前两轮报告的三个方向性判断（HBM 管的是"谁买"、封装规则是"签证窗口"、EDA 管辖附着于软件原产地）**都成立**；本次修正集中在**法律概念的分层**——把"受管辖""需要许可""推定拒绝"这三个不同的东西严格分开后，美国的控制力描述反而更有力，因为每一层都有明确的法规原文支撑。

---

## 2. HBM 补充审计：严格区分"管辖—触发—审查"三层

### 2.1 为什么必须分三层

前两轮报告把三件事压成了一句话："美国通过 FDPR 管住了外国产的 HBM"。这句话在法律上混了三个不同的问题：

1. **管辖层**：这批 HBM 是否"受 EAR 管辖"（subject to the EAR）？——由 §734.9(h) FDPR 或其他管辖规则决定。
2. **触发层**：受管辖的交易是否"需要许可证"？——由 §742.6（目的地管制）＋ §744.23（最终用途管制）＋实体清单决定。
3. **审查层**：递交许可申请后按什么政策审查？——由 §742.6(b)(10)(ii) 决定。

EAR 原文明确说这三层不是一回事（§734.9 段首注，R4）：

> "If a foreign-produced item is subject to the EAR, then you should separately determine the license requirements that apply to that foreign-produced item (e.g., by assessing the item classification, destination, end-use, and end-user in the relevant transaction). **Not all transactions involving foreign-produced items that are subject to the EAR require a license.**"

——即：**受管辖 ≠ 需要许可；需要许可 ≠ 许可会被拒绝。** 任何把这三层压扁的写法都会被专业读者挑出来。

### 2.2 第一层：韩国产的 HBM 何时受 EAR 管辖（FDPR 独立判断）

**产品范围**：3A090.c 管的是"带宽密度 > 2 GB/s/mm²"的 HBM（R8；BIS 在 89 FR 96790 中明确"All HBM stacks currently in production exceed this threshold"）。三星与 SK 海力士的现行产品全部落入此范围。

**FDPR 条件**（§734.9(h) 现行全文，R4）：外国产物项同时满足"产品范围"和"目的地范围"才受管辖。产品范围有**两条路径，条件不同**：

**路径 (h)(1)(i)——"技术／软件的直接产品"**：

> "(A) The foreign-produced item is the 'direct product' of 'technology' or 'software' **subject to the EAR** and specified in 3D001, 3D901, 3D991, 3D992, 3D993, 3D994, 3E001, 3E002, 3E003, 3E901, 3E991, 3E992, 3E993, 3E994, … of the CCL; and (B) The foreign-produced item is: (1) Specified in ECCN 3A090…"

注意两个精确点：
- 该路径的"技术／软件"只要求**受 EAR 管辖**，**不要求美国原产**（美国原产是另一条路径的要求）。前两轮报告写"必须是清单内**美国原产**技术／软件的直接产品"，对这一条路径是**不准确的**；
- 2024 年 12 月的 FDP IFR（R1 第 10 节）把 3D901、3D992、3D993、3D994、3E901、3E992、3E993、3E994 追加进了 (h) 规则的技术／软件清单——即与半导体制造设备相关的软件与技术也被纳入了"上游锚点"。

**路径 (h)(1)(ii)——"整厂或设备主要部件的直接产品"**：

> "(A) The foreign-produced item is produced by any complete plant or 'major component' of a plant that is located outside the United States, when the plant or 'major component' of a plant, whether made in the United States or a foreign country, itself is a 'direct product' of **U.S.-origin** 'technology' or 'software' that is specified in [同一清单]…"

只有这条路径才要求上游技术／软件**美国原产**。对韩国 HBM 工厂而言，更现实的入口是这条：工厂设备（如美国设备商的工具，或以美国技术为核心部件的外国设备）若是美国原产受控技术的直接产品，则该厂产的 3A090.c 物项落入产品范围。

**"直接产品"的定义**（§772.1，R9）：

> "Direct product. The immediate product (including processes and services) produced directly by the use of technology or software."

**目的地范围**（§734.9(h)(2)）：只要"知晓"该物项"destined to any location worldwide"，目的地范围即满足——这一条几乎总是满足。另有 (h)(2)(ii) 针对"总部在澳门／D:5 的实体开发的技术用于生产掩模或晶圆"的情形。

**FDPR 独立判断结论**：
- 具体产品（3A090.c）属于规则范围——**成立**；
- 是否满足"美国技术／软件关联"——**必须逐产品、逐设备核实**，不能仅因韩国工厂使用美国设备、软件就认定其全部 HBM 受管辖。BIS 序言的原文也是条件句（R1）："foreign-produced 3A090.c items **will be subject to the EAR if they meet the scope of that FDP rule**"；
- 是否存在例外——FDPR 本身对 3A090.c 无目的地豁免；受管辖后的许可例外见 2.4。

### 2.3 第二层：许可证何时被触发（两个触发器，不是一个）

**触发器一：目的地管制（§742.6(a)(6)(i)(B)，R5）**：

> "(B) High Bandwidth Memory (HBM). A license is required for items specified in ECCNs 3A090.c, 3D001 (for 3A090.c), and 3E001 (for 3A090.c) when exported, reexported, or transferred (in-country) **to or within Macau or a destination specified in Country Group D:5**… The license requirements in this paragraph (a)(6)(i)(B) do not apply to deemed exports or deemed reexports."

中国属于 Country Group D:5，因此**向中国出口 HBM 需要许可证**——前提是这批 HBM 已受 EAR 管辖（第一层）。对照 CCL 现行许可要求表（R8）：3A090.a 是"any destination worldwide"（全球管制），3A090.c 只对澳门／D:5（目的地管制）。

**触发器二：知情型最终用途管制（§744.23(a)(3)(i)(B)，R7）——前两轮报告遗漏**：

> "(B) Any item subject to the EAR and specified in ECCN 3A090.c **destined to any destination other than Macau or those specified in Country Group D:5, for an entity that is headquartered in, or whose ultimate parent company is headquartered in, either Macau or a destination specified in Country Group D:5**."

即：如果出口商**知晓**这批 HBM 将流向一个"总部或最终母公司总部在澳门／D:5"的实体，那么**无论货物发往哪个目的地**（例如发到东南亚的封装厂），都需要许可证。这一条把"总部测试"从审查层提到了触发层，是 HBM 管制真正的"穿透"机制。

### 2.4 第三层：许可审查政策（§742.6(b)(10)(ii)，R5）

> "There is a **presumption of approval** review policy for license applications for items specified in paragraph (a)(6)(i)(B) to or within Macau or a destination specified in Country Group D:5 … **for entities neither headquartered in nor whose ultimate parent company is headquartered in either Macau or a destination specified in Country Group D:5**. There is a **presumption of denial policy for all other license applications**."

精确读法：**推定批准只适用于"递交给澳门／D:5 的申请"，且申请人不是澳门／D:5 总部实体**；其余申请（买方或其最终母公司总部在中国等 D:5 地）一律推定拒绝。注意表述中的"or"——**买方总部**和**最终母公司总部**是两个独立测试，任一命中即落入推定拒绝。

### 2.5 许可例外的精确条件（§740.25 License Exception HBM，R6）

现行全文条件比前两轮报告的"低于 3.3 GB/s/mm²"丰富得多：

| 条件 | 原文要点 |
|---|---|
| 密度门槛 | 3A090.c 物项"memory bandwidth density **less than 3.3 GB/s/mm²**" |
| 出口方资格 | 出口方总部须在美国或 Country Group A:5，且最终母公司不得在澳门／D:5 |
| 买方资格 | 直接向"共同封装商品的设计者"出售（不得经分销商） |
| 物流 | 直接发往封装现场，不得转运 |
| 封装厂资格 | 封装厂须为美国／A:5／A:6 总部，且最终母公司不得在澳门／D:5 |
| 事后义务 | 封装厂须书面确认封装去向（该确认属"出口管制文件"，受 762 部分记录保存约束）；封装成品不得超过 3A090 技术门槛（除非适用临时通用许可） |

现行 HBM3/HBM3E/HBM4 的带宽密度远超 3.3（行业估算，C 级），因此该例外对先进 HBM 实际无效——此判断维持。

### 2.6 韩国 HBM 的触发情形表（本次重点核查）

以三星、SK 海力士在韩国生产的 HBM 为对象（两家 HBM 前段与堆叠产能主要在韩国，部分中国封装业务不涉及先进堆栈——C 级）：

| 情形 | 是否需要美国许可 | 审查政策 | 结论 |
|---|---|---|---|
| A. 韩国产 HBM（受管辖）→ 中国买方 | **需要**（触发器一：目的地 D:5） | 买方或其最终母公司总部在中国 → **推定拒绝** | **有效封锁**——这是规则设计的主靶（89 FR 96790 序言明确写"to prevent the PRC… from producing advanced computing ICs incorporating HBM"） |
| B. 韩国产 HBM（受管辖）→ 台湾地区／东南亚封装厂，用于美系客户 GPU | 不需要（非澳门／D:5 目的地；除非触发器二的"知晓"情形或买方列名） | — | 美系 AI 芯片供应链照常运转 |
| C. 韩国产 HBM（受管辖）→ 澳门／D:5 以外的目的地，但出口商知晓最终流向 D:5 总部实体 | **需要**（触发器二） | 推定拒绝 | 封锁"换道出海" |
| D. 韩国产 HBM **不受 EAR 管辖**（FDPR 产品范围未满足） | **不需要**（EAR 无管辖） | — | 美国许可制度够不着——尽管实体清单等其他工具仍可能约束特定交易 |
| E. 低于 3.3 GB/s/mm² 的 HBM → 澳门／D:5 | 可走 License Exception HBM | — | 现行先进产品不适用；仅覆盖上一代／低端堆栈 |

**媒体旁证（B 级）**：规则生效后，路透社、韩联社报道三星与 SK 海力士的对华 HBM 销售实质停止；路透估计三星约 30% 的 HBM 销售额来自中国，SK 海力士的 HBM 当时几乎全部供美国客户。这佐证了情形 A 的执法效果，但媒体报道不能替代法规原文。

### 2.7 最终回答：美国能否有效限制韩国生产的先进 HBM 向中国出口？

**明确适用的情形**：
- 韩国产 HBM 若满足 §734.9(h) FDPR 产品范围（作为受管辖技术／软件的直接产品，或由"直接产品"性质工厂／设备产出），其对华出口需要许可证，且审查政策为推定拒绝——**机制完整、有法规原文、有执法旁证**。
- 即使货不发往中国，只要出口商知晓最终流向 D:5／澳门总部实体，同样触发许可（§744.23(a)(3)(i)(B)）。

**不适用或不能直接推导的情形**：
- 不能仅因韩国工厂使用美国设备、软件就认定其**所有** HBM 自动受 FDPR 管辖——(h)(1)(i) 要求物项本身是受管辖技术／软件的"直接产品"，（h)(1)(ii) 要求工厂／设备是美国原产受控技术的直接产品，都是逐产品的事实判断；
- FDPR 产品范围未满足的 HBM，美国许可制度管不到（此情形是否在现实中存在，无公开裁定）；
- 对非澳门／D:5 目的地、非 D:5 总部买方的交易（情形 B），美国许可制度不设卡。

**仍存在法律解释不确定性的情形**：
- "直接产品"在具体产线上的认定（哪台设备算"major component"、上游技术算不算"直接"作用），无公开裁定；
- 三星的 HBM 对华销售中是否存在不受管辖的产品线，无公开数据；
- 许可申请的实际审批结果不公开，"推定拒绝"不等于"每一件都被拒"的实证。

---

## 3. 先进封装补充审计：Note 1 的三种推翻推定路径

### 3.1 Note 1 现行法规全文（ECCN 3A090.a Note 1，R8；原文本见 R2 第 774 部分修订）

推定规则：

> "When a 'front-end fabricator' or 'OSAT' company is seeking to **export, reexport, or transfer (in-country)** an 'applicable advanced logic integrated circuit,' there is a presumption that the item is 3A090.a and designed or marketed for datacenters. If the … company cannot overcome this presumption, then it must comply with all license requirements applicable to items specified in 3A090.a. **However, this presumption does not apply to any entity other than the 'front-end fabricator' or 'OSAT' company.**"

三个关键限定，前两轮报告都没有完整交代：
1. **适用行为**：出口、再出口、境内转让——不含"提供封装服务"本身；
2. **适用对象**：只有前端晶圆厂和 OSAT 受推定约束，其他主体（如芯片设计公司）不受；
3. **适用物项**："applicable advanced logic integrated circuit"——§772.1 定义为"logic integrated circuits produced using the '16/14 nanometer node' or below, or using a non-planar transistor architecture"（16/14 纳米节点及以下，或非平面晶体管架构）。**成熟制程芯片不适用。**

三种推翻路径（原文逐条）：

**路径 a——设计者证明（主体：前端厂或 OSAT；证明人：芯片设计者）**：

> "If the designer … is an approved or authorized integrated circuit designer, then a **datasheet or other attestation of the 'total processing performance' and the 'performance density'** from the approved or authorized integrated circuit designer **indicating that the IC is not specified in 3A090.a** will overcome the presumption."

适用主体资格（现行文本，截止日已延至 2026-12-31）：
- 经批准设计者：列于 part 740 补编 6（BIS 审查后点名）；
- 经授权设计者（2026-12-31 前）：总部在台湾地区或 Country Group A:1／A:5、不在澳门／D:5 且最终母公司不在澳门／D:5，并同意按 §743.9(b) 向前端厂提供信息、由前端厂向 BIS 报告；
- 2026-12-31 之后：须提交"经批准设计者"申请，授权状态自申请提交起 180 天后失效。

**路径 b——前端厂自行封装（主体：前端厂；地点：澳门／D:5 之外）**：

> "If the integrated circuit die is packaged by the 'front-end fabricator' at a location outside of Macau or a destination specified in Country Group D:5, then the attestation of the 'front-end fabricator' that (a) the 'aggregated approximated transistor count' of the final packaged IC is **below 30 billion transistors**, or (b) the final packaged IC **does not contain high-bandwidth memory** and that the … count is below (i) **35 billion** transistors for any exports … completed in **2027**; or (ii) **40 billion** transistors for any exports … completed in **2029 or thereafter**, then this overcomes the presumption…"

**路径 c——经批准 OSAT 封装（主体：OSAT；资格：列于 part 740 补编 7）**：门槛与路径 b 完全相同（<300 亿；或不含 HBM 且 <350 亿（2027）／<400 亿（2029 年起））。

**300 亿／350 亿／400 亿三个数字的精确关系**（本次核查最重要的修正点）：
- **300 亿**：不需要看是否含 HBM——晶体管数低于 300 亿即可推翻，含 HBM 也行；
- **350 亿／400 亿**：只适用于**不含 HBM** 的芯片——两档更高的门槛是为"无 HBM 但晶体管较多"的芯片设计的阶梯；
- 法规文本字面上**没有规定 2025–2026 年和 2028 年**完成交易适用的 (b) 档门槛（原文只写了 2027 和 2029 or thereafter），这是一个文本缺陷，实务上应按 BIS 咨询意见处理——写作时不要替 BIS 补 interpretation。

**另一条边界**（R2 序言）："the presumption … does not apply to the extent an item is classified under ECCNs 4A003.z, 4A004.z, 4A005.z, or 4A090"——已按其他 ECCN 分类的物项不适用该推定；且该规则"primarily limited to circumstances in which a 'front-end fabricator' seeks to export an IC to a chip designer or 'OSAT' company"。

**技术注 1（R8）**：'approximated transistor count' = 晶体管密度 × 芯片面积（平方毫米）；前端厂／OSAT 可按工艺节点的公开密度计算，或按晶圆厂提供的数据计算。

### 3.2 推翻失败之后发生什么（许可结构与例外）

推定未被推翻 → OSAT／前端厂必须按 3A090.a 处理 → 触发现行 3A090.a 的**全球许可要求**（§742.6(a)(6)(iii)(A)，R5）与审查政策（§742.6(b)(10)(iii)，R5）：
- 出口到澳門／D:5 或 D:5 总部实体：**推定拒绝**（仅 TPP<21,000 且 DRAM 带宽 <6,500 GB/s 的低性能商品对中国／澳门最终用户可逐案审查）；
- 出口到补编 5(a) 名单目的地（含美、日、韩、台等）：**推定批准**；
- 同时存在 **License Exception ACM**（§740.28，R6）：对"经批准／经授权设计者设计的" 3A090.a 芯片，前端厂与 OSAT 的开发、生产、仓储、再出口，只要最终客户不在澳门／D:5 且收货方非 D:5 总部实体，**无需许可证**。

**这条例外解释了整个规则的实际流向**：英伟达、AMD 等"经批准／经授权设计者"的 AI 芯片，在台积电／OSAT 环节的流转由 ACM 覆盖，供应链不受影响；而**中国设计公司**的先进芯片（无批准／授权资格、晶体管数与 HBM 全部超标）无法走任何一条推翻路径，只能申请许可——而对中国目的地或中国总部买方的申请是推定拒绝。**管制的实际落点：防止外国晶圆厂和封装厂为中国设计公司代工、封装先进 AI 芯片。**

### 3.3 最终回答：美国能否通过先进芯片出口管制间接影响境外先进封装企业？

**能产生实际约束的情形**：一家 OSAT／前端厂为"中国设计 + 先进制程"的芯片做封装后出口，会先撞上 Note 1 推定；无法推翻就必须申请许可，而对中国的申请按现行政策推定拒绝——所以**"封完了也出不去"成立**，这正是 2025 年 1 月规则的设计目的。补编 7 白名单意味着 OSAT 想维持对美客户业务，就必须接受这套尽职调查。

**不能直接推导的情形**：
- 美国没有"封装服务"许可类别，Note 1 管的是**芯片的出口**，不是封装服务本身；台积电为谁封装、排多少产能，仍是商业决策；
- 推定只约束前端厂与 OSAT 的出口行为，不约束其他主体；
- 成熟制程芯片（16/14 纳米以上、平面架构）完全不适用；
- 对美系设计公司的芯片，ACM 例外使封装环节的合法流量不受影响——美国并不借 Note 1"卡"自己的客户。

**仍不确定的情形**：补编 6／7 名单的完整名单与准入标准未完全公开；"aggregated approximated transistor count"对多芯粒（chiplet）封装的计数口径以技术注为准但个案仍有解释空间。

---

## 4. EDA 补充审计：三家企业的技术所有权与 EAR 管辖范围

### 4.1 三家企业的主体事实

| 企业 | 注册地／总部 | 归属 | 技术来源 | 证据等级 |
|---|---|---|---|---|
| Synopsys（新思科技） | 特拉华州注册，总部加州 Sunnyvale | 美国上市公司 | 产品主要在美国开发 | A（SEC 文件） |
| Cadence（楷登电子） | 特拉华州注册，总部加州 San Jose | 美国上市公司 | 产品主要在美国开发 | A（SEC 文件） |
| Siemens EDA | **总部俄勒冈州 Wilsonville**（前身 Mentor Graphics，1981 年创立于该地） | 2016 年 11 月宣布收购（45 亿美元、每股 37.25 美元），**2017 年 3 月完成**；2021 年 1 月由"Mentor, a Siemens Business"更名为 Siemens EDA，隶属 Siemens Digital Industries Software | 旗舰工具（Calibre、Questa、Veloce、Tessent、Capital 等）主要在美国开发；但 Mentor 时期研发点分布美国、台湾地区、埃及、波兰、匈牙利、日本、法国、加拿大、英国、亚美尼亚、印度、俄罗斯等十余地 | 收购与总部：A（Mentor 官方新闻稿，R13）；研发地点分布：C（Wikipedia，R14，仅作沿革旁证） |

**必须修正的过度概括**：前两轮报告称西门子 EDA"产品是地地道道的美国原产软件"。准确的说法是：**总部与主要研发在美国，旗舰工具主要在美国开发**；但 Mentor 的研发布局跨国，**逐项产品的原产地判定（尤其是是否存在完全在美国境外开发的产品）需要企业内部数据，无公开来源**。EAR 对软件的管辖可以有多条附着路径：美国原产（无论位于何处都受管辖）、超过最低美国成分（de minimis）、外国直接产品规则、最终用途／最终用户规则、美国人规则（§744.6）。不能把它们压成"软件在哪开发"一条。

### 4.2 EDA 产品的出口分类

公开可查的分类锚点（均为公司披露或既有规则，非推测）：
- 主流 EDA 工具的管制层级为 **ECCN 3D991／3E991**（2025 年 5 月函件涉及的就是这一档——三家公司披露一致）；
- GAAFET 结构设计相关 EDA 为 **3D006**（2022 年 10 月新增）；
- 与 3A090 先进计算芯片相关的软件／技术为 **3D001／3E001**（对 3A090.c 也有对应许可要求，见 §742.6(a)(6)(i)(B)）；
- 部分低端版本可能为 EAR99（行业通识，无官方清单，写作时不作断言）。

**没有公开的官方分类裁定证明任一家具体产品的分类**；各公司的分类号来自其 8-K／10-Q 对函件的转述。

### 4.3 2025 年 5 月事件：证据链（本次升级后的完整版本）

| 日期 | 事件 | 证据等级 |
|---|---|---|
| 2025-05-23 | BIS 函件送达 **Cadence**（Cadence 8-K 载明）与 **Siemens**（西门子官方声明载明"5 月 23 日致函西门子"），限制向中国客户出口 3D991／3E991 软件与技术 | A（两公司披露） |
| 2025-05-29 | **Synopsys** 收到类似函件（Synopsys 8-K 原文："pursuant to a letter received on May 29, 2025"） | A（8-K） |
| 2025-06 | 三家暂停对华销售与支持；Synopsys 部分恢复非核心服务（媒体报道） | B |
| 2025-07-02 | BIS 致函 Cadence 与 Synopsys：许可要求撤销，立即生效 | A（两家 8-K） |
| 2025-07-03 | 西门子确认收到撤销通知，恢复对 3D991／3E991 软件与技术的"完整访问权限"，恢复对华销售与技术支持 | A（西门子声明，R12） |

Synopsys 8-K 的关键原文（R10）——这是对函件内容最精确的公司转述：

> "BIS imposing a license requirement for the export, reexport, or in-country transfer of EDA software and technology classified under export control classification numbers (ECCNs) 3D991 and 3E991 **when a party to the transaction is located in China or is a Chinese 'military end user,' wherever located**."

三点精确化：
1. 函件的法律机制是**逐家"知情函"（is-informed letter）**，不是新规则、无联邦公报文本；援引的是既有 EAR 管制（3D991/3E991）加许可要求，前两轮报告写作"isomorphic letter"是笔误，应为 **is-informed**；
2. 三家收到的限制**在范围上一致**（同一档 ECCN、同一触发条件），但**函件文本从未公开**，是否逐字相同无法核实——只能说到"三家公司披露的限制内容一致"为止；
3. Cadence 2025 年 7 月 28 日的 9,500 万美元罚款（司法部另有 4,500 万美元没收协议）是**独立的执法案件**，与 5 月函件无关——必须分开写。

### 4.4 三家企业的管辖权判断

| 企业 | 技术所有权维度 | EAR 法律管辖维度 |
|---|---|---|
| Synopsys | 美国公司，技术所有权在美国 | 产品为美国原产软件 → 无论位于何处均受 EAR 管辖（§734.3）；对华销售受目的地规则、实体清单、军事最终用户规则约束 |
| Cadence | 美国公司，技术所有权在美国 | 同上 |
| Siemens EDA | **股权在德国，经营与主要研发在美国**；技术所有权不可简单归国——是"德国资本持有的美国研发资产" | 其**美国原产产品**（旗舰工具）受 EAR 管辖，附着点是软件原产地而非母公司注册地；**非美国开发的产品**是否受管辖须逐项判断（de minimis／直接产品／最终用途路径）；2025 年 5 月函件证明 BIS 将其涉华交易纳入同一许可框架（其美国业务实体是执法接触点） |

**"影响力来自哪里"的分解**：
- **美国企业的技术所有权**（Synopsys、Cadence）→ 决定"产品是美国原产、天然受 EAR 管辖"，也决定 IP／生态依赖；
- **EAR 法律管辖** → 决定"任何一家——包括德国母公司旗下的西门子 EDA——只要出口美国原产或受管辖物项，就在许可制度内"。技术所有权不是管辖的前提；管辖附着于**物项**，不附着于**股东**；
- 两条通道在 2025 年 5 月叠加生效：没有新规则、没有盟友配合，一封信当天改变三家企业（含一家德资企业）的对华交易状态；40 天后又以同样方式撤销。

### 4.5 最终回答：西门子 EDA 应该如何准确描述？

准确表述："西门子 EDA 是德国西门子集团旗下、总部在美国俄勒冈州的 EDA 业务（前身 Mentor Graphics），其旗舰工具主要在美国研发。它的对华销售之所以受美国出口管制，不是因为'德国公司听美国的话'，而是因为**它出口的软件主要是美国原产物项——EAR 管辖附着在物项的原产地和技术属性上，不附着在母公司的注册地上**。2025 年 5 月 BIS 的通知函证明，这家德资企业的对华业务与美国两家 EDA 公司同受同一套许可框架约束；7 月初撤销时，它也是同样恢复。"

仍不确定、写作时必须回避的内容：函件原文是否逐字相同；西门子 EDA 是否存在完全在美国境外开发、不受 EAR 管辖的产品线；各产品官方分类裁定。

---

## 5. 对前两轮报告的勘误清单

### 5.1 可以保留的内容

1. HBM 管制的三个基本事实：密度门槛 >2 GB/s/mm²、"所有在产 HBM 都超门槛"、共同封装物项排除在 3A090.c 之外（R1 原文）。
2. "美国管住的不是 HBM 这个产品，是'谁买'这件事"——本次核查显示这一判断比前一轮写得更对：买方总部测试同时出现在触发层（§744.23(a)(3)(i)(B)）和审查层（§742.6(b)(10)(ii)）。
3. License Exception HBM 对先进产品形同虚设（3.3 GB/s/mm² 门槛）。
4. Note 1 的"签证窗口"比喻和"封完了也出不去"的结论。
5. EDA 三家企业约七成中国市场份额、40 天开关的时间线、Cadence 罚款单列的处理。
6. "EAR 管辖附着于软件原产地，不附着于母公司注册地"的原则表述。

### 5.2 必须修改的内容

| 位置 | 原表述 | 问题 | 修改为 |
|---|---|---|---|
| 四项审计·证据 3（HBM） | "必须是清单内**美国原产**技术／软件的直接产品" | §734.9(h)(1)(i) 只要求"subject to the EAR"，不要求美国原产；只有 (h)(1)(ii) 工厂路径要求美国原产 | "路径一要求技术／软件受 EAR 管辖并列于清单；路径二（工厂／设备）才要求美国原产" |
| 四项审计·证据 3（HBM） | "设计验证依赖美国 EDA…因此这一条基本会被满足" | 把"使用美国工具"直接等同于 FDPR 成立，越过了"直接产品"的事实判断 | "是否满足取决于逐产品、逐设备的'直接产品'认定，无公开裁定；BIS 序言原文为条件句" |
| 四项审计·证据 4（HBM） | "许可要求只覆盖澳门／D:5 目的地与总部在该地的买方" | 遗漏第二个触发器 §744.23(a)(3)(i)(B)：目的地不限的知情条款 | 补"若知晓物项将流向澳门／D:5 总部实体，任何目的地都需要许可" |
| 四项审计·证据 5（HBM） | "买方总部在 D:5 → 推定拒绝" | 不完整：总部测试是"总部**或**最终母公司总部"二选一即命中 | 补全"或其最终母公司"；并注明推定批准仅适用于向澳门／D:5 递交的申请 |
| 四项审计·License Exception HBM | 只写了密度条件 | 遗漏出口方资格、买方资格、物流、封装厂资格、事后书面确认五组条件 | 按 §740.25 现行全文补全 |
| 四项审计·封装三条路径 | "由经批准的 OSAT 封装并出具证明——低于 300 亿，**或不含 HBM 且**低于 350 亿／400 亿"；公众号版"低于 300 亿、且不含 HBM" | ①300 亿档**不需要**"不含 HBM"条件；②公众号表述把两个 prong 合并成"且"，改变了规则的宽严 | 按原文拆分："低于 300 亿（不论含不含 HBM）；或不含 HBM 且低于 350 亿（2027）／400 亿（2029 年起）" |
| 四项审计·封装 | 未说明推定的适用边界 | 专业读者会误以为推定约束所有人、所有芯片 | 补"仅约束前端厂与 OSAT 的出口／再出口／境内转让；仅适用 16/14 纳米以下或非平面架构；已按 4A003.z 等分类的不适用" |
| 四项审计·封装 | 未提 License Exception ACM | 没有它就无法解释美系芯片为何不受影响 | 补 §740.28：经批准／授权设计者的 3A090.a 芯片，前端厂与 OSAT 的流转无需许可（最终客户不在澳门／D:5） |
| 六节点＋四项审计（EDA） | "isomorphic letter" | 术语错误 | "is-informed letter（知情函）" |
| 四项审计·EDA 时间线 | "2025-05-29 Synopsys 公开确认收到类似函件" | Synopsys 是 5 月 29 日**收到**函件（8-K 原文），公开确认在之后 | 改为"2025-05-29 Synopsys 收到函件（8-K 载明收函日期）" |
| 四项审计·EDA | 西门子收到函件仅媒体佐证 | 现有西门子官方声明（7 月 3 日）自证收到 5 月 23 日函、涉 3D991/3E991、已恢复 | 证据等级从 B 升 A；表述补"西门子自证" |

### 5.3 必须删除或降级表述的内容

1. **"西门子 EDA 的产品是地地道道的美国原产软件"**（四项审计 2.3 节）——降级为"旗舰工具主要在美国研发；逐项产品原产地无公开数据"。公众号表述"产品是地地道道的美国原产软件"删掉，改为"主要在美国研发"。
2. **"总部在澳门或 D:5 的实体，不得进入上述两份名单"**（四项审计·封装）——经授权设计者的排除条件有原文依据，但"不得进入补编 6/7 名单"是推断（名单准入标准未完全公开），降级为"授权设计者的资格条件明确排除澳门／D:5 总部实体；批准名单由 BIS 审查产生"。
3. 前两轮报告中"许可要求只覆盖澳门/D:5"这类**唯一触发器**式的表述——因 §744.23(a)(3)(i)(B) 的存在，一律改为"许可要求主要覆盖澳门／D:5 目的地，另有知情型最终用途条款覆盖'流向 D:5 总部实体'的任何目的地交易"。

### 5.4 仍然无法确认的内容

1. 三星／SK 海力士任何具体 HBM 产品是否满足 §734.9(h) FDPR"直接产品"条件（无公开裁定；实践中两家对华 HBM 销售已实质停止，但这是执法旁证不是法律判定）；
2. 2025 年 5 月三封 EDA 函件的原文（未公开）；三家限制是否逐字一致；
3. 补编 6（经批准 IC 设计者）与补编 7（经批准 OSAT）的完整名单；
4. EDA 具体产品的官方分类裁定；
5. Note 1 中 (b) 档门槛对 2025–2026 年、2028 年交易的字面空缺如何执行（无 BIS 解释公开）。

---

## 6. 可用于公众号文章的准确表述

**问题一（HBM）**：

> 美国本土没有一条 HBM 量产线，但它管住了韩国产 HBM 卖给谁。规则分三层：第一层，三星、SK 海力士的先进 HBM 只要满足"美国技术直接产品"的条件，就落入美国出口管辖；第二层，向中国出口需要许可证，而且如果美国企业"知道"这批货最终流向中国总部企业，哪怕货发到第三国也要申请许可；第三层，申请递交上来，买方是中国企业的，按"推定拒绝"审查。三层加起来，韩国厂把先进 HBM 卖给中国客户这条路，从 2024 年 12 月起就实质关闭了。但注意分寸：美国管的不是"HBM 这个产品"，是"谁买"这件事——卖给美国、日本、台湾客户的 HBM，从头到尾不需要一张美国许可证。

**问题二（先进封装）**：

> 2025 年 1 月，BIS 在先进逻辑芯片的管制条目下加了一条注释：晶圆厂和封装厂出口一颗 16/14 纳米以下的芯片时，先推定它是受控的 AI 芯片。要推翻这个推定，只有三条路：芯片设计者在 BIS 的名单上；晶圆厂自己在澳门和中国以外完成封装，并证明成品晶体管数低于 300 亿；或者由 BIS 批准的封装厂出具同样的证明。注意，300 亿这条不需要看含不含 HBM；再放宽一档（350 亿、400 亿）就必须不含 HBM。全球的 AI 加速器全部超过这条线。所以结果很清楚：英伟达的芯片在封装厂之间流转畅通无阻，中国设计的先进芯片封完了也出不去。美国不能决定台积电把产能分给谁，但它能让一颗封装好的芯片出不去——前者是产能，后者是许可，这两件事经常被混为一谈。

**问题三（EDA）**：

> 2025 年 5 月，BIS 没有发布任何新规则，只是给新思、楷登、西门子 EDA 各发了一封信：向中国出口 3D991 和 3E991 档的 EDA 软件，需要许可证。三家当天停售，40 天后一封信又全部恢复。容易被忽略的是第三家：西门子 EDA 的母公司是德国企业，但它前身 Mentor Graphics，总部在美国俄勒冈州，旗舰工具主要在美国研发。美国出口管制管辖的是软件的出身，不是股东的国籍——所以"德国公司不受美国管辖"这个直觉，在这一行不成立。也要说准另一头：美国管住的是这些美国原产软件的出口，管不住德国母公司账上的资本，更管不住中国工程师桌上那台正在跑国产 EDA 的电脑。

---

## 附：本次审计与总表的衔接

| 修订记录号 | 对应总表条目 | 修改要点 |
|---|---|---|
| R12-01 | HBM/FDPR 相关台账 | 补第二许可触发器 §744.23(a)(3)(i)(B)；FDPR 两路径条件拆分 |
| R12-02 | 先进封装/Note 1 台账 | 三路径主体与门槛拆分；补 ACM 例外与推定适用边界 |
| R12-03 | EDA 管辖台账 | 西门子证据升级；"美国原产"表述降级；is-informed 术语更正 |

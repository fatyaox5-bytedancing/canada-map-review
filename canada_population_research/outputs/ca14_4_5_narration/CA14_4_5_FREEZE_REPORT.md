# CA-14.4.5 冻结报告（V5 → V6）

**结论：建议冻结。** 见 §五。

**输出**：`CA14_4_5_NARRATION_V6_CANDIDATE.md`（英文旁白 + 中文对照，五章完整）
**来源**：`outputs/ca14_4_4_narration/CA14_4_4_NARRATION_V5_CANDIDATE.md`

---

## 一、本次两处修改

### 修改 1｜第 1 章 1.4：地理跨度表述

**修改前（V5）**

> The six largest are spread far apart, from the Pacific coast to the Atlantic. So where is everybody?

**修改后（V6）**

> The six largest are spread across thousands of kilometres, from Vancouver on the Pacific coast to Montreal in the east. So where is everybody?

中文对照同步改为：**「最大的六个相距数千公里，从太平洋沿岸的温哥华，一直东到蒙特利尔。那么，人都到哪里去了？」**

`So where is everybody?` 作为独立设问句保留。

### 修改 2｜第 3 章 3.3：均值与中位数段落

**修改前（V5）**

> ... That average is pulled up by a few very large centres — Toronto itself accounts for five and a half million of the six and a quarter million. The median population centre in that band is not much bigger than the median one to the west.

**修改后（V6）**

> ... That average is dominated by Toronto itself, which accounts for about five and a half million of the six and a quarter million people in this band. The median tells a less dramatic story: the typical population centre is much smaller than the average suggests.

中文对照同步改为：**「这个平均值主要由多伦多本身决定——在这个带约 625 万人里，它一个就占了约 550 万。中位数讲的则是另一个没那么惊人的故事：典型的人口中心，比平均值给人的印象要小得多。」**

**关于 550 万 / 625 万的口径标注**：这两个数是**原始 0.5° 经度分箱口径下的约数**，**不是**不受分箱边界影响的统计量。CA-14.4.4 的边界敏感性检验已证明：该带的总人口与成员数会随分箱边界变化（Toronto 带 n 在 28 ~ 34 之间浮动）。**因此 V6 未在任何位置把这两个数描述为「不受分箱边界影响」。**

---

## 二、历史版本未被覆盖（逐一核验）

| 版本文件 | 状态 |
|---|---|
| `ca14_4_narration/CA14_4_NARRATION_V1.md` | ✅ 未改动 |
| `ca14_4_narration/CA14_4_FACT_CHECK.md` | ✅ 未改动 |
| `ca14_4_1_narration/CA14_4_1_NARRATION_V2_CANDIDATE.md` | ✅ 未改动 |
| `ca14_4_1_narration/CA14_4_1_REVISION_REPORT.md` | ✅ 未改动 |
| `ca14_4_2_narration/CA14_4_2_NARRATION_V3_CANDIDATE.md` | ✅ 未改动 |
| `ca14_4_2_narration/CA14_4_2_FINAL_REVIEW_REPORT.md` | ✅ 未改动 |
| `ca14_4_3_narration/CA14_4_3_NARRATION_V4_CANDIDATE.md` | ✅ 未改动 |
| `ca14_4_3_narration/CA14_4_3_FINAL_CHECK_REPORT.md` | ✅ 未改动 |
| `ca14_4_4_narration/CA14_4_4_NARRATION_V5_CANDIDATE.md` | ✅ 未改动（**本次只读**） |
| `ca14_4_4_narration/CA14_4_4_FREEZE_REVIEW.md` | ✅ 未改动 |

**新文件只写入** `outputs/ca14_4_5_narration/`。项目目录内**未创建** `.git`。**未生成**分镜、图片、地图、音频或视频。

---

## 三、词数与估算时长

| 章 | English title | V5 | **V6** | 变化 |
|---:|---|---:|---:|---:|
| 1 | *A Country That Looks Empty* | 115 | **121** | +6 |
| 2 | *Two Squares* | 152 | **152** | 0 |
| 3 | *One Corridor, Two Different Things* | 354 | **354** | 0 |
| 4 | *The Other Half* | 162 | **162** | 0 |
| 5 | *What This Map Does and Doesn't Say* | 175 | **175** | 0 |
| | **合计** | **958** | **964** | **+6** |

**全片英文词数：964 词**（V5 为 958 词，+6）

| 语速 | 估算时长 |
|---|---:|
| 135 wpm | **428 秒** |
| 140 wpm | **413 秒** |
| 150 wpm | **386 秒** |

**中文对照合计 1,486 字。**

**第 3 章词数显示「变化 0」是巧合而非漏改**：该章 3.3 段确实被替换（已逐块核验：3.1 / 3.2 / 3.4 / 3.5 / 3.6 逐字相同，**仅 3.3 被改动**），但新旧两版按同一计词规则恰好都是 109 词，因此该章合计 354 词不变。

**未为满足 379 秒而删减或填充内容。**

---

## 四、尚未实际试读或合成（事实记录）

- **本项目没有任何一段旁白被实际朗读过。**
- TTS 路径在沙箱内被阻断，CA-13.4 已穷尽 6 条尝试（含 SAPI `E_ACCESSDENIED`），**全部失败**。
- 因此上表**所有时长均为按词数换算的估算值**，精度约 ±10%，**未经任何实测校准**。
- 英文旁白为**书面稿**，**未经英语母语者朗读测试**。
- **本轮未做任何音频相关工作**，未生成音频文件。

---

## 五、是否存在阻止冻结的重大问题

**判断：不存在阻止冻结的重大问题。建议冻结。**

已逐项复核以下验收事项：

| 验收事项 | 结果 |
|---|---|
| 1. 两处指定修改已完成（英文与中文对照均已同步） | ✅ |
| 2. 其他已核验数字未被意外改动 | ✅ 逐块比对确认仅 3.3 被改动；59% 分母澄清、3.5 两段采样点数（32 / 47）、25 km 阈值、「不意味着中间土地无人」限定、北部 12 / 69,029 与 14 / 71,592、561 组距离中位数约 1,400 km、15 组距离中位数约 2,700 km、43% / 80,000 km²、414 与约 59%、51.8 km / 21.1% / 232 km 均在位 |
| 3. 五章完整，英文正文完整 | ✅ 五章标题齐全，各章引文块数 4 / 4 / 6 / 3 / 4 |
| 4. 词数与时长计算正确 | ✅ 各章变化之和 +6 = 总计变化 +6；964 词 → 428 / 413 / 386 秒 |
| 5. 无明显语法错误、数字错误或自相矛盾 | ✅ 未发现 |

**需随冻结一并入档、但不阻止冻结的既有事项**：

1. **全片 135 wpm 估算为 428 秒**，超出 379 秒。按任务要求未因此删减内容。由于从未试读，该估算本身的 ±10% 不确定度**大于**它与 379 秒的差值。
2. **画面精确值 58.7% 与旁白「约 59%」并存**——沿用既有裁定。
3. **414 与 424 的集合关系仍未证明**；按任务要求本次未再追查，旁白 0 处出现 424。
4. **经度带比较的纬度带不同**（3.40° vs 4.08°），且以西四带被 BOUNDS 西界截断（8 个中心 / 41,188 人未计入），因此该比较只能表述为「这两个经度带之间」。V6 未做任何外推。
5. **第 3 章 3.3 的 550 万 / 625 万为原始分箱口径下的约数**，随分箱边界变化（见 §一 修改 2）。V6 未宣称其为边界无关量。
6. **`PCCLASS` 官方含义与 population centre 官方定义文本本项目均未取得**；V6 只说 `A population centre is where people are concentrated`。

**除两处指定修改外，本次未做任何其他修辞优化，未新增未经核验的事实或因果解释。**


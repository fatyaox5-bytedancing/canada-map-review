# Task 17-A · 第一章音频切分报告

- 生成时间：2026-10-13T10:25:55Z
- 唯一音频源：`BehindTheBreakdown\assets\audio\narration\tencent-101050\ch01.wav`
  - sha256 `ea9b566bde289de437e3a5e867731f6f72a80441e7d7b3ad6016426b9f0d8e1f`
  - 1 声道 / 16 bit / 16000 Hz / 1462880 帧 / 91.430 秒
- 词级时间戳：`BehindTheBreakdown\assets\audio\narration\tencent-101050\ch01.timings.json`（253 条，`duration_ms=91430`，4 个分块）
- 文本依据：`BehindTheBreakdown\assets\audio\ch1_manifest.json` 的六段，与 `04_TRICOLOR_SCRIPT_V2.md` 第一章旁白**逐字符相等**（1352 字符）
- V2 sha256：`c3a5b9da2788a2a54eafd2b9330e961cc5600dab4f5cb1aa838f12db175dafd2`
- **未调用任何 TTS 接口，未重新生成任何语音，未修改源音频。**

## 1. 六段总览

| 段 | 对应 V2 段落 | 词数 | 起始（章内） | 结束（章内） | 时长 | 峰值 dBFS | 削波 | 静音占比 | sha256 前缀 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | 第 1 段 | 29 | 0:00.250 | 0:10.040 | 0:10.245 | -8.9 | 0 | 42.5% | `0241bc4ea71eddaa…` |
| 2 | 第 2 段 | 24 | 0:10.570 | 0:20.640 | 0:10.635 | -8.9 | 0 | 45.2% | `e4db19e89673db3f…` |
| 3 | 第 3 段 | 27 | 0:21.240 | 0:31.110 | 0:10.460 | -8.9 | 0 | 44.1% | `4e642e761d88a241…` |
| 4 | 第 4 段 | 63 | 0:31.690 | 0:55.590 | 0:24.510 | -8.9 | 0 | 45.6% | `eb84a7970762d9fa…` |
| 5 | 第 5 段 | 34 | 0:56.230 | 1:09.830 | 0:14.185 | -9.1 | 0 | 47.3% | `7e41b476e07731bb…` |
| 6 | 第 6 段 | 46 | 1:10.360 | 1:31.180 | 0:21.395 | -8.9 | 0 | 43.3% | `bf6d76cfa4ae080d…` |
| | **合计** | **223** | 0:00.000 | 1:31.430 | **1:31.430** | | | | |

文件：`BehindTheBreakdown\outputs\voice_auditions\task17_ch1_segments/ch1_seg01.wav` … `ch1_seg06.wav`

## 2. 切分点与“未截断单词”的证据

每个切点都落在两段之间的**静音间隙内、且取该间隙内振幅最小的采样点**，并逐一核对它位于**前一词的结束时间之后、后一词的开始时间之前**。

| 切点 | 前一词（结束 ms） | 后一词（开始 ms） | 间隙长度 | 切点位置 | 距前词 | 距后词 | 切点振幅 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | `bank` (10040) | `Tricolor` (10570) | 530 ms | 10245.0 ms | 205.0 ms | 325.0 ms | 0 （静音） |
| 2 | `histories` (20640) | `But` (21240) | 600 ms | 20880.0 ms | 240.0 ms | 360.0 ms | 0 （静音） |
| 3 | `investors` (31110) | `Here` (31690) | 580 ms | 31340.0 ms | 230.0 ms | 350.0 ms | 0 （静音） |
| 4 | `loans` (55590) | `That` (56230) | 640 ms | 55850.0 ms | 260.0 ms | 380.0 ms | 0 （静音） |
| 5 | `clear` (69830) | `Tricolor` (70360) | 530 ms | 70035.0 ms | 205.0 ms | 325.0 ms | 0 （静音） |

## 3. 验证结果

| 检查项 | 结果 | 说明 |
| --- | --- | --- |
| segment count | PASS | 6 files |
| contiguous, no gaps or overlap | PASS | each segment starts where the previous ends |
| sum of durations equals source | PASS | 91.430s vs 91.430s |
| reassembly is byte-identical to source PCM | PASS | sha256 eb4f00d2416e6803… == eb4f00d2416e6803… |
| cut 1 keeps both words whole | PASS | between frame 160640 and 169120 |
| cut 2 keeps both words whole | PASS | between frame 330240 and 339840 |
| cut 3 keeps both words whole | PASS | between frame 497760 and 507040 |
| cut 4 keeps both words whole | PASS | between frame 889440 and 899680 |
| cut 5 keeps both words whole | PASS | between frame 1117280 and 1125760 |
| no segment is silent | PASS | seg1 peak 11796, seg2 peak 11796, seg3 peak 11731, seg4 peak 11796, seg5 peak 11551, seg6 peak 11796 |
| no clipped samples | PASS | 0 clipped samples in every segment |
| VIOLATION CHECK: source audio untouched | PASS | sha256 ea9b566bde289de4… unchanged |

## 4. 拼接还原

六段是**连续无重叠**的切片，按原顺序拼接后与源音频 PCM：

- 源音频 PCM sha256：`eb4f00d2416e680367dbda28619e58c39a3e0a1f8d671a728507fbe27e017eea`
- 拼接结果 PCM sha256：`eb4f00d2416e680367dbda28619e58c39a3e0a1f8d671a728507fbe27e017eea`
- **字节级完全一致：是**

## 5. 各段对应的 V2 原文（完整）

### 第 1 段 · `ch1_seg01.wav` · 0:10.245 · 章内 0:00.250–0:10.040

In the United States, some used-car dealers do more than sell cars. They also lend money to customers who may struggle to get a loan from a traditional bank.

### 第 2 段 · `ch1_seg02.wav` · 0:10.635 · 章内 0:10.570–0:20.640

Tricolor was one of those businesses. Based in Texas, it sold used cars and provided subprime auto loans to customers with limited credit histories.

### 第 3 段 · `ch1_seg03.wav` · 0:10.460 · 章内 0:21.240–0:31.110

But the business did not depend only on customers making their monthly payments. Those loans could also be used to raise money from financial institutions and investors.

### 第 4 段 · `ch1_seg04.wav` · 0:24.510 · 章内 0:31.690–0:55.590

Here is how it works. A lender makes hundreds or thousands of car loans. Instead of waiting years for every borrower to pay the money back, it can group those loans together and use them to obtain funding. In a securitization, the loans are packaged into financial securities that investors can buy. The lender gets money upfront, which can help finance more loans.

### 第 5 段 · `ch1_seg05.wav` · 0:14.185 · 章内 0:56.230–1:09.830

That arrangement can be perfectly legitimate. But it depends on a basic assumption: the loans must exist, the information about them must be accurate, and the rights to the underlying assets must be clear.

### 第 6 段 · `ch1_seg06.wav` · 0:21.395 · 章内 1:10.360–1:31.180

Tricolor filed for Chapter 7 bankruptcy on September 10, 2025. The subsequent investigations raised serious questions about whether the auto loans backing its financing arrangements had been accurately reported—and whether some of the same loans had been used to support more than one claim for funding.

---

**报告结束。**

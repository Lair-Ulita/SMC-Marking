<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=220&section=header&text=SMC%20Marks&fontSize=72&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Smart%20Money%20Concepts%20for%20TradingView&descSize=20&descAlignY=60" alt="SMC Marks banner" width="100%"/>

<a href="https://github.com/kxngHADES/SMC-Marking">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=800&color=2EE6A6&center=true&vCenter=true&width=700&lines=Market+Structure+%E2%80%A2+HH+%2F+HL+%2F+LH+%2F+LL;BMS+%2F+BOS+and+CHoCH+detected+automatically;Premium+%E2%80%A2+Discount+%E2%80%A2+Equilibrium;Order+Blocks+%E2%80%A2+Fair+Value+Gaps+%E2%80%A2+Liquidity;Free+to+use.+Not+for+sale." alt="Typing animation"/>
</a>

<br/>

<p align="center">
  <a href="https://github.com/kxngHADES/SMC-Marking/stargazers"><img src="https://img.shields.io/github/stars/kxngHADES/SMC-Marking?style=for-the-badge&logo=github&color=f5c542" alt="Stars"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking/network/members"><img src="https://img.shields.io/github/forks/kxngHADES/SMC-Marking?style=for-the-badge&logo=github&color=2ea44f" alt="Forks"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking/watchers"><img src="https://img.shields.io/github/watchers/kxngHADES/SMC-Marking?style=for-the-badge&logo=github&color=1f6feb" alt="Watchers"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking/issues"><img src="https://img.shields.io/github/issues/kxngHADES/SMC-Marking?style=for-the-badge&color=d73a4a" alt="Issues"/></a>
</p>

<p align="center">
  <a href="https://github.com/kxngHADES/SMC-Marking/commits/main"><img src="https://img.shields.io/github/last-commit/kxngHADES/SMC-Marking?style=flat-square&color=8250df" alt="Last commit"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking/graphs/commit-activity"><img src="https://img.shields.io/github/commit-activity/m/kxngHADES/SMC-Marking?style=flat-square&color=0e8a16" alt="Commit activity"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking"><img src="https://img.shields.io/github/repo-size/kxngHADES/SMC-Marking?style=flat-square&color=orange" alt="Repo size"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking/graphs/contributors"><img src="https://img.shields.io/github/contributors/kxngHADES/SMC-Marking?style=flat-square&color=blue" alt="Contributors"/></a>
  <a href="https://github.com/kxngHADES/SMC-Marking/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-Free%20Use%20%7C%20Non--Commercial-red?style=flat-square" alt="License"/></a>
  <img src="https://img.shields.io/badge/Pine%20Script-v6-1f9d55?style=flat-square&logo=tradingview&logoColor=white" alt="Pine Script v6"/>
  <img src="https://img.shields.io/badge/platform-TradingView-2962ff?style=flat-square&logo=tradingview&logoColor=white" alt="TradingView"/>
  <img src="https://img.shields.io/badge/price-FREE-brightgreen?style=flat-square" alt="Free"/>
</p>

<br/>

**[安装](#安装)** &nbsp;|&nbsp; **[使用方法](#使用方法)** &nbsp;|&nbsp; **[设置](#设置)** &nbsp;|&nbsp; **[警报](#警报)** &nbsp;|&nbsp; **[基础术语](#基础术语)** &nbsp;|&nbsp; **[许可](#许可)**

<br/>

> 一款 Pine Script&trade; v6 指标，自动标注**市场结构**、**BMS / BOS**、**CHoCH**、带**溢价 / 折价 / 均衡**的**交易区间**、**订单块**、**公允价值缺口**、**EQH / EQL 流动性**、**时段关键价位**、**分形**以及**警报**。

</div>

---

> **中文翻译说明**：本文件译自英文原版 README，原文与原始许可见 [kxngHADES/SMC-Marking](https://github.com/kxngHADES/SMC-Marking)。译文仅为阅读便利，若与原文有出入以原文为准；翻译不改变原许可条款，作者署名与许可声明须随文保留。

## 实战演示

> **仅为动画演示，不构成任何投资建议。** 以下只是视觉示意，不是教学，也不是推荐。

一段示意图，展示在 TradingView 风格图表上使用 SMC Marks 时，一笔交易可能如何演进。示例中，交易者等待 **CHoCH**、标出**折价区**，在折价区**做多**并设好止损（SL）与止盈（TP），最终打到目标；随后行情转空，交易者又以同样方式从**溢价区**做空。

<div align="center">

<img src="https://raw.githubusercontent.com/kxngHADES/SMC-Marking/main/assets/trade-demo.svg" alt="动画演示：看涨 CHoCH 进入折价区做多，随后看跌 CHoCH 进入溢价区做空，各自带止损与止盈" width="100%"/>

</div>

| 步骤 | 动画展示的内容 |
|---|---|
| 1 | 结构为看跌（LH、LL）。等待 **CHoCH**。 |
| 2 | CHoCH 突破最近的 LH，偏向翻转为看涨，并标出**折价区**。 |
| 3 | **做多**：在折价区入场，**SL** 放在 HL 下方，**TP** 设为 3R。 |
| 4 | 让行情自行演进。TP 达成，**+3R**。 |
| 5 | 出现新的 HH 与 **BMS**，随后一根看跌 CHoCH 再次翻转偏向。 |
| 6 | **做空**：在溢价区入场，**SL** 放在 LH 上方，**TP** 设为 2.5R。TP 达成，**+2.5R**。 |

> **仅为动画。** 演示中的价格走势为虚构，仅用于说明一笔交易*可能*如何演进。它**不是真实交易，不是投资建议，也不是教学**，不代表任何收益承诺。

---

## 概览

这款 Smart Money Concept（SMC，聪明钱概念）指标把运用 SMC 交易所需的核心功能集于一身。它基于 Inner Circle Trader（ICT）所传授的聪明钱概念构建。

"聪明钱"指机构投资者、基金及其他大型市场参与者所配置的资金。本指标把这种机构交易行为可视化，让散户也能通过机器自动绘制的标注看清市场内在结构。

它在单一指标里给出 SMC 最重要的原则：市场结构突破、性质转变、当前交易区间、溢价与折价、分形、摆动结构，全部自动完成并实时更新。此外还包含基于市场结构原理的 SMC 趋势判断，以及可选的"已确认摆动趋势"背景着色，让趋势一眼可读。

### 核心功能

- **摆动结构**：识别主要市场结构，并把每个确认的摆动点标注为 **HH**、**HL**、**LH** 或 **LL**。
- **当前交易区间**：始终显示当前区间在哪，以及溢价区与折价区在区间中的位置。区间实时更新，无延迟。
- **溢价与折价区**：自动绘制溢价区、折价区与均衡区。
- **结构突破**：实时识别并绘制市场结构突破（**BMS/BOS**）与性质转变（**CHoCH**）。可选的次级（内部）突破为 **MBOS** 与 **iCHoCH**。
- **供给与需求**：订单块标出高概率的供给区与需求区，一旦被消化（缓解）即移除。
- **失衡（FVG）**：三根K线形成的公允价值缺口，部分回补时收缩，完全回补（缺口回补）后移除。
- **流动性**：等高点（**EQH** = 买方流动性）与等低点（**EQL** = 卖方流动性）。
- **时段关键价位**：日内高点/低点（**HOD / LOD**）与周内高点/低点（**HOW / LOW**）。
- **分形**：经典 5 根K线分形高与分形低。
- **信息面板**：显示当前趋势（看涨 / 看跌 / 中性），以及区间的上沿、下沿与中轴数值。
- **图内 SMC 术语表**：可开关的缩写对照表。
- **悬停提示**：图上每个标签都带说明，鼠标移上去即可看到含义。
- **警报**：覆盖 CHoCH、BMS、内部突破、新 HH/LL、EQH/EQL，以及价格进入溢价区或折价区。

---

## 安装

1. 打开 [TradingView](https://www.tradingview.com/) 并加载任意图表。
2. 点开屏幕底部的 **Pine 编辑器（Pine Editor）** 标签页。
3. 删除模板代码，然后整段复制粘贴 [`SMC_Terminology_marks.pine`](https://raw.githubusercontent.com/kxngHADES/SMC-Marking/main/SMC_Terminology_marks.pine) 的全部内容。
4. 点击 **保存（Save）**，再点 **添加到图表（Add to chart）**。
5. 点击图表上指标名称旁的 ⚙️ 齿轮图标，打开**设置**。

---

## 使用方法

1. **先读趋势。** 信息面板（默认在右上角）显示当前摆动趋势：**看涨**（绿）为多头结构，**看跌**（红）为空头结构。也可以打开*已确认摆动趋势背景着色*，给图表整体加底色。
2. **跟随结构。** 上涨中寻找 **HH → HL** 序列，以及确认延续的看涨 **BMS/BOS**；下跌中寻找 **LH → LL** 与看跌 BMS/BOS。
3. **留意 CHoCH。** **CHoCH** 是第一次*逆着*当前趋势的突破，往往是最早的反转征兆。
4. **用溢价与折价。** 看涨趋势里从**折价区**（区间下部）找做多；看跌趋势里从**溢价区**（区间上部）找做空。**均衡区**是区间的 50% 位置。
5. **用 POI 细化入场。** 打开**订单块**与**公允价值缺口**，在溢价区或折价区内寻找精确的兴趣点。
6. **关注流动性。** **EQH / EQL** 显示滞留流动性（BSL / SSL）所在。价格启动前常被吸引到这些位置。HOD/LOD 与 HOW/LOW 同样可作为流动性目标。
7. **多周期配合。** 在高周期（HTF）定偏向，再切到低周期（LTF），等待与偏向同向的 CHoCH 或 MBOS 出现后入场。
8. **设置警报。** 右键图表 → **添加警报（Add alert）**，条件选 **SMC Marks**，再选择事件（例如 *看涨 CHoCH*）。

> 多数附加功能（订单块、FVG、EQH/EQL、时段关键价位、分形、内部结构）默认关闭，以保持图表简洁。按需开启即可。

---

## 设置

### 市场结构（摆动）

| 设置项 | 默认 | 说明 |
|---|---|---|
| 市场结构周期 | `10` | 确认一个摆动高点/低点所需的左右两侧K线数量。超短线：3–5，日内：5–10，波段：10–20，趋势：20–50。 |
| 突破确认方式 | `收盘价` | **收盘价**：K线必须收在摆动价位之外；**影线**：影线越过该价位即算突破。 |
| 顺势突破标签 | `BMS` | 沿趋势方向突破时显示的文字：`BMS` 或 `BOS`。 |
| 显示 HH / HL / LH / LL | 开 | 标注每个已确认的摆动点。 |
| 显示 BMS / CHoCH | 开 | 绘制结构突破线与标签。 |
| 标签字号 | `小` | 极小 / 小 / 正常。 |
| 颜色 | — | 看涨/看跌趋势、BMS/BOS、CHoCH、HH、HL、LH、LL。 |
| 已确认摆动趋势背景着色 | 关 | 按摆动趋势给图表背景填充绿/红。 |

### 内部结构（次级）

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示 MBOS / iCHoCH | 关 | 次级（内部）结构突破，以虚线绘制。 |
| 内部结构周期 | `5` | 用于内部结构的枢轴长度。 |
| 颜色 | — | MBOS、iCHoCH。 |

### 当前交易区间

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示交易区间 | 开 | 填充当前成交（dealing）区间，并标注区间上沿/下沿。 |
| 显示溢价 / 折价 / 均衡区 | 开 | 绘制溢价区、折价区与均衡区。 |
| 溢价/折价区深度 % | `20` | 溢价区与折价区的高度，占区间跨度的百分比。 |
| 溢价/折价区距区间边缘 % | `5` | 区间边缘与溢价/折价区之间的间隔。 |
| 均衡带宽度 % | `5` | 50% 位置附近均衡带的厚度。 |
| 向右延伸（K线数） | `20` | 区域与水平线向右延伸出当前K线的长度。 |
| 颜色 | — | 区间、溢价区、均衡区、折价区。 |

### 订单块（供给与需求）

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示订单块 | 关 | **需求订单块**：看涨突破前最低的那根K线。**供给订单块**：看跌突破前最高的那根K线。 |
| 每侧最大数量 | `3` | 每侧保留的有效订单块数量。 |
| 失效判定 | `收盘价` | 收盘价还是影线穿越该块时将其移除。 |
| 颜色 | — | 需求、供给。 |

### 失衡（FVG / IMB）

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示公允价值缺口 | 关 | 三K线失衡。部分回补的缺口收缩，完全回补后移除。 |
| 最小缺口（× ATR） | `0.0` | 过滤掉过小的缺口（ATR 200 的倍数）。 |
| 每侧最大数量 | `5` | 每侧保留的有效缺口数量。 |
| 颜色 | — | 看涨、看跌。 |

### 流动性（EQH / EQL）

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示等高点 / 等低点 | 关 | EQH 标记上方的买方流动性，EQL 标记下方的卖方流动性。 |
| 确认K线数 | `3` | 用于识别等高点与等低点的枢轴长度。 |
| 等值阈值（× ATR） | `0.1` | 两个枢轴要多接近（ATR 的倍数）才算"相等"。 |
| 颜色 | — | EQH、EQL。 |

### 时段关键价位

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示日内高点 / 日内低点 | 关 | 当日截至目前运行的最高价/最低价（仅日内周期图表）。 |
| 显示周内高点 / 周内低点 | 关 | 本周截至目前运行的最高价/最低价（周线以下的周期）。 |
| 颜色 | — | 日内高低、周内高低。 |

### 分形

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示分形 | 关 | 经典 5 根K线分形高点（▼）与分形低点（▲）。 |

### 信息面板

| 设置项 | 默认 | 说明 |
|---|---|---|
| 显示趋势 / 区间面板 | 开 | 趋势状态，以及区间上沿、区间下沿、中轴数值。 |
| 面板位置 | `右上` | 面板在图表上的位置。 |
| 显示 SMC 术语表 | 关 | 图内的 SMC 缩写对照表。 |
| 术语表位置 | `左下` | 术语表在图表上的位置。 |

---

## 警报

| 警报 | 触发条件 |
|---|---|
| 看涨 CHoCH / 看跌 CHoCH | 摆动结构逆趋势方向突破 |
| 看涨 BMS / 看跌 BMS | 摆动结构沿趋势方向突破 |
| 看涨 / 看跌内部结构突破 | 出现内部 MBOS 或 iCHoCH |
| 新的更高高点 / 新的更低低点 | 确认新的 HH 或 LL |
| 等高点 / 等低点 | 检测到 EQH（BSL）或 EQL（SSL） |
| 价格进入溢价区 / 折价区 | 收盘价穿越到溢价区或折价区 |

---

## 基础术语

| 缩写 | 含义 |
|---|---|
| SBD | 供需区（Supply & Demand） |
| S2D | 供给转需求（Supply to Demand） |
| D2S | 需求转供给（Demand to Supply） |
| OB | 订单块（Orderblock） |
| AOI | 关注区域（Area of Interest） |
| POI | 兴趣点（Point of Interest） |
| LoR | 有效水平（Level of Respect） |
| FLOR | 第一有效水平（First Level of Respect） |
| IMB | 失衡（Imbalance） |
| Ineff. | 低效性（Inefficiency）：单边订单流留下未填补缺口的价格运行（见 FVG） |
| IRL | 内部区间流动性（Internal Range Liquidity） |
| FML | 公允价值缺口流动性（Fair Value Gap Liquidity） |
| FVG | 公允价值缺口（Fair Value Gap） |
| HH | 更高高点（Higher High） |
| HL | 更高低点（Higher Low） |
| LH | 更低高点（Lower High） |
| LL | 更低低点（Lower Low） |
| BOS | 结构突破（Break of Structure） |
| BMS | 市场结构突破（Break of Market Structure） |
| RBOS | 散户结构突破（Retail Break of Market Structure） |
| MBOS | 次级结构突破（Minor Break of Structure） |
| SMC | 聪明钱概念（Smart Money Concepts） |
| CHoCH | 性质转变（Change of Character） |
| EQH | 等高点（Equal Highs） |
| EQL | 等低点（Equal Lows） |
| BSL | 买方流动性（Buy Side Liquidity） |
| SSL | 卖方流动性（Sell Side Liquidity） |
| LQ | 流动性（Liquidity） |
| ES | 均衡（Equilibrium） |
| PA | 价格行为（Price Action） |
| HTF | 高时间周期（Higher Timeframe） |
| LTF | 低时间周期（Lower Timeframe） |
| FT | 斐波那契（Fibonacci） |
| CF | 已确认趋势（Confirmed Trend） |
| OF | 订单流（Orderflow） |
| EXO | 外部订单流（External Orderflow） |
| LOD | 日内低点（Low of the Day） |
| HOD | 日内高点（High of the Day） |
| HOW | 周内高点（Highs of the Week） |
| LOW | 周内低点（Lows of the Week） |
| RE | 风险入场（Risk Entry） |
| RR | 风险回报比（Risk Reward） |
| GF | 缺口回补（Gap Fill） |
| HFs | 对冲基金（Hedge Funds） |

---

## 支持项目

如果这个指标对你的交易有帮助，可以用这些免费的方式表示感谢：

<div align="center">

[![Star this repo](https://img.shields.io/badge/%E2%AD%90_Star_this_repo-f5c542?style=for-the-badge&logo=github&logoColor=black)](https://github.com/kxngHADES/SMC-Marking)
[![Fork](https://img.shields.io/badge/Fork_it-2ea44f?style=for-the-badge&logo=github)](https://github.com/kxngHADES/SMC-Marking/fork)
[![Report issue](https://img.shields.io/badge/Report_an_issue-d73a4a?style=for-the-badge&logo=github)](https://github.com/kxngHADES/SMC-Marking/issues/new)

<br/>

<a href="https://star-history.com/#kxngHADES/SMC-Marking&Date">
  <img src="https://api.star-history.com/svg?repos=kxngHADES/SMC-Marking&type=Date" alt="Star History Chart" width="600"/>
</a>

</div>

---

## 免责声明

本指标仅用于教育目的与信息参考，**不构成投资建议**。外汇、差价合约及其他杠杆产品的交易风险极高，未必适合所有投资者。请务必自行分析并做好风险管理。

## 许可

**免费使用。免费分享。不得销售。**

本项目基于 [SMC Marks Free Use License (Non-Commercial)](https://github.com/kxngHADES/SMC-Marking/blob/main/LICENSE) 发布。

| 你可以 | 你不可以 |
|---|---|
| 用于自己的交易 | 出售它或任何修改版本 |
| 免费复制、修改与分享 | 放到付费墙、订阅、课程或付费社群之后 |
| 学习它并在此基础上继续开发 | 移除作者署名或本许可声明 |

需要商业使用？请先取得书面许可。

<div align="center">

&copy; [kxngHADES](https://github.com/kxngHADES)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=100&section=footer" width="100%" alt="footer"/>

</div>

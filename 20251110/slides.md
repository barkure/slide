---
theme: neversink
mdc: true
---

## Three stages of plateau evolution manifested in present-day Tibetan Plateau

**冯超俊 & 齐鑫瑶**

**2025.11.10**

---

# Introduction

<div class='mt-5'>
问题：青藏高原的演化是大陆动力学中的一个核心课题，但关于高原隆升的普遍机制仍不明确，以往的高原演化模型也未能清晰揭示实际的地球动力学过程。
</div>
<div class='mt-10'>
本研究利用 CSRM 项目整合的地震数据，基于高分辨率地震联合反演，识别出青藏高原中地壳低速带（LVZs）的空间分布与熔体成熟度梯度，提出“年轻熔融—莫霍加厚—地表隆升”三阶段中地壳流变演化模型：
</div>

<div class='mt-3 grid grid-cols-2 gap-6'>
<div class='mt-7'>

1. Pre-response stage：中地壳存在年轻的局部熔融区，但地表地形和莫霍面几乎无明显响应；
2. First stage of response：中地壳局部熔融区趋于成熟，莫霍面加深，但地表未发生大规模隆升；
3. Last stage of response：地表发生大规模隆升。
</div>
<img border="rounded" src="/fig1.png">
</div>


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #2eafc0ff 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

# Data and inversion of LVZ features

本研究通过反演地壳剪切波速度（${\text{V}}_{\text{s}}$）结构来识别低速带（LVZ）特征，使用了三类地震数据约束：
- 来自远震事件的 P 波接收函数（RFs）；
- 基于连续背景噪声和地震数据反演的 Rayleigh 波相速度；
- 来自远震事件的 Rayleigh 波垂直/水平位移比（ZH）。

## RFs
RFs 共包含来自 1,933 个地震台的 727,201 条接收函数，对其进行如下处理：

1. 统一校正至相同射线参数（0.06 s/km），并按 10° 分组叠加（Bin stacked RF）；
2. 根据是否在 Pms 震相（莫霍面的 P-to-S 转换）前是否出现明显的负相位（ Pls 震相），将 RFs 分为两类，并进一步按波形相似性聚类，形成“聚类叠加 RF”（Cluster stacked RF）。

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #2eafc0ff 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

## RFs - Station & events locations (a), Raw RF (b)

<div class='mt-10 mx-20'>
<img border="rounded" src="/sup_fig1_ab.png">
</div>
---

## RFs - Bin stacked RF \(c), Cluster stacked RF (d)

<div class='mt-10 ml-10'>
<img border="rounded" src="/sup_fig1_cd.png">
</div>
---

## Rayleigh wave phase velocities

<div class='mt-5'>
Rayleigh 波相速度采用同步反演方法获得：8–50 s 周期的模型同时受背景噪声的台站间测量和区域地震事件-台站测量约束；50–70 s 周期的模型仅由地震事件-台站测量约束。
</div>

(a) 展示了周期为 10 秒、20 秒、30 秒、40 秒、50 秒和 62 秒的 Rayleigh 波相速度反演图。

<div class='mx-34'>
<img border="rounded" src="/sup_fig2_a.png">
</div>

---

## Rayleigh wave phase velocities

(b) 环境噪声数据库（AN database）中用于测量台站间 Rayleigh 波相速度频散曲线的地震台站（蓝色三角形）。

<div>
(c) 地震面波数据库（ESW database）中用于测量地震事件-台站间 Rayleigh 波相速度频散曲线的地震台站（蓝色三角形）和地震事件（红色五角星）。
</div>

<div class='mt-3 mx-20'>
<img border="rounded" src="/sup_fig2_bc.png">
</div>

---

## ZH ratio dataset

ZH 比数据集由区域内 4709 个地震事件构成，仅选用具有高质量接收函数的台站。

(a) 为周期为 20s、40s、60s 和 80s 时反演得到的 Rayleigh 波 ZH 比分布图；(b) 为对应的测量不确定性分布图。

<div class='mx-25'>
<img border="rounded" src="/sup_fig3.png">
</div>

---

## Methods Overview
<div class='mt-5'>
本研究采用 Xiao 等人发展的联合反演方法<span style="color: #00f">*</span>，在不同后方位角聚类下，约束每个地震台站下方的一维地震速度结构。反演输入数据包括：聚类叠加接收函数（RFs）、Rayleigh 波的相速度频散曲线和垂直/水平位移比（ZH）。
</div>

反演算法为马尔可夫链蒙特卡洛（MCMC），通过最小化下面的目标函数，搜索最佳拟合的 ${\text{V}}_{\text{s}}$ 模型：

$$
S_{\text{joint}}(m) = \alpha S_{\text{RF}}(m) + \beta S_{\text{PV}}(m) + \gamma S_{\text{ZH}}(m) + \omega S_{\text{SM}}(m)
$$

$S_{\text{SM}}$ 是模型平滑项，用于惩罚在深度小于 10km 或大于 (${\text{d}}_{\text{moho}}$ - 10) km 处出现的局部低速区，并以 0.01 ${\text{s}}^{-1}$ 进行归一化。

根据 RF 中是否存在 Pls 震相，采用两种不同的模型参数化方案：
- 无 Pls 震相：模型包括三层：浅层沉积、结晶地壳、上地幔顶部；
- 有 Pls 震相：在结晶地壳中加入一个顶部界面清晰的低速带（LVZ）。

<div class="abs-b mx-10 mb-10 text-sm opacity-50 flex flex-row gap-2">
<div>*</div>
<div>
Xiao, X. et al. Shallow seismic structure beneath the continental China revealed by P-wave polarization, Rayleigh wave ellipticity and receiver function. Geophys J. Int 225, 998–1019 (2021).
</div>
</div>

---

# Presence, absence and features of LVZs

反演得到的 ${\text{V}}_{\text{s}}$ 结构可根据地壳中 LVZ 的特征分为三类：LVZ-free、LVZ-smooth、LVZ-sharp。

<div>
LVZ-free 表示地壳中不存在 LVZ；LVZ-smooth 表示存在 LVZ，但其顶部边界为平滑过渡；LVZ-sharp 表示存在 LVZ，且其顶部为明显的速度突变界面。
</div>

<div class='mt-3'>
(a)、(c)、(e) 是三类结构的地壳剖面。(b)、(d)、(f) 是三类结构对应的三种地震数据的反演结果，不确定度用蓝色曲线包围的区域标记，不同周期的相速度和 ZH 比的不确定度分别用蓝点和垂直条表示。
</div>
<div class='mx-5 mt-5'>
<img border="rounded" src="/fig2.png">
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #2eafc0ff 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

<div>
在高原外围区域，几乎所有地壳剖面都为 “无 LVZ” 型，包括：扬子克拉通西部、塔里木块体、祁连块体东部、滇西块体和滇南块体（下图）。
</div>

<div class='mt-2'>
“平滑 LVZ” 型剖面主要集中在高原东南缘，包括：川滇块体南部及其南侧、扬子克拉通西部、滇西和滇南块体北部（下图中橙色阴影区），在川滇块体北部、柴达木块体东部及其周边也有零星分布。
</div>

<div class='mx-60 mt-2'>
<img border="rounded" src="/fig3_a.png">
</div>

---

<div>
“尖锐 LVZ” 型剖面广泛分布于高原内部及其东部边缘，包括：羌塘块体中东部、松潘-甘孜块体中东部、柴达木块体中东部、祁连块体东部、川滇块体及其周边（下左图中黑色阴影区）。这些 LVZ 的顶部深度介于 15–50 km之间，其中羌塘和拉萨块体较深（大于 40 km），高原北部和东部边缘较浅（小于 26 km）（下右图）。
</div>
<div class='mx-10 mt-5 grid grid-cols-2 gap-8'>
  <img border="rounded" src="/fig3_a.png">
  <img border="rounded" src="/sup_fig7.png">
</div>

---

## The LVZs are attributed to partial melting

LVZ 不太可能是由以下机制单独引起的：

<div>
1. 单纯升温：
温度升高无法解释 LVZ 顶部尖锐的速度突变，因为热量会通过热扩散在深度上平滑分布；同时，V<sub>s</sub> 降低至小于 3.40 km/s 需要温度升高至 1000°C 以上，足以引发部分熔融，而非单纯升温。
</div>
<div class='mt-5'>
2. 固态岩石成分变化：
无法解释东南缘 LVZ 顶部的平滑速度结构；同时，即使在高原中地壳的典型温压条件下（30 km 深度，770°C，1000 MPa），已知变质岩或火成岩的最低 V<sub>s</sub> 约为 3.47 km/s，也无法解释观测到的小于 3.40 km/s。
</div>
<div class='mt-5'>
3. 含水流体：
岩石学研究表明，中-下地壳的流体含量最多仅为 0.1%，不足以解释 LVZ 中观测到的速度降低和<Link to="2" title="大地电磁特性"/>；此外，流体对 V<sub>p</sub>/V<sub>s</sub> 比值影响很小，也无法解释部分地区观测到的地壳 V<sub>p</sub>/V<sub>s</sub> 升高。
</div>
<div class='mt-5'>
因此，LVZ 最可能的成因是部分熔融。部分熔融不仅能解释 V<sub>s</sub> 的降低幅度，也能解释 LVZ 顶部速度结构的尖锐性。值得注意的是，LVZ 通常<Link to="10" title="未延伸至莫霍面"/>，这可能表明部分熔融更倾向于发生在中地壳，或暗示深地壳底部存在变质过程。
</div>

---

## Estimation of melt fraction

<div class='mt-5'>
基于 LVZ 内 V<sub>s</sub>（V<sub>s</sub> , melt）与无熔融状态下 V<sub>s</sub>（V<sub>s</sub> , ref）的比值，并结合 Watanabe 提出的理论关系<span style="color: #00f">*</span>，估算 LVZ 中的熔体体积分数。估算结果显示，LVZ 中最大熔体含量为 1–10%，其中 87% 的区域集中在 2–8% 之间。
</div>

<div class='flex flex-row gap-5'>

<div class='mt-3'>
以下四个区域的最大熔体含量较高（>4%）：

R1：羌塘块体腹地及拉萨块体东部

R2：松潘-甘孜块体东部（靠近龙门山断裂西侧）

R3：东昆仑断裂周边，包括松潘-甘孜块体东北部与柴达木块体东部

R4：海原断裂附近
<div>
这些区域要么靠近主要断裂带（R2–R4），要么位于地壳最厚区域（R1），或被认为在三叠纪岩石圈拆沉后曾有热地幔物质上涌<span style="color: #00f">**</span>。
</div>

</div>

<div class='w-2/3'>
<img border="rounded" src="/fig3_b.png">
</div>
</div>

<div class="abs-b mx-10 mb-5 text-sm opacity-50">
<div class='flex flex-row gap-'>
<div>*</div>
<div>
Watanabe, T. Effects of water and melt on seismic velocities and
their application to characterization of seismic re ectors. Geophys
Res Lett. 20, 2933–2936 (1993).
</div>
</div>
<div class='flex flex-row gap-2'>
<div>**</div>
<div>
Zhang, H. et al. A-type granite and adakitic magmatism association
in Songpan–Garze fold belt, eastern Tibetan Plateau: Implication for
lithospheric delamination. Lithos 97, 323–335 (2007).
</div>
</div>
</div>

---

## Three stages of plateau evolution

通过联合分析 LVZ 的分布与特征、地表高程和莫霍面深度，我们识别出高原现今存在的三个演化阶段区域：

1. 前响应（Pre-response stage）：中地壳形成年轻熔融区，地表无明显变化；
2. 第一响应（First stage of response）：熔融区成熟，莫霍面加深，地表轻微隆升；
3. 最终响应（Last stage of response）：地表大规模隆升，形成现今高原主体。

<div class='mx-35'>
<img border="rounded" src="/fig4.png">
</div>

---

# Discussion

### I. Mid-crustal flow is a major mechanism for the uplift and crustal thickening of the Plateau.

<div class='mt-5'>
青藏高原内部普遍存在的地壳低速带（LVZ），以及高原外部几乎完全缺失 LVZ 的现象，表明<span class="highlight">中地壳流动是高原隆升与地壳增厚的主要机制</span>。根据实验数据建立的熔体-粘度关系<span style="color: #00f">*</span>，我们估算的熔体含量足以显著降低岩石粘度，从而在中地壳形成可流动的低速层，这一结论也得到了数值模拟的支持<span style="color: #00f">**</span>。
</div>
<div class='mt-5'>
LVZ顶部界面的深度从高原内部向边缘逐渐变浅<Link to="12" title="从高原内部向边缘逐渐变浅"/>，这可能反映了中地壳流动通道上方地壳的缩短程度不同，或高原内部存在横向热结构和成分差异。
</div>
<div class='mt-5'>
此外，高熔体含量区域（<Link to="14" title="R1–R4"/>）的空间分布表明，除了地壳放射性产热外，主要断裂带的摩擦生热以及深部热地幔的上涌也可能是地壳熔融的重要热源。
</div>

<div class="abs-b mx-10 mb-5 text-sm opacity-50">
<div class='flex flex-row gap-4'>
<div>*</div>
<div>
Rosenberg, C. L. & Handy, M. R. Experimental deformation of par-
tially melted granite revisited: implications for the continental crust.
J. Metamorph. Geol. 23, 19–28 (2005).
</div>
</div>
<div class='flex flex-row gap-2'>
<div>**</div>
<div>
Beaumont, C., Jamieson, R. A., Nguyen, M. H. & Medvedev, S.
Crustal channel flows: 1. Numerical models with applications to the
tectonics of the Himalayan-Tibetan orogen. J. Geophys. Res.: Solid
Earth 109 (2004).
</div>
</div>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #2eafc0ff 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
.highlight {
  background: linear-gradient(to top, #ffeb3b 20%, transparent 50%);
  padding: 0 0.2em;
}
</style>

---

### II. Sharpness of the top of LVZ serves as an indicator of the time period of partial melt.

<div class='mt-3'>
<span class="highlight">LVZ 顶部界面的尖锐程度可作为部分熔融持续时间的指标</span>。
</div>
<div class='mt-3 mb-2'>
数值模拟表明，在热而厚的地壳中，熔体可通过孔隙以每年毫米至厘米的速度垂直迁移，孔隙间距约为 1mm 或更大。这种垂直渗流由熔体与围岩的密度差驱动，并可独立于中-下地壳的水平流动而发生。随着时间推移，渗流的熔体及富集矿物成分会在熔融区顶部积累，形成明显的地震速度突变界面，即“尖锐 LVZ” （LVZ-sharp）。
</div>

<div class='mx-30'>
<img border="rounded" src="/fig3_c.png">
</div>

“尖锐 LVZ”区 → 中地壳存在成熟、发育良好的部分熔融区；“平滑 LVZ”区 → 中地壳存在年轻、尚未充分发展的部分熔融区。

<style>
.highlight {
  background: linear-gradient(to top, #ffeb3b 20%, transparent 50%);
  padding: 0 0.2em;
}
</style>

---

### III. The surface responses of the Tibetan Plateau may not necessarily occur in synchrony with the dynamical stages inside the crust.

<div class='flex flex-row gap-3 mt-5'>

<div class='grid grid-cols gap-4'>
高原对中地壳流动的三种不同响应阶段：
<div>
1. 前响应阶段（Pre-response stage）：中-下地壳形成年轻熔融区，地表几乎无隆升，莫霍面未明显加深；
</div>
<div>
2. 第一响应阶段（First stage of response）：熔融区成熟，中地壳流动导致莫霍面加深，但地表仍无大规模隆升；
</div>
<div>
3. 最终响应阶段（Last stage of response）：地表发生大规模隆升，形成现今高原主体。
</div>
<div>
关键结论：<span class="highlight">地表响应不一定与地壳内部动力学阶段同步</span>。
</div>
</div>

<div class='w-[90%] mt-10'>
<img border="rounded" src="/fig4_b.png">
</div>
</div>

<div class='mt-5'>
同一地壳动力学阶段可能对应多种地表响应；相似的地表响应也可能出现在不同地壳演化阶段；某些阶段甚至可能完全没有地表响应。
</div>

<style>
.highlight {
  background: linear-gradient(to top, #ffeb3b 20%, transparent 50%);
  padding: 0 0.2em;
}
</style>

---

### IV. Re-interpretation of geological records.

<div class='grid grid-cols gap-4 my-4'>
<div>
以往对高原地表地质过程的研究已提出了多种演化阶段。将这些发现置于三阶段模型中，可以发现：
</div>
<div>
1. 大多数地表地质过程发生在高原演化的最终阶段；
</div>
<div>
2. 地表响应在时间和空间上具有复杂性；
</div>
<div>
3. 在前响应和第一响应阶段，尽管地表地形未明显变化，但仍可能存在其他类型的地表响应（如断层活动、岩浆侵入等），只是尚未被识别或关联。
</div>
</div>

### V. Significance and prospects of the model.

<div class='grid grid-cols gap-4 my-4'>
<div>
本研究提出的三阶段演化模型为今后研究大陆高原演化机制和古高原历史提供了独特参考。现今青藏高原所展现的三阶段空间分布、地震特征与动力学响应，将对未来的地球动力学模型构成重要约束。
</div>
<div>
此外，这三个阶段也可作为解释高原地质记录的新框架，帮助我们更好地理解高原的演化历史。这种三阶段演化模式也可能存在于：
</div>
<div>
青藏高原西部（目前地震覆盖不足）；其他大陆碰撞造山带（如安第斯、阿尔卑斯等）。
</div>
</div>

---
layout: center
class: text-center
---

# Thank you | Questions are welcome (if I know the answer)

<PoweredBySlidev mt-10 />

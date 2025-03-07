---
description: （以压缩硬铅为例）
---

# CTI中压力室的AE自动化方案

_<mark style="color:red;background-color:orange;">**CTI 中压力室是合成压缩硬铅的唯一途径，而压缩硬铅是后期大量需求的材料之一。由于压力室特殊的机制，很多合成分配手段难以让压力室全速运行，从而产生一种压力室合成速度慢的假象。**</mark>_

_**如图所示，这是一个AE自动化压力室的装置（在CTI外的环境同样适用）；**_

<figure><img src="../.gitbook/assets/屏幕截图 2025-03-03 221216.png" alt=""><figcaption></figcaption></figure>

_<mark style="color:red;background-color:orange;">**它的基本原理是子网合成：右侧的存储总线形成了一个网络，这个网络的存储是压力室接口。当样板供应器将物品通过ME接口送进这个网络时，物品会被直接分配进压力室接口。**</mark>_

_<mark style="color:red;background-color:orange;">**合成完的物品通过另一个压力室接口返回样板供应器（图中未出现）。**</mark>_

_<mark style="color:red;background-color:orange;">**得益于AE的一个特性：当样板供应器与me接口相连时，它会把me接口所在网络视为容器，而非me接口，所以原料直接进入压力室接口，就不会出现卡合成（即只有硬铅板进入压力室而彩钢板不进压力室的情况）。**</mark>_

_<mark style="color:red;background-color:orange;">**压力室接口每1秒钟与压力室传输一次物品，所以这里为了提高压力室接口的效率还要使用一个叫多倍样板的小技巧，即样板写多份原料，让AE一次性向压力室接口里发送多份原料，使压力室接口每次传输都能传一组物品，最大化效率。**</mark>_

<figure><img src="../.gitbook/assets/屏幕截图 2025-03-03 221339.png" alt=""><figcaption></figcaption></figure>

_<mark style="color:red;background-color:orange;">**这之后合成效率就只与压缩空气供应有关了。那么如何高速获得大量压缩空气呢？**</mark>_



<figure><img src="../.gitbook/assets/屏幕截图 2025-03-03 221430.png" alt=""><figcaption></figcaption></figure>

_<mark style="color:red;background-color:orange;">**是的，没错，是手摇压缩机。**</mark>_

_<mark style="color:red;background-color:orange;">**CTI中在木星上手摇压缩机能无限产生4.9bar的压力，对于合成压缩硬铅而言肯定是足够的。如图所示，往压力室上贴9个手摇压缩机就能持续进行16倍样板合成，此时每秒就能合成256个压缩硬铅，轻轻松松合成几万个压缩硬铅。**</mark>_

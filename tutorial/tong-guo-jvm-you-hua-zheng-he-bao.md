# 通过jvm优化整合包

## _1.jvm是什么？_

_JVM 是 <mark style="color:red;">**Java Virtual Machine**</mark> 的缩写，它是一个虚构出来的计算机，一种规范。通过在实际的计算机上仿真模拟各类计算机功能实现···_

_好，其实抛开这么专业的句子不说，就知道 JVM 其实就类似于一台小电脑运行在 windows 或者 linux 这些操作系统环境下即可。它直接和操作系统进行交互，与硬件不直接交互，而操作系统可以帮我们完成和硬件进行交互的工作。_

_minecraft也是运行在JVM中的程序，那么我们就可以通过添加JVM参数来优化minecraft。_

***

### 2.JVM调优

_JVM调优听起来很高大上，但是要认识到，JVM调优应该是Java性能优化的最后一颗子弹。_

_JVM调优是一个关键的过程，涉及到调整Java虚拟机的配置以提升Java应用程序的性能。这包括优化堆内存设置、选择合适的垃圾收集器以及调整其他性能相关的参数。合理的调优可以显著提高应用的响应速度和吞吐量，优化资源利用，并增强稳定性。_

_JVM调优的重要性_

_JVM调优的目的是为了提高性能，优化资源利用，并增强应用的稳定性。通过调整JVM的配置，可以使应用更高效地利用系统资源，减少资源浪费，并避免内存泄漏和崩溃，确保应用的稳定运行。_

***

## 如何为MC添加jvm参数

以HMCL为例

{% hint style="danger" %}
q
{% endhint %}

_在版本管理中下拉找到<mark style="color:red;">**编辑高级设置（图1）。**</mark>_

<figure><img src="../.gitbook/assets/屏幕截图 2025-03-08 141814.png" alt=""><figcaption><p>图1</p></figcaption></figure>

打开编辑高级设置，下拉找&#x5230;_<mark style="color:red;">**java虚拟机设置**</mark>_

<figure><img src="../.gitbook/assets/屏幕截图 2025-03-08 142145.png" alt=""><figcaption><p>图2</p></figcaption></figure>

_<mark style="color:red;">**在java虚拟机参数一栏添加JVM参数 ，下拉。**</mark>_

<figure><img src="../.gitbook/assets/屏幕截图 2025-03-08 142451.png" alt=""><figcaption></figcaption></figure>

勾选不添加默认的JVM参数，退出即完成了添加。


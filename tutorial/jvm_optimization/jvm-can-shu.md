# JVM参数

## _1.常用参数_

```sh
-Xms4096M: 设置 JVM 初始内存分配为 4096MB（4GB）。
-Xmx4096M: 设置 JVM 最大内存分配为 4096MB（4GB）。
```

本参数是jvm的头参数，用于分配java应用使用内存的大小，可以根据自己电脑大小自行调整。

{% hint style="warning" %}
_<mark style="color:orange;">**如果勾选了不添加默认jvm，必须要添加此参数**</mark>_
{% endhint %}

{% hint style="danger" %}
_<mark style="color:red;">**xms xmx不能分配电脑最大内存，必须要给系统留10%-20%用于内存交换，否则会导致卡顿和崩溃**</mark>_
{% endhint %}

```powershell
// 垃圾回收器设置
-XX:+UseG1GC: 使用 G1GC 垃圾回收器，适用于大内存堆和低延迟要求的场景。
-XX:+UnlockExperimentalVMOptions: 解锁实验性 VM 选项，允许使用一些未正式发布的参数。
```

```powershell
//G1GC 特定参数
-XX:+ParallelRefProcEnabled: 使用多个线程处理引用，提高垃圾回收效率。
-XX:MaxGCPauseMillis=200: 设置最大垃圾回收暂停时间为 200 毫秒，减少卡顿。
-XX:+DisableExplicitGC: 禁用显式垃圾回收调用，防止插件触发全量垃圾回收导致卡顿。
-XX:+AlwaysPreTouch: 预先分配和触摸所有内存页面，提高内存访问效率。
-XX:G1NewSizePercent=30: 设置新生代最小占堆的 30%。
-XX:G1MaxNewSizePercent=40: 设置新生代最大占堆的 40%。
-XX:G1HeapRegionSize=8M: 设置每个堆区域的大小为 8MB，减少巨大对象分配。
-XX:G1ReservePercent=20: 设置保留 20% 的堆空间用于垃圾回收时的临时分配。
-XX:G1HeapWastePercent=5: 设置允许浪费的堆空间百分比为 5%。
-XX:G1MixedGCCountTarget=4: 设置混合垃圾回收的次数目标为 4 次。
-XX:InitiatingHeapOccupancyPercent=15: 设置当堆占用达到 15% 时开始垃圾回收。
-XX:G1MixedGCLiveThresholdPercent=90: 设置当老年代区域存活对象比例超过 90% 时，将其纳入混合垃圾回收。
-XX:G1RSetUpdatingPauseTimePercent=5: 设置用于更新 RSet 的暂停时间百分比为 5%。
-XX:SurvivorRatio=32: 设置新生代中 Eden 区与 Survivor 区的比例为 32:1。
-XX:MaxTenuringThreshold=1: 设置对象在新生代中存活的最大次数为 1，减少老年代污染。
-XX:+PerfDisableSharedMem: 禁用性能数据的共享内存，避免潜在的性能问题。
```

完整jvm参数（通用）

```sh
-Xms4096M -Xmx4096M -XX:+UseG1GC -XX:+UnlockExperimentalVMOptions -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 
```

-Xms4096M -Xmx4096M -XX:+UseG1GC -XX:+UnlockExperimentalVMOptions -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1

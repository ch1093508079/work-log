---
layout: post
title:  "IT知识与资讯"
date:   2021-09-21 19:20:23 +0800
categories: jekyll update
---
# 电脑硬件层面的运维

## [以前是这样"修电脑"的](https://www.bilibili.com/video/BV11q4y1Z7mp?spm_id_from=333.999.0.0)
1. 键盘不能切换大小写，大概率是内存的问题：重新插拔内存，做清洁
1. 重新插拔主板的电池
1. 还不行就可能是CPU的问题

## [打包电脑得这样来](https://www.bilibili.com/medialist/play/ml1350003812/BV1tf4y1H7s4)
1. 有大显卡就先取显卡
1. 把泡沫填满机箱空间，围住风扇，盖上机箱
1. 在机箱外部做防摔缓冲

## [13款最新最全CPU大横评测试，看完就知道2021年怎么配电脑](https://www.bilibili.com/medialist/play/ml1350003812/BV1pL4y1Y7FP)
本视频所有的测试都针对游戏玩家。
省流助手:5600x最合适，预算不够3600，预算太多5950x

## [那些品牌电脑是如何降低成本的](https://www.bilibili.com/medialist/play/ml1350003812/BV1JV411x79d)
区分真正的品牌机与有牌子的京东淘宝组装机
1. 真正的品牌机没有一处插槽是多余的
1. 真正的品牌机的电源阉割过，难以替换配件，无法DIY
1. 真正的品牌机把售后的价格加到机器上了
下期视频再聊有牌子的京东淘宝组装机

## [【科普】正确认识CPU，该如何选择，影响CPU性能的主要参数是什么](https://www.bilibili.com/medialist/play/ml1350003812/BV1Hh411W7eU)
品牌台式机性价比普遍不高
### 了解 INTEL CPU 产品线
1. 低端		赛扬	CELERON
1. 中低端	奔腾	PENTIUM
1. 高端		酷睿	CORE
1. 服务器	志强	XEON
+ CORE I7-10650G7表示10代酷睿，SUK为650，G7表示全新集成显卡
+ 后缀的具体含义见视频3:40

### 了解 AMD CPU 产品线
1. AMD RYZEN 9 5900X
1. AMD RYZEN 7 5900X
1. AMD RYZEN 5 5900X
1. AMD RYZEN 3 5900X
+ 后缀的具体含义见视频5:10

### 其他重要参数
1. 主频
1. 核心和线程数
1. 架构
1. 缓存

## [【科普】主板该怎么选？主板的工作原理，以及主板插槽的简单认识](https://www.bilibili.com/video/BV1RM4y1G7WP)
1. 电源到主板的接口一般是24针，给CPU的是4针或8针的接口
1. 通过并联一对疙瘩为CPU供电，一对疙瘩就是一项供电。例如主板的供电项数是 8+2 就代表着8项供电给CPU，2项给内存
1. intel平台的针脚在主板上
1. 硬盘接口有SATA、M.2、IDE（已淘汰）；其中M.2又有SATA协议和NVME协议
1. PCI4.0插槽一般给显卡
1. 南桥芯片——输入输出控制器
+ 直接和CPU对接的有内存和PCIE-X16显卡插槽
+ 对于实时通信要求不高的给南桥，也就是平时大家说的主办芯片组
1. 电池

## [买不起NAS，一百元解决存储问题，SSK硬盘底座开箱](https://www.bilibili.com/medialist/play/ml1350003812/BV1uq4y1S7y7)
评论区：
1. 这种商品的定位应该是利用废旧机械硬盘。或者给设备做冷备的。长期运行着不靠谱，散热应该hold不住
1. 要是像海康h99那样到还能考虑，当个轻度局域网nas，很快的。一般硬盘温度都不会太高
1. 主要是太多的硬盘底座，现在的供电都不满足于现在的3.5寸硬盘需求。最好选一个方方正正的硬盘底座，不然容易倒容易导致硬盘损坏。

## [绿联硬盘拓展坞为啥叫升天座啊？绿联拓展坞与希捷硬盘盒对比评测](https://www.bilibili.com/medialist/play/ml1350003812/BV13P4y1h7yA)
评论区：第三方的问题主要是芯片方案不行，都是直接采用的一些小公司的芯片方案，除了便宜就没有其它优点，根本没有安全性稳定性上的保障。最常见的问题就是因没有弹出和接触不良导致的热插拔，第三方硬盘底座就容易导致文件系统损坏，只有格式化后才能继续使用，而移动硬盘盒就基本不会出现这个问题。

## [值得入手的个人轻量级NAS，海康威视H99 PRO使用体验](https://www.bilibili.com/medialist/play/ml1350003812/BV1ZQ4y1h7Fe)
+ 单盘位，是插入式的底座；有手机客户端和win10客户端
+ 300价位，外网访问卡顿

# 软件与操作系统层面的运维
## [如何用Dism++删除Windows预装软件](https://www.bilibili.com/medialist/play/ml1338075412/BV1r3411q71B)

## [SpaceSniffer可视化分析磁盘空间](https://www.bilibili.com/medialist/play/ml1338075412/BV1VL411t7MS)
评论区：网上说wiztree分析速度会快一点

## [5款良心UWP应用推荐](https://www.bilibili.com/medialist/play/ml1338075412/BV1cf4y1N7UC)
C盘清理工具-清理君Lite：可视化展示C盘空间布局

## [好用的老版本迅雷](https://www.bilibili.com/video/BV1YT4y1E7PA?spm_id_from=333.824.b_765f64657363.3)

## [【装机教程】沙雕看了都能学会的驱动安装教程（装驱动教程，手动安装驱动）](https://www.bilibili.com/medialist/play/ml1350003812/BV1Fy4y1D7ZJ)
一般用户只需要手动安装以下驱动：主板芯片组、网卡、声卡、显卡和外设
1. N卡的驱动类型：不玩游戏选择Studio，玩游戏选Game Ready
1. I卡要从CPU型号看出是第几代CPU

## [电脑系统版本对电脑性能的影响](https://www.bilibili.com/medialist/play/ml1338075412/BV1eq4y1K7X4)
1. 家庭版
1. 教育版
1. 专业版
评论区：这些win系统的版本，只要是同一内核，区别只在于附加功能组件不同而已，相当于你买的同一型号的车，高配和普通版，多两个真皮坐垫和一套音响系统并不会影响车辆的动力。

## [淘汰的老旧电脑能干嘛](https://www.bilibili.com/medialist/play/ml1350003812/BV1UK4y1L78N)
1. 远程控制挂机下载，共享文件夹
1. 做路由器
1. 变身NAS：推荐万由UNAS
1. 装linux，推荐Ubuntu文档丰富适合新手
+ 搭建个人网站
+ 装安卓
+ Chrome OS
+ 装OpenELEC变身Kodi媒体中心
+ Batocera游戏模拟器
评论区：讲半天还是当服务器。这没啥，其实无非就是最简liunx加云服务，确实对性能要求不高，但是我觉得也不会太好用。与其这么用，还不如直接当跳板机用，纯liunx加nginx

# 网络设备

## [网络各厂家之间的关系链](https://www.bilibili.com/medialist/play/ml1350003812/BV1L64y1Y7d1)
1. 华为仿思科，命令行不同但内核一样
1. 锐捷配置命令与思科一样。主要做校园网，无线做得不错
1. 学了华为以后H3C就顺水推舟了
评论区：
1. 思科认证是真的很不错，不过因为国产化要求，思科产品退出中国市场得速度会大大加快
+ 但是思科的技术体系是最全面的，一家学会全产商不愁

## [通过h3c交换机irf堆叠](https://www.bilibili.com/medialist/play/ml1338075412/BV1TU4y1N7EL)
```h3c
# 第一台交换机
interface range Ten-Gigabitthernet 1/0/47 to Ten-Gigabitthernet 1/0/48
	shutdown
	irf member 1 priority 32
irf-port 1/1
	port group interface Ten-Gigabitthernet 1/0/47
	port group interface Ten-Gigabitthernet 1/0/48
	quit
irf-port-configuration active
interface range Ten-Gigabitthernet 1/0/47 to Ten-Gigabitthernet 1/0/48
	undo shutdown
	quit

# 第二台交换机
disp int brief
irf member 1 renumber 2

save


quit
reboot

interface range Ten-Gigabitthernet 2/0/47 to Ten-Gigabitthernet 2/0/48
	shutdown
	irf member 2 priority 1
irf-port 2/2
	port group interface Ten-Gigabitthernet 2/0/47
	port group interface Ten-Gigabitthernet 2/0/48
	quit
irf-port-configuration active
interface range Ten-Gigabitthernet 2/0/47 to Ten-Gigabitthernet 2/0/48
	undo shutdown
	quit

disp irf
```

## []()
## []()

# 专门扣图的应用
## [绝对好用的免费抠图网站，确定不试一试？](https://www.bilibili.com/medialist/play/ml1338075412/BV1ey4y1G7Bp)
## []()

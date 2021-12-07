---
layout: post
title:  "nas与存储专项笔记"
date:   2021-08-19 15:50:28 +0800
categories: jekyll update
---



### 硬盘
关于颗粒：MLC很贵性价比不高，首选TLC，别碰QLC
1. 固态硬盘
+ SATA接口：400~560M/s
+ M.2接口
	+ SATA通道：退化为SATA接口
	+ PCIE通道（NVME协议）
		+ PCIE4.0：5600~7000MB/s
		+ PCIE3.0 **最具性价比**
			+ 普通款：1500MB/s~2500MB/s
			+ 旗舰款：3000MB/s以上
1. 搭配建议
+ 固态放系统、软件、游戏
+ 机械当仓库

## [绿联硬盘拓展坞为啥叫升天座啊？绿联拓展坞与希捷硬盘盒对比评测](https://www.bilibili.com/medialist/play/ml1350003812/BV13P4y1h7yA)
评论区：第三方的问题主要是芯片方案不行，都是直接采用的一些小公司的芯片方案，除了便宜就没有其它优点，根本没有安全性稳定性上的保障。最常见的问题就是因没有弹出和接触不良导致的热插拔，第三方硬盘底座就容易导致文件系统损坏，只有格式化后才能继续使用，而移动硬盘盒就基本不会出现这个问题。

## [如何科学地启动硬盘](https://www.bilibili.com/medialist/play/ml1350003812/BV1z7411T7dY)
机械硬盘由电机带动，电机的特性是启动电流大于标称电流
1. 常见的消费级主板，只能连接6块SATA硬盘，同时启动的峰值电流也不过12V15A、5V3A，也就是接近200W，配个300W的电源已经够用。4盘位的蜗牛大军也不必担心250W的FLEX或小1U电源功率不足
1. 挂在SAS控制器上的硬盘，会受控制排队起转，每2秒一个避免扎堆。SAS自检+24块硬盘启动就要1分钟。

## [值得入手的个人轻量级NAS，海康威视H99 PRO使用体验](https://www.bilibili.com/medialist/play/ml1350003812/BV1ZQ4y1h7Fe)
+ 单盘位，是插入式的底座；有手机客户端和win10客户端
+ 300价位，外网访问卡顿

## [买不起NAS，一百元解决存储问题，SSK硬盘底座开箱](https://www.bilibili.com/medialist/play/ml1350003812/BV1uq4y1S7y7)
评论区：
1. 这种商品的定位应该是利用废旧机械硬盘。或者给设备做冷备的。长期运行着不靠谱，散热应该hold不住
1. 要是像海康h99那样到还能考虑，当个轻度局域网nas，很快的。一般硬盘温度都不会太高
1. 主要是太多的硬盘底座，现在的供电都不满足于现在的3.5寸硬盘需求。最好选一个方方正正的硬盘底座，不然容易倒容易导致硬盘损坏。

## [NAS 用什么硬盘](https://www.bilibili.com/medialist/play/watchlater/BV1C44y1Y74K)
1. 西数红盘（CMR硬盘，不是垂直盘）
	+ PLUS：100万小时的MTBF三年质保
	+ PRO：100万小时，5年质保
1. 希捷，支持多盘位RAID优化，在震动时可快速恢复
	+ Exos X 氦气全密封

## [紫盘、监控盘究竟能不能放在普通电脑和NAS上当做普通数据盘使用？](https://www.bilibili.com/medialist/play/watchlater/BV1944y1h77r)
1. 紫盘不是没有纠错功能，而是多了一个“可选择关闭纠错功能”的功能
1. 紫盘的设计通电时间是7×24小时，而蓝盘是5×8小时
1. 紫盘一般采用传统CMR磁记录方式
1. 紫盘价格便宜，预算充足还是推荐NAS专用盘

## [带USB路由器启动NAS](https://www.bilibili.com/video/BV1Ug411c7eJ)
进入管理页面->工具箱->路由存储

买群晖nas前
---
买群晖nas后

## [向领导介绍raid基础知识](https://www.bilibili.com/medialist/play/ml1401654412/BV1VJ411s7T5?oid=80240051&otype=2)

## [搭载OpenWRT的4G随身路由器，还可当轻量NAS，GL XE300随身WIFI体验](https://www.bilibili.com/video/BV1JZ4y197BH)

## [号称100％不宕机的百万存储开箱，配置到底如何？](https://www.bilibili.com/medialist/play/watchlater/BV1X34y1X7t6)

## [【大卫装机】1000元组10T容量高性能NAS，SAS硬盘赛高](https://www.bilibili.com/medialist/play/watchlater/BV1iP4y1V7oi)

## []()

## []()

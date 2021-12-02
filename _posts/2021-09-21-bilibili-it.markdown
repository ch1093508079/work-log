---
layout: post
title:  "IT知识与资讯"
date:   2021-09-21 19:20:23 +0800
categories: jekyll update
---


# 电脑硬件层面的运维

## [NAS 用什么硬盘](https://www.bilibili.com/medialist/play/watchlater/BV1C44y1Y74K)
1. 西数红盘（CMR硬盘，不是垂直盘）
	+ PLUS：100万小时的MTBF三年质保
	+ PRO：100万小时，5年质保
1. 希捷，支持多盘位RAID优化，在震动时可快速恢复
	+ Exos X 氦气全密封

## [按电源键没反应怎么排查故障检修思路](https://www.bilibili.com/video/BV1ig411V7ip?spm_id_from=333.1007.top_right_bar_window_view_later.content.click)
所有电源都有触发线，就是绿线。
用万用表查电源

## [以前是这样"修电脑"的](https://www.bilibili.com/video/BV11q4y1Z7mp?spm_id_from=333.999.0.0)
1. 键盘不能切换大小写，大概率是内存的问题：重新插拔内存，做清洁
1. 重新插拔主板的电池
1. 还不行就可能是CPU的问题

## [打包电脑得这样来](https://www.bilibili.com/medialist/play/ml1350003812/BV1tf4y1H7s4)
1. 有大显卡就先取显卡
1. 把泡沫填满机箱空间，围住风扇，盖上机箱
1. 在机箱外部做防摔缓冲
博主注：使用中的电脑还要保护硬盘

## [那些品牌电脑是如何降低成本的](https://www.bilibili.com/medialist/play/ml1350003812/BV1JV411x79d)
区分真正的品牌机与有牌子的京东淘宝组装机
1. 真正的品牌机没有一处插槽是多余的
1. 真正的品牌机的电源阉割过，难以替换配件，无法DIY
1. 真正的品牌机把售后的价格加到机器上了
下期视频再聊有牌子的京东淘宝组装机

## [13款最新最全CPU大横评测试，看完就知道2021年怎么配电脑](https://www.bilibili.com/medialist/play/ml1350003812/BV1pL4y1Y7FP)
本视频所有的测试都针对游戏玩家。
省流助手:5600x最合适，预算不够3600，预算太多5950x

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
+ 直接和CPU对接的有：内存、PCIE-X16显卡插槽、非SATA的M.2硬盘、PS/2键鼠接口
+ 对于实时通信要求不高的给南桥，也就是平时大家说的主办芯片组
1. 纽扣电池
1. 外部接口
+ USB3.x中的Gen1和Gen2差别挺大的
+ VGA、DP和HDMI都是视频输出接口
1. 主板芯片对应的CPU见视频10:50，要避免不配套可咨询客服

## [一站式台式机DIY入门指南！游戏主机/生产力主机全攻略！](https://www.bilibili.com/medialist/play/ml1350003812/BV1k64y1h7QP)
前言跳过
+ [快科技显卡天梯图网址](https://www.mydrivers.com/zhuanti/tianti/gpu/)
+ [快科技桌面CPU天梯图网址](https://www.mydrivers.com/zhuanti/tianti/cpu/)
+ [秋刀鱼半藏显卡天梯图网址](https://tieba.baidu.com/p/6133450546?see_lz=1#135699450528l)
+ [秋刀鱼半藏cpu天梯图网址](https://tieba.baidu.com/p/5005825360)
+ [FCPPOWERUP极电魔方网址](https://www.fcpowerup.com/)

### 显卡
1. NVIDIA公卡供应慢
+ 每1~2年都会推出新的显卡核心
+ NVIDIA把显卡核心卖给AIC厂家（例如COLORFUL七彩虹）做出非公显卡
+ 其他条件相同时，旗舰版比丐版强5%
1. AMD情况也差不多
1. 光线追踪是尚未成熟的技术
+ NVIDIA在硬件层面做光线追踪
+ AMD在软件层面做光线追踪
1. 所有的生产力需求都建议N卡。需要明确你在生产什么
+ 平面设计软件PS、AI的硬件优先级：内存 > CPU > 显卡
+ 视频处理类软件PR、AE：内存 = CPU > 显卡1050Ti起步
+ 3D建模渲染类软件3ds、C4D、草图大师、工程渲染：内存 = CPU = 显卡

### CPU
重要参数
1. 核心数和线程数
+ 据intel和AMD的说法：超线程最多能提升20%~25%左右的性能
1. 频率
+ 基础频率
+ 加速频率：现在新手玩家没必要折腾超频
1. 不推荐intel的11代，游戏玩家不推荐AMD ZEN2
1. 游戏玩家选CPU的原则就是不拖显卡后退，对应表见视频21:00

### 主板
1. 普通消费级常见版型：ATX（大板）、MATX（中板和小板）、ITX（mini板）。
1. 一般而言板越大越豪华，板越小越低端。
1. intel和AMD每发布一代新U，都会随之发布新的芯片组。这是分割高中低档定位的手段

### 内存主要参数 容量 频率
1. 消费级DDR4内存的频率
+ 普通频率：2240Mhz、2666Mhz
+ 高频内存 >= 3200Mhz
+ 超过了3600Mhz后，再高对游戏提升很小
1. 注意事项
+ 尽量不要混用不同品牌、型号、容量、频率的内存
+ 能双通道不单通道
+ 能二不四：能两根16G就不要4根8G

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

### 电源
美国能源署出台的降低能耗的标准——80PLUS认证只能体现转换率优势。市面标称的功率都是转换后的功率

模组电源
1. 直出电源：中低端，所有线材都一起出来
1. 全模组电源：所有线都可以插拔，用几根插几根
1. 半模组电源：只有主板的24根线焊死，其余可插拔

根据吃电大户——CPU和显卡——来选。推荐高瓦数电源的主要原因：随着显卡规模越做越大，显卡的瞬时功耗的波动比官方宣传的要剧烈，顶不住时可能断电重启甚至烧毁

品牌型号怎么选，见视频41:20。在视频所述品牌里，遵循5毛一瓦起步、7~8毛一瓦为不错、1元一瓦为最佳且起码5年质保

### 散热器的选择很简单：能压住CPU
1. 风冷：安全性高，寿命长
+ 下压式
+ 塔式
1. 一体式水冷：虽然很少漏水单安全性依然差，寿命短
+ 120
+ 240
+ 280
+ 360

### 机箱
注意
1. 主板兼容性
1. 显卡兼容性
1. 散热器兼容性
1. 硬盘位数量
1. 机箱是否闷罐

## [散热硅脂选购涂抹指南](https://www.bilibili.com/video/BV1CQ4y1i7EK)
1. 视频1:04。除了利民和信越外，绝大多数硅脂采用画叉或九点法都能自行铺开。利民散热器附赠的TF7就很不错

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

## [如何科学地启动硬盘](https://www.bilibili.com/medialist/play/ml1350003812/BV1z7411T7dY)
机械硬盘由电机带动，电机的特性是启动电流大于标称电流
1. 常见的消费级主板，只能连接6块SATA硬盘，同时启动的峰值电流也不过12V15A、5V3A，也就是接近200W，配个300W的电源已经够用。4盘位的蜗牛大军也不必担心250W的FLEX或小1U电源功率不足
1. 挂在SAS控制器上的硬盘，会受控制排队起转，每2秒一个避免扎堆。SAS自检+24块硬盘启动就要1分钟。

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

## [带USB路由器启动NAS](https://www.bilibili.com/video/BV1Ug411c7eJ)
进入管理页面->工具箱->路由存储

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

# 影视听处理
## [绝对好用的免费抠图网站，确定不试一试？](https://www.bilibili.com/medialist/play/ml1338075412/BV1ey4y1G7Bp)
## [在线录屏好用吗](https://www.bilibili.com/video/BV1844y1v7b6)
## [2GB的视频压缩到80Mb？HandBrake最好用的免费视频压缩Win&Mac&Linux](https://www.bilibili.com/medialist/play/watchlater/BV1KL4y1q7zj)
## [【一键变清晰！】rick配音，超实用的位图转矢量图工具！](https://www.bilibili.com/medialist/play/watchlater/BV1jU4y1T7KB)
## [ffmpeg基础奠基](https://www.bilibili.com/medialist/play/watchlater/BV1EQ4y1S7KP)
1. ffprobe用于查看格式
1. 查看支持的编码器和解码器：`ffmpeg -encoders`和`ffmpeg -decoders`
1. `ffmpeg -h encoder=名称`查看编码器支持的参数和选项
1. 转码命令格式：`ffmpeg -i INPUT -c:v ENCODER OPTIONS -c:a ENCODER OPTIONS OUTPUT`。常用的如下
+ ffmpeg -i FLAWER.flv -c:c libx264 -c:a acc OUT.mp4
+ 未完，看到2:40

# 其他
1. 车子本身不具备检测机油寿命和品质的功能，保养提示是一个三角形的警告；如果是红色的阿拉丁神灯，那就要非常谨慎
1. 165HZ和60HZ显示器刷新率对比：没有好显卡就没必要超60Hz
1. 淘宝种类多，京东售后好但都加到价格上了，拼多多省了服务
1. 合规轮胎每月漏气0.7bar
1. 高德地图适合小路，但要小心它导你去帮忙探小路
1. 国内芯片价格高，树莓派约贵1倍
1. 省流：
+ 一般人达不到蓝光损害眼睛程度
+ 市面上的电子产品基本过滤蓝光
+ 真要买就去看国家标准
+ 灰灰的奶茶补充，阳光中的蓝光伤害较大  长期户外作业的需要防蓝光

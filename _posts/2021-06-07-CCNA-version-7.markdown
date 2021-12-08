---
layout: post
title:  "《CCNA学习指南（第七版）》读书笔记"
date:   2021-06-07 11:25:00 +0800
categories: book-note
---

# ch04 IOS和SDM

## IOS的用户界面
#### 连接到Cisco路由器
首选方式是通过控制台端口进行连接，一般是一个RJ-45的连接器（8针的模块）
#### 启动路由器
`Cisco 2811 (revision 49.46) with 249856K/12288K bytes of memory.`
上述启动信息中显示此路由器有256MB的RAM，下方显示239KB的NNVRAM和64MB的闪存
+ 239K bytes of **n**on-**v**olatile configuration memory.
+ 62720K bytes of **ATA CompactFlash** (Read/Write)

### 命令行接口（CLI）
#### 路由器模式概述
只有conf t命令经常使用。可是，如果你想强行修改你的running-config文件，但却又不想重新启动路由器，则使用命令con men和con net就会显得十分有效
#### 编辑和帮助功能
show history显示最近输入过的10条命令

### 路由器和交换机的管理配置
#### 主机名
通过hostname设置的路由器标识只在局部起作用。我们将在第14章中讨论PPP时介绍为认证而使用的主机名
#### 标志区
`banner motd #`可以设置对操作者给出一个信息
#### 设置口令
##### 启用加密口令
```
enable secret todd
```
##### 控制台口令
```
line console 0
login
password todd
```
##### Telnet口令
```
line vty 0 4
password todd
login
```
#### 接口描述
在接口配置模式下执行`description MESSAGE`将会在`sh run`和`sh int f0/0`中显示

### 路由器接口
#### 串行接口命令
+ `sh controllers s0/0/0`可以了解到路由器的串行接口是否连接有DCE电缆
+ `clock rate 1200`设置时钟频率为每秒1200**位**
+ `bandwidth 1200`设置度量为每秒1200**千位**，仅用于EIGRP和OSPF等协议计算开销，并不会影响数据通过链路的传送过程

### 查看、保存并擦除配置
+ `sh int f0/0`将给出硬件地址、逻辑地址和封装方式，以及发生冲突的统计信息
+ `sh ip interface`提供有关路由器接口的第3层配置的信息
+ `sh ip int brief`提供了包含有逻辑地址和状态的路由器接口的快速汇总
+ `sh protocols`查看每个接口上第1层和第2层的状态以及使用的IP地址
+ `sh controllers s0/0`显示关于物理接口自身的信息
在全局配置模式下使用show需要在前面加do

## Cisco的安全设备管理器（SDM）
要让你的主机可以使用SDM进行登录，必须首先对路由器进行配置
```
en
conf t
int f0/0
ip address 1.1.1.1 255.255.255.0
no shut
do ping 1.1.1.2
```
这样，你就只需打开一个浏览器，输入http://1.1.1.1，按给出的提示完成连接

在路由器上使用HTTPS需要更多的命令。在全局配置模式下执行
```
ip http server
ip http secure-server
ip http authentication local

username cisco privilege 15 password 0 cisco

line console 0
login local
exit
line vty 0 1180
privilege level 15
login local
transport input telnet
transport input telnet ssh
^Z
```

## 书面实验4
1. clockrate 64000
2. 如果在远程登录到某台路由器时得到“connection refused, password not set”，怎么取消口令输入提示？
```
line vty 0 4
no login
```
3. no shut
4. erace startup-config
5. 为控制台接口设置用户模式口令
```
line console 0
login
password todd
```
6. enable secret cisco
7. sh controllers s0/0/0
8. 查看终端历史记录的大小
+ 答案是：show terminal
9. 初始化路由器并使用当前的startup-config文件整个替换running-config文件
+ 答案是：reload
10. hostname Chicago


# ch05 管理Cisco互联网络

### 管理配置寄存器
### 备份和恢复Cisco IOS
### 备份和恢复Cisco配置
### 使用Cisco发现协议（CDP）
#### 获取CDP定时器和保持时间信息
+ `sh cdp`显示两个CDP全局参数信息
+ `cdp holdtime 180`配置CDP保持时间
+ `cdp timer 60`配置CDP定时器

#### 收集直连设备信息
CDP数据包不经过Cisco交换机
+ `sh cdp neighbors`显示有关直连设备的信息。
+ `sh cdp nei detail`显示详细信息，`sh cdp entry *`显示同样的信息
+ `sh cdp entry * protocols`告诉你每个直连邻居的IP地址
+ `sh cdp entry * version`只告诉你直连邻居的IOS版本

#### 收集接口流量信息
`sh cdp traffic`显示设备发送和接收CDP数据包数

#### 收集端口和接口信息
`sh cdp inter`显示路由器接口或交换机端口的CDP状态
+ 可以用`no cdp enable`关闭每个接口
+ 可以用`cdp enable`启动端口

### 使用Telnet
CDP不能收集到未和你的设备直连的路由器和交换机的信息。然而，可以使用Telnet应用程序连接到相邻设备上收集
#### 同时telnet到多台设备
输入exit可结束连接。然而，如果希望在和一台远程设备保持连接的同时还回到原来的路由器控制台上，可以按下Ctrl+Shift6组合键，再按X键
#### 检查Telnet连接
sh sessions
#### 检查Telnet用户
sh users
#### 关闭Telnet回话
+ 从远程设备结束会话：`exit`
+ 从本地设备结束会话：`disconnect 会话号`。其中会话号在`sh session`输出中的Conn列
+ 如果想结束通过Telnet和你的路由器建立了连接的设备的会话：`clear line 线路号`。其中线路号在`sh users`输出中的Line列。

#### 使用SDM telnet到路由器
单击“Tools（工具）”菜单，然后选择“Telnet”
### 解析主机名
有两种方法可以将主机名解析为IP地址，两种方法建立的主机表都可以用`sh hosts`查看。
1. 建立主机表
一个主机名最多指派8个IP地址。使用`ip host 主机名 tcp端口号 IP地址`建立主机表仅供本路由器提供名称解析
2. 使用DNS解析名称

```
conf t
ip domain-lookup
ip name-server 10.191.131.131
ip name-server 10.191.130.130
ip domain-name lammle.com

```
Cisco设备接收了一个无法理解的命令时，默认情况下它尝试通过DNS解析。可以再全局模式下使用`no ip domain-lookup`防止费时的DNS查找

### 检查网络连接并排除故障
#### debug命令
debug有非常高优先权，只能短时间作为故障排除工具使用，它会严重降低路由器的性能。
+ `debug all`显示各种路由器操作系统及其产生和接收的相关流量信息和错误信息
+ `no debug all`或`un all`取消上述诊断

`debug ip rip`显示路由器发送和接收RIP更新情况

在使用任何诊断命令前应当检查一下路由器的使用情况。如果路由器的CPU利用率已达到50%以上，就不适合使用`debug all`命令了，用`sh process`
#### `sh process`命令
`sh process`的输出中`CPU utilization for the last five seconds: 2%/0%`的第一个数据等于总利用率，第二个数据给出了由于中断运行时程序导致的利用率

## 书面实验5
1. copy flash: tftp:
2. copy start tftp:
3. reload
4. copy start run
5. show cdp ip
6. show cdp all
7. Ctrl Shift 6 X
8. show sessions
9. 
10. 


# ch10 安全

### 非军事区、防火墙和内网路由器
### 认识安全威胁
常见的攻击
1. 应用层攻击
1. Autorooters
1. 后门程序
1. 拒绝服务和分布式拒绝服务攻击
+ TCP SYN泛洪攻击
+ 死亡之ping攻击
+ 族群式泛洪攻击
+ Stacheldraht
1. IP欺骗
1. 中间人攻击
1. 网络侦查
1. 包嗅探
1. 口令攻击
1. 强暴攻击
1. 端口重定向攻击
1. 特洛伊木马攻击和病毒
1. 信任利用攻击

### 降低安全威胁
#### Cisco IOS防火墙
##### 基本和高级流量过滤

### 访问列表简介
访问列表主要有两种类型
1. 标准ACL：基于源IP地址，不区分WWW、Telnet、UDP等服务
1. 扩展ACL：可以测试源IP、目的IP、网络层报头中的协议字段、传输层端口号
命名ACL：可以是标准的也可以是扩展的

配置指南
1. 每个接口只能有1个入口访问列表和1个出口访问列表
1. 将更特殊的测试放在前面
1. 添加新条目时放到末尾
1. 编辑列表之前把它复制到一个文本编辑器中
1. 除非末尾有permit any，否则测试不通过的数据包将被丢弃
1. 先创建访问列表，然后将列表应用到一个接口
1. 访问列表设计为过滤通过路由器的流量，但不过滤路由器产生的流量
1. 将标准的访问列表尽可能放置在靠近目的地址的位置
1. 将扩展的访问列表尽可能放置在靠近源地址的位置

#### 使用ACL降低安全威胁

### 标准的访问列表
可以使用访问列表号1~99或1300~1999创建标准的访问列表。例如`access-list 10 deny host 172.16.30.2`
#### 通配符
有效的块大小：64、32、16、8、4
`172.16.16.0	0.0.3.255`匹配172.16.16.0~172.16.19.0
`172.16.16.0	0.0.7.255`匹配172.16.16.0~172.16.23.0
#### 标准访问列表示例
将访问列表应用到接口的指定方向
```
int e1
ip access-group 10 out
```
#### 控制VTY（Telnet）访问
对于有上百个接口的大型路由器，逐个接口创建扩展的IP访问列表很难。更好的办法是使用标准的IP访问列表控制访问VTY线路
```
conf t
accrss-list 50 permit 172.16.10.3
line vty 0 4
access-class 50 in
```

### 扩展的访问列表
扩展访问列表的号码范围时100~199和2000~2699
```
conf t
access-list 110 deny tcp any host 172.16.30.2 eq 23 log
accrss-list 110 permit ip any any
int e1
ip accrss-group 110 in
```

### 高级访问列表
#### 命名的ACL更容易识别
在全局配置模式下执行`ip access-list standard BlockSales`会进入命名acl配置模式
```
deny 172.16.40.0 0.0.0.255
permit any
exit
```
用`sh run | begin ip access`验证

在接口配置模式下用`ip access-group BlockSales out`应用到接口
#### 12.4.5 注释
关键字remark能够在IP标准和扩展ACL中添加注释

`show access-list`看不到这些注释，只能在运行配置中看到

### 12.5 禁用和配置网络服务
默认情况下，思科IOS运行了一些不必要的服务，它们很可能成为拒绝服务攻击的目标
#### 12.5.1 阻断SNMP分组
思科IOS默认允许从任何地方远程接入。访问控制列表能够保护你的路由器

通过在外围路由器的接口serial0/0上配置如下指令，可禁止任何SNMP分组进入该路由器和DMZ
```
conf t
access-list 110 deny udp any any eq snmp
permit ip any any
int s0/0
access-group 110 in
```
#### 12.5.2 禁用echo
默认情况下，思科路由器启用了一系列诊断端口。

为防范chargen攻击，可配置如下命令
```
conf t
no service tcp-small-servers
no service udp-small-servers

no service finger
```
finger是一个实用程序，允许因特网上的Unix主机用户能够彼此获取对方的信息
#### 12.5.3 禁用BootP和自动配置
默认情况下，思科路由器也提供异步线路BootP服务以及远程自动配置服务。禁用方法：
```
conf t
no ip boot server
no service config
```
#### 12.5.4 禁用HTTP进程
对配置和监视路由器来说，命令`ip http server`可能很有用，但HTTP的明文特征显然是一种安全风险。要在路由器上禁用HTTP进程，可使用`no ip http server`
#### 12.5.5 禁用IP源路由选择
IP报头包含一个源路由选项，让源IP主机可指定分组穿越IP网络时采用的路由。要禁用可使用`no ip source-route`
#### 12.5.6 禁用代理ARP
代理ARP可让主机到达远程子网，而无需配置路由选择或默认网关。要禁用代理ARP，可在接口配置模式下使用`no ip proxy-arp`，请在路由器的所有LAN接口上都配置该命令
#### 12.5.7 禁用重定向消息
为禁用重定向消息，以防坏人根据这种信息推断出网络拓扑，在接口配置模式下使用`no ip redirects`
#### 12.5.8 禁止生成ICMP不可达消息
要防止外围路由器告诉外部主机哪些子网不存在，进而泄露拓普信息，可使用命令`no ip unreachables`
在连接到外部的所有路由器接口上都配置这个命令

|标题|范围|命令|副作用|
|----|----|----|----|
|禁用组播路由缓存|所有路由器接口|no ip mroute-cache|降低合法组播性能|
|禁用维护操作协议|所有路由器接口|no mop enabled|-|
|关闭X.25 PAD服务|全局配置|no service pad|-|
|启用Nagle TCP拥塞算法|全局配置|service nagle|Xwindows断开，负载超平均|

本章未读完

# ch13 网络地址转换（NAT）

端口地址转换（PAT）也叫NAT重载

### 13.1 在什么情况下使用NAT
与CIDR一样，最初开发NAT也旨在推迟可用IP地址空间耗尽的时间。

但随后人们发现，在网络迁移和合并、服务器负载均衡以及创建虚拟服务器方面，NAT也是很有用的工具。

### 13.2 网络地址转换类型
静态NAT：一对一
动态NAT：地址池
NAT重载：多对一，使用端口，最常用

### 13.3 NAT术语
```
+-----------------+  +------+  +-----------------+
|from 内部本地地址|  | 边界 |->|from 内部全局地址|
|  to 外部全局地址|->|路由器|  |  to 外部本地地址|
+-----------------+  +------+  +-----------------+
```

### 13.4 NAT的工作原理
理论上PAT最多可让大约65000台主机共用一个公有IP地址
#### 13.4.1 配置静态NAT
```
ip nat inside source static 10.1.1.1 170.45.2.2
!
int e0
	ip address 10.1.1.10 255.255.255.0
	ip nat inside
!
int s0
	ip address 170.46.2.1 255.255.255.0
	ip nat outside
```
#### 13.4.2 配置动态NAT
```
ip nat pool todd 170.168.2.3 170.168.2.254 netmask 255.255.255.0
ip nat inside source list 1 pool todd
!
int e0
	ip address 10.1.1.10 255.255.255.0
	ip nat inside
!
int s0
	ip address 170.168.2.1 255.255.255.0
	ip nat outside
!
access-list 1 permit 10.1.1.0 0.0.0.255
```
访问控制列表用于指定感兴趣的数据流
#### 13.4.3 配置PAT（NAT重载）
```
ip nat pool globalnet 170.168.2.1 170.1668.2.1 netmask 255.255.255.0
ip nat inside source list 1 pool globalnet overload
!
int e0/0
	ip address 10.1.1.10 255.255.255.0
	ip nat inside
!
int s0/0
	ip address 170.168.2.1 255.255.255.0
	ip nat outside
!
access-list 1 permit 10.1.1.0 0.0.0.255
```
#### 13.4.4 NAT的简单验证
查看基本的IP地址转换信息，使用`show ip nat translations`

还可使用命令`debug ip nat`

想将NAT表中的转换条目清除，可使用`clear ip nat translations *`

### 13.5 NAT的测试和故障排除
故障常见原因
+ 检查动态地址池，看它包含的地址范围是否正确
+ 检查不同动态地址池所包含的地址是否重复
+ 检查用于静态映射的地址和动态地址池中的地址是否重复
+ 确保访问控制列表正确地指定了要转换的地址
+ 确保包含了应包含的地址，且没有包含不应包含的地址
+ 确保正确地指定内部接口和外部接口




















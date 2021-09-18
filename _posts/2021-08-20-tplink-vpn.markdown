---
layout: post
title:  "德珹常用设备的官网参考文档"
date:   2021-08-20 15:50:28 +0800
categories: jekyll update
---

# [VPN路由器](https://www.tp-link.com.cn/product_442.html?v=download#tag)

# H3C SecPath F100系列防火墙
[安装指导-6PW103](https://www.h3c.com/cn/d_201804/1076961_30005_0.htm#_Toc407281792)

## 负载均衡概述技术介绍
[6W100](http://www.h3c.com/cn/Service/Document_Software/Document_Center/Home/Switches/00-Public/Trending/Technologies/FZJH_Tech-Long/)
出链路负载均衡技术可基于多种分配原则，在多条链路上分担内网用户访问外部互联网流量。智能选路可以将访问特定运营商网络或特定应用的流量从指定的链路发送。动态调整支持动态探测链路的剩余带宽、路由跳数和网络时延等，根据探测结果为用户动态分配最优链路。会话保持用户访问同一业务的流量始终走同一出链路，保障关键业务流量不因跨链路而访问中断。故障感知支持对链路健康状况进行探测，自动屏蔽故障的链路。

## H3C 负载均衡产品 配置指导(V7)
[(R8110 R8107 R8112 R8102)-6W10302-负载均衡配置指导](http://www.h3c.com/cn/d_201805/1078270_30005_0.htm#_Toc511918346)
### 3 出方向链路负载均衡
TODO

## 负载均衡web配置
[1.7.3  Outbound链路负载均衡典型配置举例](https://www.h3c.com/cn/d_202001/1271989_30005_0.htm#_Toc30509385)

___

## [H3C交换机指示灯颜色](https://zhidao.baidu.com/question/360109930942902012.html)
绿色常亮 端口工作在1000Mbps，接收或发送数据时指示灯快速闪烁
黄色常亮 端口工作在10/100Mbps，接收或发送数据时指示灯快速闪烁

## [H3C交换机温度显示为0 或者N/A](https://zhiliao.h3c.com/questions/dispcont/17241)

## [h3c防火墙指导的配置备份](http://www.h3c.com/cn/d_202001/1271998_30005_0.htm#_Toc30509383)
### 1.2.2  配置备份
请同时备份“.cfg”和“.xml”结尾的配置文件，否则在某些情况下（如配置不小心被删除的情况）可能会导致部分配置信息无法恢复。
### 1.2.3  配置恢复
恢复的配置文件在设备下次启动后才会生效。
### 1.2.5  导入配置
导入配置提供将保存在用户主机上的.cfg配置文件导入到设备，对设备执行文件中的配置的功能。导入的配置是即时生效的，但不会自动保存到下次启动配置文件中，需要用户手动保存配置。

## [tplink的VPN路由器 用户手册](https://www.tp-link.com.cn/product_442.html?v=download#tag)
导入的配置文件版本与路由器当前配置版本差距过大，将有可能导致路由器现有配置信息丢失，如果有重要的配置信息，请谨慎操作。
### 链路维护时间间隔 设置发送链路维护检测报文的时间间隔。

## [配置Loopback接口](http://www.h3c.com/cn/d_202001/1271922_30005_0.htm#_Toc30507438)

## [通过console口配置](https://www.h3c.com/cn/d_201809/1107276_30005_0.htm#_Toc523326297)

## [核心交换机官网手册](https://www.h3c.com/cn/Service/Document_Software/Document_Center/Switches/Catalog/S5500/S5500-EI/)

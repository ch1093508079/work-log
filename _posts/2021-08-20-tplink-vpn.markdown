---
layout: post
title:  "VPN专项笔记"
date:   2021-08-20 15:50:28 +0800
categories: jekyll update
---

# https://www.tp-link.com.cn/product_442.html?v=download#tag

## 用户手册

#### NAT穿透
在实际网络应用中，IPSec VPN通信双方的物理连接线路中可能存在着NAT网关，当数据包经过NAT网
关时，其IP地址或端口号会改变，这就导致VPN隧道对端收到数据包后验证失败，数据包被直接丢弃。
NAT穿透功能可以解决这一问题，实现方法为在原ESP协议的报文外添加新的IP首部和UDP首部。这样
数据包（隧道模式下）的格式为：新IP/UDP首部 | ESP首部 | IP首部 | 数据 。由于NAT网关只会改变
最外层的IP首部，而且ESP校验不包含IP首部，所以此时IPSec VPN的通信不会受到影响。但是NAT穿
透只适用于ESP协议，AH协议的校验包含了IP首部，因此无法与NAT共存。TL-ER6120G目前默认支持
NAT穿透，当对端也支持NAT穿透，并且双方协商时检测到存在NAT设备的时候，会自动启用该功能。

# https://smb.tp-link.com.cn/service/detail_article_216.html
TL-ER6120支持IPSEC 、PPTP、L2TP 以及L2TP over IPSEC 多种VPN， 当前Windows、Mac OS、Android系统都自带有PPTP、L2TP连接方式，无需安装第三方软件，可直接通过Internet连接到公司内网。这样移动用户就可以在笔记本、平板电脑，甚至是手机上进行办公。

PPTP/l2tp VPN功能的详细配置方法请参考[文档]


以上为网络资料
---
以下为《构建高可用Linux服务器》对vpn的介绍

## 7.2 如何选择自己需要的VPN
1. 总部与远程用户的上网地点是否固定？
+ 如果是，考虑用IPsec
+ 如果否，例如在家办公，考虑PPTPD和OpenVPN
2. 远程连接的管理是否方便？
+ IPsec客户端的配置很烦琐
+ PPTPD和OpenVPN就简单容易多了
3. 是否需要额外的硬件和软件成本投入？
+ IPsec要求每一个连锁店都安装一台VPN硬件设备
+ 而其他几种VPN都是开源软件
4. 是否需要单独为VPN划分网络？见原书描述

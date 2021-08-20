---
layout: post
title:  "tplink-vpn"
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

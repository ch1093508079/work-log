---
layout: post
title:  "HCIA-Datacom V1.0 培训教材"
date:   2021-12-16 11:25:00 +0800
categories: book-note
---

# WLAN

## 有线侧组网

### AC与AP间会建立CAPWAP隧道
CAPWAP基于UDP
1. 有两种类型的消息
+ 业务数据流量，封装转发无线数据帧。——通过CAPWAP数据隧道
+ 管理流量，管理AP和AC之间交换的管理消息。——通过CAPWAP控制隧道
1. CAPWAP端口
+ 管理流量：UDP5246
+ 业务数据流量：UDP5247

### 大型组网中一般采用三层组网
1. 二层组网AP可以通过二层广播或者DHCP即插即用上线
1. 三层网络AP无法直接发现AC，需要通过DHCP或DNS方式动态发现，或者配置静态IP

### AC连接方式
1. 直连式组网：AC同时扮演了汇聚层交换机，对AC的性能要求较高
1. 旁挂式组网（使用率较高）：AP的业务数据可以不经AC而直接到达上行网络

## 看到P640:无线侧组网概念


以上为HCIA-Datacom V1.0 培训教材
---
以下为《CCNA-ICDN1》读书笔记

# ch23 高级IPv4 ACL和设备安全

### 23.1 小测试
df ae e a 

### 23.2 基础内容
#### 23.2.2 命名ACL和ACL编辑
##### 使用序列号编辑ACL
默认序号为10，20，30…

用no 20删除20

用5 deny……插入

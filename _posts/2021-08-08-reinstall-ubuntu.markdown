---
layout: post
title:  "安装Ubuntu后要做的设置"
date:   2021-08-08 15:50:28 +0800
categories: jekyll update
---

## [Ubuntu16.04系统安装后的10件真正必做之事。](https://www.cnblogs.com/fnight/p/5722016.html)总结如下：
```shell
sudo echo 获取临时sudo免密权限
cd /usr/local/
sudo rm games
sudo ln -s ~/文档/dot-file/bin games
cd ~
# 使用本地时区可避免与windows时间错乱
timedatectl set-local-rtc 1
sudo apt-get update
sudo apt-get -y install vim
sudo apt-get -y install git
git config --global core.editor vim
git config --global core.quotepath false
git config --global alias.goa 'log --graph --pretty=oneline --abbrev-commit'
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
ssh-keygen -t rsa -C "you@example.com"



# 按3次回车
cat ~/.ssh/id_rsa.pub
# 需手动把公钥放上github或gitee
ssh -T git@gitee.com
yes
```

## [Cygwin中文配置](http://www.cygwin.cn/site/info/show.php?IID=1005)

cygwin\home\username\.bashrc

```shell
# 让ls和dir命令显示颜色
alias ls='ls --show-control-chars --color'
alias dir='dir -N --color'
export LANG="zh_CN.UTF-8"
## 设置为中文环境，使提示成为中文
#export LANG="zh_CN.GBK"
## 输出为中文编码
#export OUTPUT_CHARSET="GBK"
```

cygwin\home\username\.inputrc

```shell
# 可以输入中文 
set meta-flag on
set output-meta on
set convert-meta off
# 忽略大小写
set completion-ignore-case on
```

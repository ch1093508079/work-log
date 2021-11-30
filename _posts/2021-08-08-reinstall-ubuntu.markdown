---
layout: post
title:  "安装Ubuntu后要做的设置"
date:   2021-08-08 15:50:28 +0800
categories: jekyll update
---

## 不改变/home重装优麒麟后要做
```shell
ssh-keygen -t ed25519 -C "Lenvo2022Jan"




# 按3次回车
cat ~/.ssh/id_ed25519.pub
# 需手动把公钥放上github或gitee
# ssh -T git@gitee.com
ssh -T git@github.com
yes
# 输出 "... GitHub does not provide shell access." 是正常的，错误输出是：
# Agent admitted failure to sign using the key.
# debug1: No more authentication methods to try.
# Permission denied (publickey).

sudo echo 获取临时sudo免密权限

cd ~/文档/
git clone git@gitee.com:ubuntubackup/dot-file.git
cd /usr/local/
sudo rm -r games
sudo ln -s ~/文档/dot-file/bin games
cd ~

git config --global core.editor vim
git config --global core.quotepath false
git config --global alias.goa 'log --graph --pretty=oneline --abbrev-commit'
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# 使用本地时区可避免与windows时间错乱
timedatectl set-local-rtc 1

sudo apt -y update 
sudo apt -y install python3-pip
pip3 install bs4
```

### 参考：[Ubuntu16.04系统安装后的10件真正必做之事。](https://www.cnblogs.com/fnight/p/5722016.html)总结如下：

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

安装bash-complete

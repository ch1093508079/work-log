---
layout: post
title:  "我的linux环境搭建"
date:   2021-08-08 15:50:28 +0800
categories: jekyll update
---

## 覆盖/home后要做
```shell
gpg --import e1024.pri
gpg --import e1024.pub
gpg --edit-key e@e.com
trust
5
y
save
ssh-keygen -t ed25519 -C "Lenvo2022Jan"




# 按3次回车
cat ~/.ssh/id_ed25519.pub
# 需手动把公钥放上github或gitee
ssh -T git@gitee.com
yes
```

## 不改变/home重装ubuntu后要做
```shell
ssh -T git@github.com
yes
# 输出 "... GitHub does not provide shell access." 是正常的，错误输出是：
# Agent admitted failure to sign using the key.
# debug1: No more authentication methods to try.
# Permission denied (publickey).

sudo echo 获取临时sudo免密权限

sudo apt -y update 
sudo apt -y install vim git
sudo apt -y install ffmpeg
sudo apt -y install python3-pip
pip3 install bs4

cd ~/文档/
git clone git@gitee.com:ubuntubackup/dot-file.git
cd /usr/local/
sudo rm -r games
sudo ln -s ~/文档/dot-file/bin games
cd ~

git config --global core.editor vim
git config --global core.quotepath false
git config --global alias.goa 'log --graph --pretty=oneline --abbrev-commit'
git config --global user.name "e1024"
git config --global user.email "e@e.com"

# 使用本地时区可避免与windows时间错乱
timedatectl set-local-rtc 1
```

### 参考：[Ubuntu16.04系统安装后的10件真正必做之事。](https://www.cnblogs.com/fnight/p/5722016.html)总结如下：

## [Cygwin中文配置](http://www.cygwin.cn/site/info/show.php?IID=1005)
经验：手动设置字体大小和中文编码

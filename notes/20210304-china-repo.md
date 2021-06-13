---
title: 国内源
tags: Linux
layout: post
---

# Ruby

```bash
gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
gem sources -l
# 确保只有 gems.ruby-china.com
```

# Anaconda

```bash
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
```

# CentOS

```bash
下载：http://mirrors.aliyun.com/centos/7/isos/x86_64/
修改 repo：
mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak
wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
yum makecache 
yum -y update
```

# Docker

```sh
vi  /etc/docker/daemon.json
#修改后如下：
{
    "registry-mirrors": ["https://registry.docker-cn.com"],
    "live-restore": true
}

systemctl restart docker.service
```
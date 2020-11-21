---
layout: article
title:  "使用docker运行多个版本的cuda"
date:   2020-11-21
tags: ['docker', 'cuda']
mathjax: true
key: 2020-11-21-blog
---

> 如果你遇到了这样一个问题:
>
> 我的机器上装的cuda版本是最新的，比如cuda 11.1，然而我拿到了一个在cuda 8.0的版本上编译好的程序，我该怎么运行它呢？总不会我又要安装一个8.0的cuda吧。(这个问题来自于我在做cmu 15-418 assignment task2时需要运行在cuda8.0环境编译的参考程序cudaScan_ref，而我的cuda是11.1版本)
>
> 这个时候你肯定立刻会想到虚拟化，作为轻便好用的虚拟化工具，docker就派上用场了。
>
> 这篇文章就来介绍一下如何使用docker运行多版本的cuda。

- 本机环境
```
系统：18.04.5 LTS (Bionic Beaver)
已安装cuda版本：11.1
```
## １ docker准备

### １.1 了解原理和基本命令
如果你还是个docker小白，建议先通过[官方文档](https://docs.docker.com/get-started/overview/)了解一下docker的原理和基本用法，如运行、停止、删除镜像等。

#### 1.2 安装
官方的[安装教程](https://docs.docker.com/engine/install/)提供了对应不同操作系统的安装方法。

当然，由于ubuntu 18.04源已经集成了docker软件，可以直接通过包管理工具安装。方法是
```
# on ubuntu 18.04
sudo apt instll docker.io
```
## 2 Nvidia Container Toolkit准备
Nvidia目前提供`Nvidia Container Toolkit`和`nvidia-docker2`包完成对docker的支持，可以通过[安装教程](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#docker)进行安装。

安装的时候要注意其支持的系统环境和需要的环境依赖。

## 3 在docker上运行cuda环境
准备工作完成后，就可以来解决文章开始提出的问题了:如何在host环境为cuda11.1的情况下使用docker运行基于cuda8.0编译的程序？

### 3.1 镜像获取
首先要从[docker-hub](https://hub.docker.com/)上找到我们需要的环境的镜像，使用关键字`cuda8.0`搜索即可，然后在本地拉取镜像源。

比如：我在docker-hub上找到这样的镜像：`klauskyj/cuda8.0-cudnn7
`。那么就可以通过
```
sudo docker pull klauskyj/cuda8.0-cudnn7
```
拉取下来了。
通过
```
sudo docker ps -a 
```
可以看到自己拉取的镜像。
### 3.2 运行镜像
类似于普通镜像运行自己拉取下来的镜像，runtime设为nvidia即可，如
```
sudo docker run -it --runtime=nvidia [DOCKER_IMAGE]:[DOCKER_TAG] /bin/bash
```
进入交互式环境后，去`/usr/local`目录下就可以看到cuda 8.0了。
### 3.3 运行程序
那么如何在容器中运行程序呢？我们需要将程序拷贝进去。从主机拷贝文件到容器中步骤如下：

1. 通过
```
sudo docker ps -a
``` 
获取容器的短ID或者name。

2. 通过


sudo docker inspect -f '&#123;&#123; .Id &#125;&#125;' [短ID or name]

获取容器的完整ID。
如：


➜  render git:(master) ✗ sudo docker inspect -f '&#123;&#123; .Id &#125;&#125;' cc1ec222c1ff
cc1ec222c1ff72272a00061aa197ab8ba13bd446697b9d9c1820c45ba16b75cd



3. 通过
```
sudo docker cp [本地文件路径] [ID全称]:[容器路径]
```
拷贝文件，注意拷贝目录的话也一样，不用加其他参数。

如果从容器中传输文件到host，通过
```
sudo docker cp [ID全称]:[容器文件路径] [本地路径]
```
完成。

最后，在容器中就可以运行这个程序啦。

## 4 总结
这篇文章其实介绍了基本的docker用法，nvidia提供的nvidia-docker2.0封装的很好，可以方便地建立cuda环境，这里要注意虚拟化的cuda的版本要和自己的GPU匹配。
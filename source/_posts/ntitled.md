title: 安装centos操作系统
author: daidai
tags:
  - centos
categories:
  - linux
date: 2018-08-10 17:02:00
---
## 制作启动盘


##### 在`https://www.centos.org/download/`下载相应的文件

- 安装包类别（注意32位和64位区别）
    - DVD ISO   --系统标准安装包
    - Everything ISO    --对完整版安装盘的软件进行补充，集成所有软件。
    - Minimal ISO   --这个镜像的目的是安装一个非常基本的系统，具有一个功能系统所需的最少的软件包。

##### 使用UltraISO，在`https://cn.ultraiso.net/`下载

- 制作启动盘步骤
    - 打开软件
    - 在本地目录栏打开刚才下载的镜像文件
    - 点击-->启动-->写入硬盘镜像...
        - 选择U盘
        - 写入方式是USB-HDD+
        - 然后写入

## 设置bios

- 查找自己电脑对应的开机进入bios的键，进入bios，设置U盘为第一启动盘，保存、开机

## 安装

- 注意：
    ```
    gnome桌面（要选上，不然没有桌面的）
    network配置（使用系统的引导，比自己设置网络省事）
    ```
    - NETWORK & HOST NAME-->打开（显示ip地址就好了）
    - SOFTWARE SELECTION-->选择GNAME Desktop就是有桌面的
    - 也可以安装后系统第一次进入的时候记得选择网络配置就好
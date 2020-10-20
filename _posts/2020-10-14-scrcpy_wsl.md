---
layout: post
title: WSL安装scrcpy
tags: wsl scrcpy wsl2 adb
categories: prodouctivity
---

> 在单位时间比较多，尤其是值班的时候，来回看手机很不方便。之前重装的win10，又装的WSL(Ubuntu)，借此机会在WSL上使用scrcpy，前后两个小半天的时间才弄好，就是传输很慢，与在mbp上使用体验相差太多，也只能用来看个状态什么的。

## 1 wsl升级wsl2
命令 | 功能
-- | --
lsb_release -a | 查看系统版本
do-release-upgrade | 升级系统版本
sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup | 备份镜像源
sudo vi /etc/apt/sources.list | 编辑系统镜像源
sudo apt-get update | 更新镜像源

## 2 wsl安装scrcpy
`sudo apt install scrcpy`

## 3 安装adb
* wsl安装adb、查看版本
```
sudo apt-get install android-tools-adb
sudo apt install adb
adb kill-server
adb devices
adb version
```

* [windows安装adb](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)、查看版本、高级系统设置添加环境变量
`adb version`

* wsl卸载当前版本并安装指定版本adb
```
sudo apt remove adb
wget https://dl.google.com/android/repository/platform-tools_r30.0.4-linux.zip
cd
sudo mv adb /usr/bin/adb
adb version
```

## 4 安装x11
* [windows安装x11](https://sourceforge.net/projects/xming/files/latest/download11)
* x11添加到wsl环境变量
`echo "export DISPLAY=:0.0" >> ~/.bashrc`


## 5 使用
```
# 不挂断运行
nohup scrcpy &
```
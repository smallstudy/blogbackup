---
layout: post
title: UnblockNeteaseMusic
date: 2019-08-07 00:14:11
tags:
---
>声明:本教程只用作学习交流，请勿作他用，如有侵权，请联系我删除;
## 1.手机安装终端模拟器
推荐termux,可以去酷安下载
>![avatar](https://github.com/smallstudy/picture/blob/master/%E8%BD%AF%E4%BB%B6.png?raw=true)
<!-- more -->
## 2.	termux配置
>推荐看这个文章，[Termux配置指南，你要的全都有](https://blog.csdn.net/qq_42471423/article/details/90582792?utm_source=app)
## 3.在termux里安装git、node.js
```
pkg install git      安装git
pkg install nodejs   安装node.js
node -v   查看node.js是否安装成功
git -v     查看git是否安装成功
```
>![avatar](https://github.com/smallstudy/picture/blob/master/%E5%AE%89%E8%A3%85git%E3%80%81nodejs.png?raw=true)
## 4.	在termux运行项目
```
git clone https://github.com/nondanee/UnblockNeteaseMusic.git    下载项目
cd UnblockNeteaseMusic    进项目根目录
node app.js (后台运行)      运行项目
```
>![avatar](https://github.com/smallstudy/picture/blob/master/%E8%BF%90%E8%A1%8C%E9%A1%B9%E7%9B%AE.png?raw=true)
## 5.改手机接入点apn
```
手机设置>>SIM卡和移动网络>>SIM卡>>接入点名称(APN)>>
选一个apn接入点改代理为127.0.0.1端口8080，设置好后使用这个apn接入点
```
>![avatar](https://github.com/smallstudy/picture/blob/master/apn.png?raw=true)

打开终端查看是否成功:
>![avatar](https://github.com/smallstudy/picture/blob/master/%E6%95%88%E6%9E%9C.png?raw=true)

打开网易云查看效果:
>![avatar](https://github.com/smallstudy/picture/blob/master/%E6%95%88%E6%9E%9C2.png?raw=true)

感谢该项目的作者，[项目地址https://github.com/nondanee/UnblockNeteaseMusic](https://github.com/nondanee/UnblockNeteaseMusic)
其他的使用方法可查看该项目的README

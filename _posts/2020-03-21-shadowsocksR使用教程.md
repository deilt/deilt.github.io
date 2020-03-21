---
date: 2020-03-21 16:26:40
layout: post
title: 小灰机教程
subtitle: 小灰机
description: 科学上网
image: https://images-na.ssl-images-amazon.com/images/I/71kMXfUIttL.png
optimized_image: https://images-na.ssl-images-amazon.com/images/I/71kMXfUIttL.png
category: vpn
tags:
  - web
  - tools
  - vpn
author: deilt
---

# 前言
ShadowsocksR常被称为SSR、酸酸乳、小飞机（粉色）、纸飞机（粉色），是由“破娃酱”发起的一个项目，也是目前热门的科学上网技术之一。SSR没有官方网站，项目代码托管在Github上，目前已经停止开发，客户端由志愿者维护。

# 下载
win: <https://github.com/shadowsocksrr/shadowsocksr-csharp/releases>

安卓客户端:<https://github.com/shadowsocksrr/shadowsocksr-android/releases>

MAC客户端:<https://github.com/qinyuhang/ShadowsocksX-NG-R/releases>

# win教程
1. 安装客户端：找到下载的安装程序，找一个合适的目录解压（不建议放在C盘的”Program Files”目录，会有权限问题），不要在压缩包里双击运行！

2. 双击文件夹内的“ShadowsocksR-dotnet4.0.exe”文件运行程序，系统防火墙可能会弹出提示，点击“允许访问”;  
   如果双击程序没有反应，托盘（托盘就是桌面右下角，显示时间输入法那块）里也没有小飞机的图标，请先更新系统并安装 [.NET Framework 4.7.2](https://www.microsoft.com/en-us/download/details.aspx?id=53840) 和 [Microsoft Visual C++ 2015 Redistributable (x86)](https://www.microsoft.com/en-us/download/details.aspx?id=53840)。

3. 右下角托盘找到小飞机图标，鼠标左键点击图标，出现服务器配置框

   如果你用的订阅地址，请参考第8步。

4. 填写“服务器IP”(勾选前面的框会显示服务器ip)、“服务器端口”、密码（勾选前面的框会显示密码），然后选择加密模式、协议和混淆模式（注意：这些信息务必和服务端一致！）。在备注和群组名里填一个好记的名字，例如“新加坡vps”、“不限流量”。配置好后点击确定。

5. 右键系统托盘的小飞机图标，鼠标移到“系统代理模式”，在右侧菜单中选择模式。建议用“PAC模式”，某些网址打不开再切换全局模式：

6. 鼠标移到“PAC”，建议点击“更新PAC为GFWList”，也可以选“更新PAC为绕过大陆常见域名列表”。如果更新出现问题，说明配置有问题或者服务端不可用。请检查输入的ip密码端口等信息是否正确、服务端程序是否正常运行，否则无法上外网！

7. “服务器”一栏中可以查看添加的服务器，也可以点击“编辑服务器”查看和更新服务器信息（效果等同于鼠标左键点击托盘图标，也就是第1步的操作）；

8. 如果你的服务端信息是订阅地址，请右键托盘图标后鼠标移到“服务器订阅”，然后点击“SSR服务器订阅设置”。在SSR订阅设置框中点击“Add”，把订阅地址复制到右侧的“网址”一栏，点击确定。在“服务器订阅中”点击“更新SSR服务器订阅”刷新服务器信息;

高级选项可以点击“选项设置”和“端口设置”更改，绝大部分情况下都不需要改动。

配置信息正确，网络通畅的话，google、youtube等网站应该能正常打开。
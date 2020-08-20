---
title: Hexo配置
date: 2020-08-18 16:31:39
hide: true
copyright_author: sdte0tw
copyright_author_href: https://github.com/sdte0tw
copyright_url: /hexo
copyright_info: 关于Hexo的配置
categories: 
- 学习
- 网页
---
# Hexo安装

## 1.安装Git
下载地址：https://nodejs.org/en/ ，按步骤安装

## 2.安装Node.js
下载地址：https://nodejs.org/en ，按步骤安装
完成后在桌面右键打开`Git Bash Here`，输入`node -v`和`npm -v`查看二者版本，以验证是否安装成功
```powershell
$ node -v
v12.18.3

$ npm -v
6.14.6
```

## 3.安装Hexo
在 Git Bash 中输入`$ npm install -g hexo`以进行全局 Hexo 安装
等待安装完成后，输入`hexo -v`查看 Hexo 版本，以验证是否安装成功
```powershell
hexo: 5.0.2
hexo-cli: 4.2.0
os: Windows_NT 6.1.7601 win32 x64
node: 12.18.3
v8: 7.8.279.23-node.39
uv: 1.38.0
zlib: 1.2.11
brotli: 1.0.7
ares: 1.16.0
modules: 72
nghttp2: 1.41.0
napi: 6
llhttp: 2.0.4
http_parser: 2.9.3
openssl: 1.1.1g
cldr: 37.0
icu: 67.1
tz: 2019c
unicode: 13.0
```

# 建立本地Hexo站点

## 1.建站
建立一个文件夹（英文名字无所谓位置无所谓）作为 Hexo 的根目录
在该文件夹中右键打开 Git Bash 窗口，输入`hexo init`初始化文件夹为 Hexo 根目录
完成后输入`npm install`安装模块
```powershell
$ hexo init
INFO  Cloning hexo-starter to file
......
INFO  Install dependencies
......
added 397 packages in 34.63s
INFO  Start blogging with Hexo!

$ npm install
......
audited 4704 packages in 5.315s
found 0 vulnerabilities
```

## 2.网站配置
根目录的`_config.yml`是网站的配置文件，可用记事本打开（推荐使用编辑器或者IDE）
>注意属性和值之间在冒号后要有空格

Site 网站相关设置

属性  |  描述
:----: | :----:
title  |  网站标题
subtitle  |  网站副标题
description  |  网站描述
keywords  |  网站关键字
author  |  网站作者
language  |  网站使用的语言，默认是en ，中文网站填zh-Hans
timezone  |  网站使用的时区，默认为 计算机的预设置，可以不填

以上是举个例子，具体的网站设置参照 [Hexo基础配置文件详解](/hexo-set)


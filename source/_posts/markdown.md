---
title: Markdown常用语法
date: 2020-08-18 15:58:57
hide: true
copyright_author: sdte0tw
copyright_author_href: https://github.com/sdte0tw
copyright_url: /markdown
copyright_info: 一些常用的Markdown语法
categories: 
- 学习
- 网页
---

# 文字编辑

## 文字居中
`<center>中间放文字</center>`
>效果
><center>文字的居中</center>

## 字体和颜色

### 字体
前面一栏加`face`
`<font face="黑体">我是黑体字</font>`
>效果
><font face="黑体">我是黑体字</font>

### 大小
前面一栏加`size`，默认大小为2，最大为10
`<font size=10>字体大小</font>`
>效果
><font size=10>字体大小</font>

### 颜色
前面一栏加`color`
`<font color=red>字体颜色</font>`
>效果
><font color=red>字体颜色</font>

### 文字效果叠加
叠加效果可以这么写`<center><font size=10 color=red>效果叠加</center></font>`
>效果
><center><font size=10 color=red>效果叠加</center></font>

# 表格
使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行
>表格语句的上一行必须为空行否则无法生成表格
```markdown
表头 | 表头
---- | ----
单元格 | 单元格
单元格 | 单元格
```
>效果
>
>表头 | 表头
>---- | ----
>单元格 | 单元格
>单元格 | 单元格

在`-`的左右或两边加`:`控制整列的左右对齐或居中
```markdown
左对齐 | 右对齐 | 居中对齐
:-----| ----: | :----:
单元格 | 单元格 | 单元格
单元格 | 单元格 | 单元格
```
>效果
>
>左对齐 | 右对齐 | 居中对齐
>:-----| ----: | :----:
>单元格 | 单元格 | 单元格
>单元格 | 单元格 | 单元格


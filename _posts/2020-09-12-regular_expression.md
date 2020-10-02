---
layout: post
title: 正则表达式教程
tags: 正则表达
categories: productivity
---
> Regular Expression (RegExr):元字符+运算符

<br/>

## 挑选出数字
```
var str = "abc123def";
var patt1 = /[0-9]+/; 
document.write(str.match(patt1));
```

## 设置用户名格式
```
#开始标记+字母、数字、下划线、连接字符+字符长度+结束标记
^[a-z0-9_-]{3,15}$
```

## 语法
普通字符 | 描述
-- | --
+ | ≥1
* | ≥0
? | 0,1
[ABC] | ABC
[^ABC] | ~~ABC~~
[A-Z] | ABC...Z
. | [^\n\r]
[\s\S] |   
\w | [A-Za-z0-9_]

非打印字符 | 描述
-- | -- 
\cx | x控制字符
\f | 换页符
\n | 换行符
\r | 回车符
\s | 空白字符
\S | 非空白字符
\t | 制表符
\v |垂直制表符

特殊字符 | 描述
-- | --
$ | 结尾
() | 开始和结束
^ | 开始

限定符 | 描述
-- | --
{n} | n
{n,} | ≥n
{n,m} | ≥n&&≤m


## 
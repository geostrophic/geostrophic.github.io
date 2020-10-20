---
layout: post
title: Windows、macOs、Android安装Mysql
tags: cmd terminal termux mysql
categories: research
---

> 各种安装，各种改密码。。。

## Windows安装Mysql
```

```

## macOs安装Mysql

```
# 连接termux
ssh 192.168.31.250 -p 8022  
```

## terumx安装Mysql
```
pkg install mariadb
mysql --version
nohup mysqld &
kill -9 `pgrep mysql`
mysql -u $(whoami)
use mysql;
set password for 'root'@'localhost' = password('6120308');
flush privileges;
quit;
mysql -u root -p
select user(), version();
quit
ip a
grant all on *.* to root@'%' identified by '6120308' with grant option;
flush privileges;
# 开启ssh服务被连接 
sshd
# 连接mbp
ssh bigechen@192.168.31.198
```
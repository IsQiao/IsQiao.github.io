---
title: mysql常见命令
date: 2020-03-15 00:00:00 Z
categories:
- Database
---

创建用户
```
 create user 'account‘ IDENTIFIED BY 'password';
```
赋予表权限
```
 grant ALL on dbname.* to 'account'@'%';
```
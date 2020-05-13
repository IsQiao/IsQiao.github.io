---
title: mysql常见命令
categories: [Database]
---

创建用户
```
 create user 'account‘ IDENTIFIED BY 'password';
```
赋予表权限
```
 grant ALL on dbname.* to 'account'@'%';
```
---
title: 右键菜单打开WindowsTerminal
date: 2020-05-14 00:00:00 Z
categories:
- Windows
layout: post
---

## 前言
*windows terminal preview版本出来了，还挺好用的，windows默认按shift+右键打开的是powershell，不太方便所以写了一下这个。*
## 具体步骤
* 首先在商店里安装windows terminal
* 新建一个wt.reg的注册表文件，填入如下信息，改好后双击运行。
```
Windows Registry Editor Version 5.00
[HKEY_CLASSES_ROOT\Directory\Background\shell\wt]
@="Open Terminal window here"
"Icon"="C:\\Program Files\\WindowsApps\\Microsoft.WindowsTerminal_0.11.1251.0_x64__8wekyb3d8bbwe\\WindowsTerminal.exe"
[HKEY_CLASSES_ROOT\Directory\Background\shell\wt\command]
@="C:\\Users\\qxwxi\\AppData\\Local\\Microsoft\\WindowsApps\\wt.exe "
```

### 注意 
图标文件路径的(Microsoft.WindowsTerminal_0.11.1251.0_x64__8wekyb3d8bbwe)部分要对应自己下载的版本号
执行文件的路径（C:\\Users\\qxwxi\\AppData\\Local）要对应自己的帐号名字，检查一下.
* 打开windows terminal的设置，在default节点下设置，打开目录为当前目录
```
    "profiles":
    {
        "defaults":
        {
            // Put settings here that you want to apply to all profiles.
            "startingDirectory": "%__CD__%"
        },
```

搞定。
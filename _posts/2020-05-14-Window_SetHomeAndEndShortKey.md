---
title: Windows设置MacOS下的Home与End快捷键
date: 2020-05-14 00:00:00 Z
categories:
- Windows
layout: post
---

## 前言
*由于最近使用windows笔记本敲代码，发现home和end快捷键要使用fn+f11或者fn+f12才能用。这很明显敲代码用不了，于是写了这个AutoHotKey脚本，改成了和MacOS一样的了*
## 操作步骤
* 下载AutoHotKey，安装，右键桌面，新建一个AutoHotKey脚本
* 将下面代码粘贴进去，双击运行，完成。
```
^left::
    send {home}
return
^right::
    send {end}
return
^Up::
    Send, {PgUp}
return
^Down::
    Send, {PgDn}
return
^+Left::
    Send, {Shift down}{Home}{Shift up}
return
^+Right::
    Send, {Shift down}{end}{Shift up}
return
^+Up::
    Send, {Shift down}{PgUp}{Shift up}
return
^+Down::
    Send, {Shift down}{PgDn}{Shift up}
return
```

现在就可以使用ctrl+->,ctrl+<-,ctrl+上,ctrl+下 等啦,懒得打字了。
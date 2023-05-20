---
title: 解决打印机列表堵塞
tags: CMD
---

有些时候，打印机会出现错误的情况，也无法删除报错的打印作业，导致无法正常打印

这里分享一个 .bat 文件，可以解决打印机列表堵塞的情况

    net stop spooler
    delc:\windows\system32\spool\printers\*.* /Q /F
    net start spooler

运行完毕后，重启电脑即可解决问题

* 脚本内容源于网络，非原创内容
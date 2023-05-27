---
title: 解决打印机列表堵塞
tags: [CMD,Printer]
---

有些时候，打印机会出现报错，并且无法删除报错的打印作业，导致无法正常打印

分享一个批处理文件，可以解决打印机列表堵塞的情况

使用方法：将以下内容复制到一个文本文档里，保存后将该文本文档的扩展名改为 .bat

    net stop spooler
    delc:\windows\system32\spool\printers\*.* /Q /F
    net start spooler

运行完毕后，**重启电脑**即可解决问题
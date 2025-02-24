---
layout: article
tags: Linux
title: Linux下gdb调试
author: Guailper
---



# Linux下gdb调试

使用`gcc infile -o outfile -g`可以使得在进行gdb调试时查看源代码

```
gdb 可执行文件名 //进入gdb调试
quit //退出gdb

set args xxx //设置参数
show args //获取设置参数

help //获取gdb使用帮助

//运行gdb程序
start //转到程序第一行
run //执行代码直到遇上断点

//显示代码
l/list //
l/list 行号/函数名 //
l/list 外部源文件:行号/函数名 //
show list/listsize //显示使用list显示的代码行数
set list/listsize 数字 //设置行数

//断点
b/break 行号
b/break 函数名
b/break 外部源文件:行号/函数名

//调试
c/continue //遇上断点时使用，至下一个断点处停
n/next //向下执行一行代码，不会进入函数体
s/step //向下单步调试，会进入函数体
finish //跳出函数体

//变量操作
p/print 变量名 //打印变量值
ptype 变量名 //打印变量类型


//自动变量操作
display 变量名 //自动打印指定变量值（回车后）
i/info display //显示display详细信息
undisplay 编号 //删除相关编号的display

//其他
set var 变量名=变量值 //
until //跳出循环
```


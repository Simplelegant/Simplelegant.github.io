---
layout:     post
title:      "UNIX网络编程代码编译"
subtitle:   ""
date:       2019-2-21 18:54:04
author:     "Simpleelegant"
header-img: "img/post-bg-newstart.jpg"
tags:
    - UNIX网络编程
---

 <center>UNIX网络编程代码编译</center>

最近开始了UNIX网络编程的学习，学习不仅仅要看书还需要写代码，因此书上的实例代码必须要编译通过，但是单独把第一章开始的代码拎出来编译始终编译不通过，例如<sys/event.h>找不到等等，花费了一下午时间后只好先整体编译示例代码。

但是编译过程还是出现了一些问题，下面做一个总结。<br>
Q1: 输入sudo ./configure提示找不到命令?<br>
A1: ~ chmod +x ./configure
	~ ./configure
	shell脚本在新机器上记得添加执行权限<br>

Q2: 整体编译流程？<br>
A2:	>$ cd unpv13e   <br>
	>~unpv13e/$ ./configure  
  
	>~unpv13e/$ cd lib  
	>~unpv13e/lib/$ make  
  
	>~unpv13e/lib/$ cd ../libfree  
	>~unpv13e/libfree/$ make  

Q3: 按流程走遇到的错误？<br>
A3:  将第60行的 size_t size 改成 socklen_t size;然后再make<br>

Q4: 接下来呢？<br>
A4: 将生成的libunp.a复制到/usr/lib下
	unpv13e/libgai/$ cd ..  
	unpv13e/$ sudo cp libunp.a /usr/lib

	修改unpv13e/lib/unp.h并复制
	unpv13e/$ vim lib/unp.h  // 将#include "../config.h" 改成 #include "config.h"  
	unpv13e/$  sudo cp lib/unp.h /usr/include  
	unpv13e/$ sudo cp config.h /usr/include 

	编译例子
	unpv13e/$  cd intro  
	unpv13e/$  gcc daytimetcpcli.c -o cli -lunp   
  

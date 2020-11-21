---
title: c++中的new与delete
date: 2020-8-30 10：23
tags:
- notes
categories:
- c++
---
new与delte都为运算符而非库函数
***
new

定义符号常量 const int N=...; const int M=...;
定义变量 int型指针p，二级指针q，int型i，j;

申请一个int型动态变量:p=new int;

申请N个元素的动态一维数组:p=new int[N];

申请N行M列的动态二维数组：q=new int[N];
                         for (i=0;i<N;i++)
                          q[i]=new int[M];
数组元素可用q[i][j]调用

注:1.new申请的动态内存空间中存放的为随机值
   2.p=new int(10); 相当于 p=new int;*p=10;
***
delete

释放一个int型的动态变量：deelte p;
释放N个元素的动态一维数组: delete[]p;
释放N行M列的动态二维数组：for(i=0;i<N;i++)
                            delete []q[i];
                        delete []q;

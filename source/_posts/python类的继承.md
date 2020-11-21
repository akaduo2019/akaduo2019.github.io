---
title: 类的继承
date: 2020-10-30 18：39
tags:
- notes
categories:
- python
---
创建子类的实例时，Python首先要完成的任务时给父类所有属性赋值。为此，子类的方法__init__()需要父类施以援手：

```py
class Father():
    def __init__(self,height,weight,age):
        --snip--
class Son(Father):
    def __init__(self,height,weight,age):
        super().__init__(height,weight,age)
        --snip--
```

创建子类时，父类必须包含在当前文件中，且位于子类前面。
定义子类时，必须在括号内指定父类名称。
super()是一个特殊函数，帮助Python将父类和子类关联起来：这行代码让Python调用父类的方法__init__(),让子类实例包含父类的所有属性。

***
私有属性和私有方法

在属性名或方法名前加上__

***
1.直接调用父类属性和方法
2.重写父类属性和方法
3.强制调用父类私有属性方法
4.调用父类的__init__方法
5.继承父类初始化过程中的参数

>详见<https://blog.csdn.net/yilulvxing/article/details/85374142>

---
title: c++中的string类型
date: 2020-8-30 09：16
tags:
- notes
categories:
- c++
---

```c++
  string s1;
  string s2("student");
  
  cin >> s1; //可用getline(cin,s1)读入待空格的串
  cout << s2.length() <<endl;//string 串名.length() 求串长

  s2.insert(7,"&Teacher");//向串s2下标为7处中插入 &Teacher
  cout << s2<< endl;//输出结果为student&Teacher

  s2.replace(2,4,"ar");//将串s2的 以下标2处为起始位置,长度为4的子串  替换成ar
  cout << s2<< endl;//输出结果为start&Teacher

  s1=s2.substr(6,7);//提取串s2中 从下标6开始，长度为7的子串 ，并赋值给s1
  cout << s1 << endl;//输出结果为Teacher

  int pos =s2.find(s1);//在串s2中寻找s1串是否存在,若存在则返回s1串的第一个字符在s3中的下标

  s2.erase(5,8);//删除串s2的从5下标开始的长度为8的子串


```

***
>c_str()函数返回一个指向正规C字符串的指针, 内容与本string串相同.

这是为了与c语言兼容，在c语言中没有string类型，故必须通过string类对象的成员函数c_str()把string 对象转换成c中的字符串样式。

注意:一定要使用strcpy()函数 等来操作方法c_str()返回的指针

1、比如:最好不要这样:

char* c;

string s="1234";

c = s.c_str(); //c最后指向的内容是垃圾，因为s对象被析构，所以不能直接利用c_str返回的字符串，要利用strcpy等函数进行复制后再使用

2、其内容被处理应该这样用:

char c[20];

string s="1234";

strcpy(c,s.c_str());

这样才不会出错，c_str()返回的是一个临时指针，不能对其进行操作。

3、再举个例子c_str() 以 char* 形式传回 string 内含字符串如果一个函数要求char*参数，可以使用c_str()方法:

string s = "Hello World!";

printf("%s", s.c_str()); //输出 "Hello World!"

---
title: 字符串
date: 2020-9-14 10：56
tags:
- notes
categories:
- python
---
一、修改字符串大小写

1. string.title()  令首字母大写
2. string.upper()  令字符串字母全部改为大写
3. string.lower()  令字符串字母全部改为小写

***
二、删除空白(泛指任何非打印字符,如空格、制表符和换行符)

1. string.rstrip() 删除字符串末尾空白
2. string.lstrip() 删除字符串开头空白
3. string.strip()  同时删除字符串两端的空白
注:但这种删除只是暂时的，接下来再次访问sting的值时会发现仍包含多余空白。若需要永久删除整个字符串中的空白，必须将删除操作的结果存回变量中
如:string=string.rstrip()

---
title: Django
date: 2021-9-25 9:10
tags:
- notes
categories:
- python
---

## 创建一个Django项目

- cd 对应的python虚拟环境文件夹

- workon 虚拟环境

- django-admin startproject 项目名

- cd 项目名文件夹

- 创建app

  - python manage.py startapp app名
  - 或 django-admin startapp app名

## 实现一个请求

- 注册一个路由

  - 在urls中

    - url(参数1，视图函数)

      - 参数1:匹配规则 正则
      - 视图函数:对应views中的一个函数，注意不写函数的括号

- 去views实现对应的视图函数

  - 第一个参数是request
  - 永远记得返回response

## 模板配置

- 在App中进行模板配置

  - 需要在App的根目录创建templates文件夹即可
  - 如果想让代码自动提示，只需标记文件夹为模板文件夹

- 在项目目录进行模板配置

  - 需要在项目目录创建templates文件夹并标记
  - 需要在settings中进行注册

- 在开发中使用第二种

  - 模板可以继承，复用

## 路由配置

- 项目如果逻辑过于复杂可以进行拆分
  - 拆分为多个App
  - 拆分多个urls

    - 在App中创建urls

      - urlpatterns = [] 路由规则列表
      - 在根urls中进行子路由的包含
    - 子路由使用

      - 跟路由规则 + 子路由规则

## 数据操作 增删改查

- 存储

  - save()

- 查询

  - 查所有 objects.all()
  - 查单个 objects.get(pk=xx)

- 更新

  - 基于查询的
  - 查好的对象，修改属性，然后save()

- 删除

  - 基于查询的
  - 调用delete()

## Django shell

- 集成了python环境的shell终端
- 通常在终端中做一些调试

## 如何调试bug

- 看日志

  - 先看第一条
  - 再看最后一条

- 梳理思路

  - 程序在哪一个位置和预期出现偏差

## 关系型数据库表关系

- 1:1 一对一
- 1:M 一对多
- M:N 多对多


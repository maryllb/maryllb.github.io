---
layout: post
title: Git核心理念&原理介绍
date: '2020-01-13 13:38:20 +0800'
categories: technology
tags: ubuntu apache mysql php phpmyadmin git
img: https://i.loli.net/2021/03/09/bUmYxyKEiqhOVeW.png
themecolor: "#fff"
themetextcolor: "#000"
describe: 玩转git
---

## Git的核心

+ 文件(Immuntable)
+ 快照(Immuntable)
+ 分支

### 文件(Immuntable)

  在git中文件是不可修改的。即，只能新建文件进入内容，不允许修改其内容。一旦允许修改，文件可能就会丢失。如果文件想修改，可能会分叉。
  
  ![git-1-1.jpg](https://i.loli.net/2020/01/14/qRNl8dJOvLWbDiw.jpg)

### 快照(Immuntable)

  在git文件夹（即快照）也是不可修改的。
  如果一个A文件夹中有a.txt、b.txt、c.txt，一旦你删除c.txt文件，它会新建一个快照中包含a.txt、b.txt。

  ![git-1-2.jpg](https://i.loli.net/2020/03/19/ivB9FYNKkw1VjZh.jpg)

### 文件与快照的关系

A.txt内容为123，修改一次后还是A.txt内容为456。

快照里不存文件，只存文件的引用。假设快照里有A.txt引用是看指向哪个版本的。

  ![git-1-3.jpg](https://i.loli.net/2020/03/19/Xi9BrRl1kqt8NZU.jpg)

### 分支

分支只要做历史版本控制。分支里没有文件，分支存的是快照的引用，但分支是可变的。

  ![git-1-4.jpg](https://i.loli.net/2020/03/19/HcXoCahvUReELgB.jpg)

## Git的特点

① 提交后东西不会丢，带给大家安心的感觉

② 分支的成本低（支持多任务）

③ 分布式

git做了社交，是行业的标准。

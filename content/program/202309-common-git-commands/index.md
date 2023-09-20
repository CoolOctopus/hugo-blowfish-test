---
title: '常用git命令行'
date: 2023-09-18T18:03:33+08:00
draft: false
description: ""
categories: ["notes","编程笔记"]
tags: ["git","命令"]
---

## git clone
1. 作用：该命令的可以帮助我们将仓库下载到本地。
2. 用法：`git clone [URL]`
```cmd
git clone https://github.com/xxxxx/xxxx.git
```
![Github仓库链接位置](img/common-git-commands-01.jpg)
> Tips：建议使用梯子或镜像站，因为在Github官网获取到的仓库链接(如上图)访问速度通常很慢，作者表示也深受其害。

## git submodule
该命令用于子模块操作添加、删除、更新等
1. 添加：`git submodule add [URL] [PATH]`，（类似于`git clone`，可以将其他仓库下载到本地作为子模块使用）

2. 更新：`git submodule deinit [URL] [PATH]`

3. 删除：`git submodule deinit [URL] [PATH]`，若有本地修改则须加上参数`--force`（完整删除过程可参考[文章](#Refrence)）

注：\[URL\]为仓库链接，\[PATH\]为存储路径。

## git remote
该命令用于远程仓库的管理相关操作
1. 查看：`git remote -v`，可查看当前添加的远程仓库

2. 添加：`git remote add [NAME] [URL]`，

3. 修改链接：`git remote set-url [NAME] [URL]`

注：\[NAME\]为远程名称，常用名称为origin，`URL`为仓库网址。

## git branch
该命令用于分支操作
1. 查看：`git branch`，可查看当前分支，前面会有\*标注

2. 创建：`git branch [NAME]`，可创建分支，命名为\[NAME\]

分支相关操作：<br>
切换：`git checkout [NAME]`，切换到\[NAME\]分支<br>
合并：`git merge [NAME]`，将\[NAME\]分支合并到主分支


## git commit
该命令将暂存区内容添加到本地仓库中。<br>
用法：`git commit -m "[message]"`<br>
注：\[message\] 可以是一些备注信息。

## Refrence
* [[Git] 如何优雅的删除子模块](https://www.jianshu.com/p/ed0cb6c75e25)
* [git的add、commit、push的详细介绍](https://www.jianshu.com/p/2e1d551b8261)
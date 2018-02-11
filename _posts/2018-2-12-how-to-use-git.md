---
layout: post
#标题配置
title: atom+git+github写博客
#时间配置
date:   2018-2-12 01:00:00 +0800
#大类配置
categories: 笔记
#小类配置
tag: atom，git
---

* content
{:toc}


这篇笔记记录了我用github pages写博客的过程。 ~~环境是ubuntu17.10, windows还没试过，后续在试试~~ 。编辑器用的github自家的atom，漂亮，和git搭配的很好。
##  github准备
1. 首先注册一个github账户
2. 然后在github页面右上角+号，New repository新建 **版本库(repository)**,版本库可以看作一个项目的一个大目录。这里我们用github写博客，版本库的名称要设置成 *username*.github.io 用自己的用户名换掉 *username*

> 这篇文章后的 **所有** username全都替换成你自己的用户名

## 安装必要的软件
1. 安装git；  ubuntu终端：sudo apt-get install git  
windows： 去git官网下载安装包，安装时一直next保持默认就好。启动git bash，后面的shell命令（以$开头）均在git bash中执行。

2. 安装atom： 官网上下载安装包直接安装即可

## 把创建的repository克隆到本地
```
$ git clone https://github.com/username/username.github.io
```
## 编写hello world
```shell
$ cd username.github.io  
$ echo "Hello World"   > index.html  
$ git add index.html
$ git commit -m "your commit"
$ git push origin master  #将本地修改提交到github服务器
### 然后根据提示输入github用户名与密码
```
然后打开博客网站http://username.github.io  
可能会有延迟，等一会刷新就能看到Hello World博客啦

## git了解
基本概念  
版本库：就是文件修改的历史记录的集合  
分支： 历史记录是 一根时间线的一系列文件，分支就是这个时间线的分支

```shell
$ git add your_filename1 #把你修改的文件提交到暂存区
$ git add your_filename2 #可以连续提交多个，甚至文件夹
$ git commit -m "your_commit" #把暂存区的修改过的文件提交到版本库，并把本次操作记录为“your_commit”
$ git push origin master #把本地的修改同步到github上
```

## 下载jekyll模板
可以先用我的试试，也可以从网络上下载jekyll主题模板。
```shell
$ git clone https://github.com/stacezhou/stacezhou.github.io
##修改stacezhou.github.io文件夹下大的_config.yml
```
然后把stacezhou.github.io文件夹下的所有文件复制到你自己的username.github.io下面
## 上传到github服务器上
```shell
$ cd username.github.io
$ git add ./*
$ git commit -m "init"
$ git push origin master
```
然后打开你自己的博客（有延迟）就发现已经使用好模板了。

## 写一篇博客
在文件夹username.github.io/posts 文件夹下添加一个md文件，名称类似2018-9-14-happy-birthday.md  
然后提交修改
```shell
$ git add 2018-9-14-happy-birthday.md
$ git commit -m "your commit"
$ git push origin master
```

## atom配置
编辑>Preferences>安装（快捷键Ｃtrl+，）
搜索并安装
* git-plus
* markdown-preview-plus
* markdown-writer
* platformio-ide-terminal
## atom 使用
* Ｃtrl+shift+Ｍ 可以打开markdown预览界面  
* atom下底左端+号可打开terminal  
* 右下角可打开git界面  
* atom左边中部鼠标移向的时候会有箭头，打开project面板（文件目录）右击选择Ａdd project folder并选择你的username.github.io文件夹，atom会自动识别
  - 新建的文件会显示成绿色
  - 修改的文件会显示成黄色
  - 在atom界面中提交更改
    - 改新建或修改的文件或文件夹上右击选择git add+commit 在弹出的commit界面上输入你的注释（注意要输入以引号包括的字符串）然后保存Ｃtrl+Ｓ
    - 在终端中git push origin master提交到github


## 参考：
[如何快速搭建自己的github.io博客](http://blog.csdn.net/walkerhau/article/details/77394659)  
[写作环境搭建(git+github+markdown+jekyll)](https://site.douban.com/196781/widget/notes/12161495/note/264946576/)  
[Atom中设置你的snippet，atom技巧](https://www.cnblogs.com/RuMengkai/p/6554760.html)

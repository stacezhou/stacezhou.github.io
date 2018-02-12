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


这篇笔记记录了我用github pages写博客的过程。环境是ubuntu17.10,windows还没试过，后续在试试。编辑器用的github自家的atom，漂亮，和git搭配的很好。
##  github准备
1. 首先注册一个github账户
2. 然后在github页面右上角+号，New repository新建 **版本库(repository)**,版本库可以看作一个项目的一个大目录。这里我们用github写博客，版本库的名称要设置成 *username*.github.io 用自己的用户名换掉 *username*

> 这篇文章后的 **所有** username全都替换成你自己的用户名

* 安装必要的软件
1. 安装git；  ubuntu终端：sudo apt-get install git
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
$ git push origin master  #将本地修改提交到github服务器
### 然后根据提示输入github用户名与密码
```
然后打开博客网站http://username.github.io  
可能会有延迟，等一会刷新就能看到Hello World博客啦

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
模板一般都会有说明：一般都是在文件夹
username.github.io/_posts 文件夹下添加一个md文件，名称类似2018-9-14-happy-birthday.md

## 参考：
[如何快速搭建自己的github.io博客](http://blog.csdn.net/walkerhau/article/details/77394659)  
[写作环境搭建(git+github+markdown+jekyll)](https://site.douban.com/196781/widget/notes/12161495/note/264946576/)  

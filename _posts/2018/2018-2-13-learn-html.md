---
layout: post
#标题配置
title: Html学习
#时间配置
date:   2018-2-13 00:00:00 +0800
#大类配置
categories: 语言
#小类配置
tag: Html，笔记
---

* content
{:toc}



参考[HTML教程](http://www.w3school.com.cn/html/index.asp)
**HTML标记语言利用标签来描述网页**  
* HTML标签由 **尖括号** 包括
* html标签分为两类，两边成对出现的，为 **封闭式的**   例如：
    <body> 和</body>

* 也有 **非成对** 出现的，称为 **自封闭** 格式是例如  
    <hr />

* 所有字母为 **小写**
* 标签里可以有属性，对标签内的内容进一步描述，例如
    <a href="https://baidu.com">超链接（指向百度）</a>


```html
<!DOCTYPE html><!--表示文档类型是html-->
<html>
  <head><!--头信息，头信息不被显示在页面上-->
    <title> Html示例 </title> <!--标题，被显示到浏览器的标题栏-->
	</head>
	<body>
		<p>第一段第一行<br />第一段第二行</p>
    <p>第二段第一行<br />第二段第二行</p>
    <hr /> <!--水平分割线 -->
    <p><a href="https://baidu.com">超链接（指向百度）</a></p>
    <p><a href="https://baidu.com" target="_blank"><img src="http://www.baidu.com/img/baidu_logo.gif" /></a></p>    
	</body>
</html>
```


## Html常用标签索引
* 框架类
  - html
  - body
  - head
  - title
  - <!--zhushi-->
* 图像链接
  - a href="https://baidu.com"
  - img src=“http://baidu.com”
* 文字
  - h 定义标题h1到h6
  - p 段落
  - div?
  - strong 强调
* 列表？
  - ul
  - li
* 表格
  - table
  - tr
  - td
* 表单
  - form
  - input
  - select
  - textarea

## 自封闭的html标签
* br hr
* col img
* area link meta *base*
* frame input param
* DOCTYPE *isindex*
* *basefont*

---
layout: post
#标题配置
title: HTML初识
#时间配置
date:   2018-2-13 00:00:00 +0800
#大类配置
categories: html
#小类配置
tag: Html，笔记，网络
---

* content
{:toc}


**建议阅读[HTML基础](http://www.w3school.com.cn/html/html_basic.asp)后，以其中的例子对照来看本文**

我主要从[w3cschool](http://www.w3school.com.cn)学习网页知识，以后只记录心得摘要，具体参考W3cschool.  
另外，W3cschool的移动端app非常好用，可以把大多数教程离线阅读。内容比网页版更丰富，甚至包括C，python，各类数据库，linux等上千个教程。大多为免费资源，极少数付费，但也非常便宜，我上次购买一个只需1元。安利一下。

### 网页的组成
下面是我的心得，与教程可能些许不同。我主要类比编程中的对象来解释。
1. **网页** 是各种网页 **元素** 的集合，元素之间有嵌套包含关系。
2. 元素有各种属性：内容，大小，颜色，位置等等。浏览器把这些元素的属性表现出来，是我们看到的网页。
3. 元素有各种方法，方法决定元素的行为：例如属性的改变（可能的效果是变色，运动，改变内容）

上面是我认为理解HTML+CSS+JavaScipt的窍门？

### 元素的组成结构

```html
<p>This is a paragraph</p>
<a href="http://www.w3school.com.cn">This is a link</a>
<img src="w3school.jpg" width="104" height="142"></img>
上面的图片元素也可以简写成
<img src="w3school.jpg" width="104" height="142" />
甚至
<img src="w3school.jpg" width="104" height="142">
```

1. 元素=开始标签+内容+结束标签
2. 标签内的字母表示元素的类型，例如上面的p为段落，a是链接。开始标签内还定义该元素的属性，例如a元素的href属性
3. 开始标签和结束标签内的文字是该元素携带的文字属性。没有文字的元素（如图片，分割线）为空。这类 **空元素** 可以省略结束标签

### 网页的结构

```html
<!doctype html>
<html>
  <head>
    <title>
      网页标题
    </title>
  </head>
  <body>
    网页内容
  </body>
</html>
```
![](http://www.w3school.com.cn/i/ct_htmltree.gif)
### 样式与CSS
样式就是元素在网页上可以看见的属性，（如大小，颜色，超链接的指向不属于此类）
样式表把各类元素的样式放在一起（一个表格中），就是css

### javascript

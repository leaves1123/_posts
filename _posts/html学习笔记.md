---
title: html学习笔记
date: 2023-10-27 11:19:40
tags: 
    - note
    - html
categories: learn
sticky: 300
---

<h1 align="center">HTML部分</h1>

## HTML是什么？

>html(Hyper Text Markup Language), 超文本标签语言, 语言内容由标签组成, 标签通常成对出现, 比如&lt;a&gt;&lt;/a>, 少数是单标签, 主要用于搭建网络框架, 通常与css和javascript联用

注意: 对于成对的标签, 其是不可以交叉的, 比如:
```html
<!--False-->                    <!--True-->
<head>                          <head>
    <title>                         <title>
    </head>                          </title>
</title>                        </head>
```
<!--more-->
## 常用的标签(基础)

```html
标题标签(六级标题)               粗线标签
<h1></h1> - <h6></h6>          <strong></strong> or <b></b>

段落标签
(段落与段落之间有较大空隙)        斜体标签
<p></p>                        <i></i>

换行标签                        下划线标签
<br>                           <u></u>

水平线标签
<hr width="px or %">

区块标签(无具体含义, 只是划分了一个区域, 注意与别的标签的联动用法)
<div></div> 一行只能有一个, 大区块
<span></span> 一行能有多个, 小区块

图片标签
<img src="图像url" alt="图片显示错误时提示文字" title:"鼠标悬停时提示文字"
width="" height="" border="" border-radius=""> 相对路径+绝对路径+网页路径, 
src为必须属性, 属性与属性之间以空格分隔

链接标签
<a href="跳转目标url(相+绝+网页)" target="窗口弹出方式(#为空链接)" title="鼠标悬停时提示文字">文本 or 图像</a>

锚点链接
<a href="#name">text</a> --> <h id="name">text</h>

注释
<!--  -->

特殊字符
不换行空格: &nbsp;   <: &lt;      >: &gt;

...
有些样式也可以通过css控制
```

## 常用的标签(一般)

### 表格
显示数据, 结构如下(实际上用得少, 考虑使用css)
```html
       对齐  单元格内容与单元格间距 单元格间距
<table align="" cellpadding="" cellspacing="" width="" height="" border="">
    <tr> <!--<tr>表示一行-->
        <td></td> or <th></th> <!--<td>是普通单元格; <th是表头单元格, 用于首行, 加粗居中效果>-->
    </tr>
</table>
```
表格还可以分为表头`<thead>`和表体`<tbody>`

### 合并单元格

<table width="50%" align="center">
    <tr>
        <td>跨行合并</td>
        <td>rowspan</td>
    </tr>
    <tr>
        <td>跨列合并</td>
        <td>colspan</td>
    </tr>
</table>

### 列表
多使用无序列表, 后面用css
<table align="center">
    <tr>
        <td>无序列表</td>
        <td>&lt;ul></td>
    </tr>
    <tr>
        <td>有序列表</td>
        <td>&lt;ol></td>
    </tr>
    <tr>
        <td>自定义列表</td>
        <td>&lt;dl></td>
    </tr>
</table>

语法:
```html
无序列表                有序列表              自定义列表(用于名词解释)
<ul>                   <ol>                 <dl>
    <li>内容1</li>        <li>内容1</li>        <dt>名词</dt>
    <li>内容2</li>        <li>内容2</li>        <dd>解释1</dd>
    <li>内容3</li>        <li>内容3</li>        <dd>解释2</dd>
</ul>                  </ol>                </dl>
```

### 表单
收集信息; 表单域`<form>`+表单控件(元素)+提示信息
```html
<form action="url" method="提交方式(post or get)" name="表单域名称">
    +元素
</form>
```

表单常用元素:
`<input>`

```html
<input type=""> <!--单标签-->
```
![type_value](input_attribution.png "type value")

标签`<label>`
```html
<input type="radio" name="key" id="id"> <!--元素的id需和text的id相同-->
    <label for="id">text</label>
效果: 单击text即相当于单击元素
```

下拉列表`<select>`
```html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
</select>
```

文本域`<textarea>`<br>
~一个更大的文本框~

```html
<textarea rows="3" cols="20"> <!--占据3行20字符-->
    text
</textarea>
```
以上基本不会使用(难看), 使用css

### 查阅相关文档
[W3C](https://www.w3school.com.cn/)
[MDN](https://developer.mozilla.org/zh-CN/)


<hr>


<br><br>



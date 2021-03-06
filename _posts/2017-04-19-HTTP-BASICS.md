---
layout: post
title: "HTTP基础"
categories: php
---
# HTTP协议的用途
网页运行在HTTP(超文本传输协议)之上。这个协议支配网页浏览器如何从服务器请求文件和如何从服务器发回文件。
# HTTP协议的运行过程
当浏览器请求一个网页时，它会发送HTTP请求消息到网页服务器。请求消息包含一些头信息，有时也会包含一些内容。网页服务器用一个回复消息来响应，它总是包含头部信息并且经常包含内容。
# HTTP请求
* 首行
```
GET /index.html HTTP/1.1
```
该行指定了一个HTTP命令，叫做"方法"，紧跟着的是文档地址和所使用的HTTP版本。
这个例子中，请求使用了GET方法和HTTP1.1版本来请求index.html文档。
* 头部信息
```
User-Agent: Mozilla/5.0 (Windows 2000; U) Opera 6.0 [en]
Accept: image/git, image/jpeg, text/*, */*
```
首行过后，在请求包含的头部信息来告诉服务器该请求中额外的数据。
User-Agent头提供了浏览器的相关信息，Accept头制定了浏览器可以接受的MIME类型。在头部后面，请求包含一个空行来指明头部的结束。
* 数据
	
	针对方法可用的情况下(例如POST方法)，请求可以包含额外的数据。如果请求不包含任何数据，它将以空行结束。

# HTTP响应
* 流程

	网页服务器收到请求，处理它，然后发送响应。
* 首行
```
HTTP/1.1 200 OK
```
这行指定了协议版本、状态码和状态码的描述。在例子中的情况下，状态码是200，意味着请求是成功的(因此描述是OK)。
* 头部

	在状态行后面，响应包含了给客户端额外信息的头部。例如：
```
Date: Thu, 31 May 2012 14:07:50 GMT
Server: Apache/2.2.14 (Ubuntu)
Content-Type: text/html
Content-Length: 1845
```
服务器头部提供了网页服务器软件的信息，同时Content-Type头指定这个响应数据的MIME类型。
* 数据

	头部过后，响应包含一个空行，紧接着是请求成功的数据。

# 常用HTTP方法
最常用的HTTP方法是GET和POST。GET方法用来检索信息，例如服务器上的一个文档、一张图片或一个数据库查询的结果。POST方法意指传递信息，例如要存储信用卡号码或信息到服务器数据库。GET方法等同于用户在网页浏览器上输入一个URL或单击一个链接。当用户提交一个表单时，GET和POST方法都可以用，只需为form标签指定method属性。

# 参考资料：
[<<PHP编程>> Kevin Tatroe  Peter Maclntyre  Rasmus Lerdorf](https://pan.baidu.com/s/1gfh3uWN)

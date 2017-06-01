---
layout: post
title: "EGPCS变量"
categories: php
---
# 定义
服务器配置和请求的信息(包含表单参数和cookie)以不同的方式在PHP脚本中访问，这些信息放在一起被标识为EGPCS(environment、GET、POST、cookie和server)。

PHP可创建包含EGPCS信息的6个全局数据。
# $_COOKIE
包含作为请求中cookie数值的部分，数组的键名是表单参数。
# $_GET
包含作为GET请求中参数的部分，数组的键名是表单参数。
# $_POST
包含作为POST请求中参数的部分，数组的键名是表单参数。
# $_FILES
包含上传文件的信息。
# $_SERVER
包含网页服务器中有用的信息。
# $_ENV
包含环境变量数值，数组的键名是环境变量的名字。
# 可见性
这些变量不仅仅是全局的，而且在函数定义内部也是可见的。
# $_REQUEST
$_REQUEST数组也会自动创建。该数组是包含$_GET、$_POST和$_COOKIES所有信息的一个组合。
# 参考资料：
[<<PHP编程>> Kevin Tatroe  Peter Maclntyre  Rasmus Lerdorf](https://pan.baidu.com/s/1gfh3uWN)

---
layout: post
title: "命令systemctl"
categories: linux
---

- 使某服务自动启动 systemctl enable httpd.service

- 使某服务不自动启动 systemctl disable httpd.service

- 检查服务状态 systemctl status httpd.service

- 显示所有已启动的服务 systemctl list-units –type=service

- 启动某服务 systemctl start httpd.service

- 停止某服务 systemctl stop httpd.service

- 重启某服务 systemctl restart httpd.service

[参考链接](http://blog.csdn.net/kenhins/article/details/74518978)

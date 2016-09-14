---
layout : post
title : shell基本命令
category : linux
tag : linux
---


* rpm -qa   //查看安装哪些软件
* rpm -ql  软件名   //查询已安装软件包都安装到何处
## 查询一个已安装软件包的信息
语法格式： rpm -qi 软件名
举例：
* [root@localhost RPMS]# rpm -qi lynx
## 查看一下已安装软件的配置文件；
语法格式：rpm -qc 软件名
举例：
* [root@localhost RPMS]# rpm -qc lynx
## 查看一个已经安装软件的文档安装位置：
语法格式： rpm -qd 软件名
举例：
* [root@localhost RPMS]# rpm -qd lynx
## 查看一下已安装软件所依赖的软件包及文件；
* 语法格式： rpm -qR 软件名

## curl使用
* curl -O https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-3.0.6.tgz   //下载
* tar -zxvf mongodb-linux-x86_64-3.0.6.tgz  //解压

* ll -list |head -10 显示最近前10条

## linux命令行快捷键：
* ctrl+a   //移到行首
* ctrl+e   //移到行尾
* ctrl+l    //清屏
* ctrl+c   //删除整行


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


## 脚本编程语言的例子有awk、Perl、Python、Ruby、Shell
>Sed：Stream Editor  流式编辑器 又称行编辑器，每次只编辑一行。Sed工作是在“模式空间”中进行的，并不操作源文件。对源文件无危害。
Linux ：
tr同sed类似  //用来替换字符、删除重复的字符
unset        //删除变量
who        //显示目前登录系统的用户
last      //显示用户登录情况

## shell执行的3种方法：
>1.绝对路径执行
#/data/shell/hello.sh
2.#cd /data/shell
a . #bash hello.sh
b.  #sh hello.sh
c.  #. hello.sh







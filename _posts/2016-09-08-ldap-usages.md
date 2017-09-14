---
layout:     post
title:      ldap登录验证
keywords:   Cache，Asynchronous，Concurrent
category:   ldap
description: 
tags:		[web, 服务器]
---

# ldap登录验证实现
以laravel框架迁入ldap服务为例，
若在windows上部署，则pc需安装OpenLDAPforWindows_x64.exe，搭建好本地ldap服务。另外，安装LdapAdmin1.1.exe进行连接ldap服务进行测试。
这里讲的只是本地简单部署ldap服务，然后使用可视化工具进行测试，服务是否OK。
接下来要讲的是，代码层如何实现ldap的使用。
1.首先使用composer工具加载adldap2组件，在composer.json文件配置adldap2版本，然后在命令行执行composer update.
2.当composer加载镜像执行完成后，在php.ini配置文件，开启ldap扩展。
3.以上2点弄好后，便可在代码层直接使用ldap服务.

**问题1：当使用ldap_bind方法时，报“protocal error”?**
答：
- 需在安装的openLDAP下的根目录slapd.conf中间行添加“allow_bindV2”.
- 然后重启openldap.

**问题2：当使用ldap_add方法时，报“strong(er) Authention required”.**
答：
此时需要做ldap_bind强绑定。

**问题3：当使用ldap_add方法时，报“object class violation”.**
答：即是缺少参数objectclass. ldap_add参数需包含cn、sn、uid、objectclass等。



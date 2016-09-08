---
layout:     post
title:      安全漏洞引言
keywords:   Cache，Asynchronous，Concurrent
category:   secure  
description: 
tags:		[web, 服务器]
---

目前互联网兴起，也带动了各大网站的建立，然而我们无可厚非要关注的就是网络安全型问题，作为目前网络攻击方式大概有哪些呢？下面总结一一列举下。

1. sql注入
2. xss注入
3. 业务逻辑注入
4. xpath注入
5. url、参数、js分析攻击
6. 绕过认证
7. csrf  重要功能增加确认操作或重新认证，例如支付交易、修改手机号码等 加验证码  每个会话中使用强随机令牌（token）来保护。 检验HTTP Referer
8. 会话攻击  采用强算法生成ID，设置回话过期时间  设置好cookie属性：secure、httponly来防御嗅探和阻止js操作


而作为防范于未然，采取的监控产品大概有：
cacti、nagios、zabbix监控产品



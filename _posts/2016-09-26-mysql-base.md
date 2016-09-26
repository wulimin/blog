---
layout : post
title : mysql使用备忘
category : sql
tag : sql
---

>mysql导入导出：
在导出mysql sql执行文件的时候，指定一下编码格式：
mysqldump -uroot -p --default-character-set=utf8 mo（dbname） > E://xxxx.sql
导入：
mysql -u root -p --default-character-set=utf8
use dbname
source /root/newsdata.sql

>mysql将unix时间戳和时间字符串的相互转化
mysql将unix时间戳转化成时间字符串:
select FROM_UNIXTIME(1349664611,'%Y-%m-%d %H:%i:%s')
mysql将时间字符串转化为unix时间戳:
select UNIX_TIMESTAMP('2012-10-25 12:00:12')


























---
layout : post
title : laravel框架使用
category : php
tag : php
---

>IOC( inversion of control)控制反转 是面向对象编程中的一种设计原则，可以用来减低计算机代码之间的耦合度。
其中最常见的方式叫做依赖注入（Dependency Injection，简称DI），还有一种方式叫“依赖查找”（Dependency Lookup）。通过控制反转，对象在被创建的时候，由一个调控系统内所有对象的外界实体，将其所依赖的对象的引用传递给它。
外觀模式（Facade pattern），是軟件工程中常用的一種軟件設計模式，它為子系統中的一組接口提供一個統一的高層接口，使得子系統更容易使用。
获取器和修改器
getFooAttribute 、setFooAttribute


>所以有了控制反转（Inversion of Control）和门面模式（Facade），实际还有服务提供器（Service Providers）和别名（Alias），我们创建自己的类库和扩展 Laravel 都会方便很多。

>这里总结一下创建自己类库的方法：

* 在 app/library/MyFoo 下创建类 MyFoo.php
* 在 app/library/MyFoo/providers 下创建 MyFooServiceProvider.php
* 在 app/library/MyFoo/facades 下创建 MyFooFacade.php
* 在 app/config/app.php 中添加 providers 和 aliases

>seed填充数据，使用php artisan执行前，请先使用composer dump-autoload加载下


* \DB::connection('mysql_crm')->enableQueryLog();
* dd(\DB::connection('mysql_crm')->getQueryLog());













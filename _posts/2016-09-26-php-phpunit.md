---
layout : post
title : phpunit使用介绍
category : php
tag : php
---

>phpunit --testsuite --coverage-html tests/coverage   查看代码覆盖率
@depends 建立依赖关系
@dataProvider  使用返回迭代器对象的数据供给器、 使用带有命名数据集的数据供给器、使用返回数组的数组的数据供给器

.   当测试成功时输出。
F  当测试方法运行过程中一个断言失败时输出。
E  当测试方法运行过程中产生一个错误时输出。
R  当测试被标记为有风险时输出（参见第 6 章）。
S  当测试被跳过时输出（参见第 7 章）。
I   当测试被标记为不完整或未实现时输出（参见第 7 章）。

setUp()  运行某个测试方法前，会调用
tearDown()  当测试方法运行结束后，不管是成功还是失败，都会调用

数据库测试的四个阶段：
1.建立基境(fixture)
2.执行被测系统
3.验证结果
4.拆除基境(fixture)

基境(fixture)是对开始执行某个测试时应用程序和数据库所处初始状态的描述。

phpunit.xml文件配置：
<testsuites name="" file="">
  	<testsuite>
	</testsuite>
</testuites>

单元测试优点：
1.修复补丁
2.能发现边缘性问题
3.测试提供了一种方法叫做快速捕捉退步（Regression）,能保证退步不会重现。
Regression Test(回归测试)
在软件项目中，如果一个模块或功能以前是正常工作的，但是在一个新的构建中出了问题，那这个模块就出现了一个“退步”（Regression），从正常工作的稳定状态退化到不正常工作的不稳定状态。
4.提供API范例，方便测试文档编制。


















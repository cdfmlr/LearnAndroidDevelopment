# 第 0 周计划
## 概述
这周先主要是立项的那些麻烦的事情，学习相关知识可以不用太着急，慢慢来就行了。还有就是希望大家能掌握 GitHub 的基本使用。

## 事务
#### 立项准备

* 完成申请表
* 完成PPT

## 学习

### GitHub

> GitHub 大家可能都听说过，很吊的开发者网站。世界上很多知名开源项目都放在 GitHub，所以我们学习一下它会很有好处。  

> 这个我之前忘了说了，但我计划以后都使用 GitHub 来完成大创项目，所以学一下GitHub。  

什么是 GitHub?
[漫话：如何解释什么是Git和GitHub？](https://mp.weixin.qq.com/s?__biz=Mzg3MjA4MTExMw==&mid=2247485189&idx=1&sn=fbe5c12bb3ebbb61741c6f91082d3557&chksm=cef5f4b3f9827da5423175abe0e114696605d0fe832ddcb9b3fc3e5e84b85b23f4115ac331c1&scene=90&xtrack=1&sessionid=1554110118&subscene=93&clicktime=1554110601&ascene=56&devicetype=iOS12.1.4&version=1700032a&nettype=WIFI&abtest_cookie=BAABAAoACwASABMABQAjlx4AVpkeAMqZHgDZmR4A3JkeAAAA&lang=zh_CN&fontScale=100&pass_ticket=ZgSgi5nXU2danIg1smld4bT6wUi1AWJYYdU%2FVrAsGwMvWg7MW%2BjMmyXb4YDnwb9R&wx_header=1)
怎么用GitHub？
[Github 简明教程 | 菜鸟教程](http://www.runoob.com/w3cnote/git-guide.html)
想学习更多关于GitHub？（这个可以看自己的情况选学）
[Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
还有我的笔记可以参考：
[mine Note](http://cr0123.gz01.bdysite.com/Notes.html)

#### Java

> Android 应用的逻辑使用 Java 编写，所以练好 Java 是关键。  
> 这一周我们先大概去认识 Java，了解 Java 程序长啥样。  

* Java 环境的安装、配置
* Java 程序的运行（实现一个 Hello World）
* Java 的基础语法（读懂 Hello World 的每一个部分）
* Java 面向对象的基本概念

【参考】[Java 教程 | 菜鸟教程](http://www.runoob.com/java/java-tutorial.html)（学到**Java 对象和类**）

#### XML（这个在劳动节前学完就行）

> Android 应用的样式使用 XML 编写，所以需要对 XML 有一定的了解。  

> 考虑到 XML 不太好学，而 HTML 和它比较接近，所以我们可以先看一下 HTML，再学 XML  

* 了解 HTML 的基本用法
	【参考】[HTML 教程 | 菜鸟教程](http://www.runoob.com/html/html-tutorial.html)（**HTML 属性**前必看，之后的选看）
* 了解 XML 的基础规则
	 【参考】[XML 教程 | 菜鸟教程](http://www.runoob.com/xml/xml-tutorial.html)（学到 XML JavaScript 之前，之后的选看）


## 练习
> 这个主要是练习基础语法和编程思想。  
> 由于我们这周才开始学的 Java，所以暂时可以不用 Java 去写（以后我们每周都用 Java 去写题练习 Java 的使用）。  

* 题目： [负二进制转换 | 力扣](https://leetcode-cn.com/contest/weekly-contest-130/problems/convert-to-base-2/)

* 题解：[leetcode周赛130 |  题解速递](https://mp.weixin.qq.com/s/3oIU1Uvfj1shoh9RCiCV8w) 里面的第二题

* 我的解法:
我的代码(用Go语言实现)和他写的答案差异很大，但也可以通过：
```go
func baseNeg2(N int) string {
	if N == 0 {
		return "0"
	}
	ans := ""
	for N != 1 {
		t := 0
		if (N < 0) && (N%(-2) < 0) {
			t = (2 - N) % 2
			N = (2 - N) / 2
		} else {
			t = N % (-2)
			N = N / (-2)
		}
		ans = string(0x30+t) + ans
	}
	ans = "1" + ans
	return ans
}
```

## 参考阅读
1. 这篇文章可以大概作为我们的学习路径：[怎样从零开始学习安卓软件开发？ - 知乎](https://www.zhihu.com/question/19741608)
2. 我想，如果可以的话，我们之后用 Git 来管理项目。所以，大家先对 Git 有个大概的认识（如果没兴趣的话暂时不用深入学习）：[漫话：如何给女朋友解释什么是Git和GitHub？](https://mp.weixin.qq.com/s?__biz=Mzg3MjA4MTExMw==&mid=2247485189&idx=1&sn=fbe5c12bb3ebbb61741c6f91082d3557&chksm=cef5f4b3f9827da5423175abe0e114696605d0fe832ddcb9b3fc3e5e84b85b23f4115ac331c1&scene=90&xtrack=1&sessionid=1554110118&subscene=93&clicktime=1554110601&ascene=56&devicetype=iOS12.1.4&version=1700032a&nettype=WIFI&abtest_cookie=BAABAAoACwASABMABQAjlx4AVpkeAMqZHgDZmR4A3JkeAAAA&lang=zh_CN&fontScale=100&pass_ticket=ZgSgi5nXU2danIg1smld4bT6wUi1AWJYYdU%2FVrAsGwMvWg7MW%2BjMmyXb4YDnwb9R&wx_header=1)
3. 2. 推荐大家学习 「命令行快速入门」，我每天使用计算机的很大一部分时间是在使用命令行，熟练使用命令行可以让操作电脑更容易，所以，如果大家有兴趣，可以看一下这篇文章：[命令行快速入门](https://github.com/cdfmlr/LearnAndroidDevelopment/blob/master/Materials/《命令行快速入门》.pdf)

## 补充说明
1. 在 “【参考】” 中我给出的是各项技术的「菜鸟教程」页，这个网站上对知识的总结挺好的，可以当作学习纲要来参考（我们要学的包括但不限于其中内容）
2. 「参考阅读」中的东西都仅只是推荐。
3. 所有内容大家都可以随意选学😂

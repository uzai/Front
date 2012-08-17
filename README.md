UZ Css规范
Css全局规范
1. 在样式表开头添加一个注释块，用以描述这个样式表的 编码格式 最后的修改时间 标记等备注信息
/*
  *	charset：UTF-8 
*  Time:2012-05-05  
* Copyright (c) 2012 www.uzai.com All rights reserved.
 */
2. 文件名规范
@1.base.css 为css样式重置和一些公用的css
@2.layout.css 为网站上所有公用的js组件、公用模块都写在这个css样式表中
@3.index.css  为首页的样式表
@4.page.css  为一些产品页 线路页的css样式表
说明：初期建立的时候按照这个来建立，等后期网站基本上完成可以考虑对base.css layout.css等进行合并为一个css global.css文件。在开发当中也可以为一些特殊的页面单独建立css文件。
Global.css文件说明：
在样式表的头部，对公用css属性默认值清零操作：
/*----start resrt----*/
代码。。。。。。。。
/*----end reset----*/
在样式表的头部对body的背景 、文本、字体、行高、全局链接等进行设置
/*----start base----*/
   代码。。。。。。
/*----end base----*/
在样式表中间书写网站公用模块样式
在样式表中间书写网站公用模块样式
/*----start layout----*/
	代码。。。。。
/*----end  layout----*/
在样式表底部书写网站公用JS组件样式
/*----start js----*/
   代码。。。。。
/*----end  js----*/
说明：css代码模块化对后期的维护和添加新的css都非常有帮助。在新增加css的时候一定要找到当前模块进行添加，拒绝代码乱添加给之后的维护带来很大的困扰。
3．Css注释
大模块我们可以采用这种注释方法：
/*----start main----*/
/*----end main----*/
大模块里面的模块可以采用这种注释：
/*--start left--*/
/*--start left--*/
最小级的模块注释：
/*start submenu*/
/*end submenu*/
针对后期的维护修改等可以采用这种注释：
/*name 2012-05-05*/
说明：注释最好采用英文，尽量避免中文注释，采用这种递减的方式写注释使得我们的css一目了然，结构清晰，看到css注释基本上能想起html的结构。最多使用3级注释，注释以模块为一单位书写。最后一种注释为修改者名字和修改日期，可能考虑到程序员添加的css和后期维护新加的css
Css引用
css都采用外链引用方式：<link href=”” type=”text/css” rel=”stylesheet” />
或者写在头部<style type=”text/css”>代码。。。。。</css>（针对一些会刊 专辑）
特别注意：坚决避免使用内嵌式方式写css :<div style=”height:20px”>可维护性差。



Css命名规范
1、	考虑到团队合作，因此CSS命名必须规范，避免开发中造成命名冲突等。
2、	Css命名语义化；如：
常用名称：
名称	定义	名称	定义	名称	定义	名称	定义
头：	header	尾：	footer	Logo：	logo	版权：	copyright
内容块：	content(A)	栏目块：	column	结构左：	left	结构中：	center
结构右：	right	矩阵导航：	matrixNav	首页导航：	indexNav	频道二级：	channelNav
导航文字：	navText	内容导航：	nav	内容主导航：	mainNav	子内容导航：	subNav
边导航：	sidebar	左导航：	leftsidebar	右导航：	rightsidebar	广告：	ad
搜索：	search	关键字：	keyWord	标签：	tag	菜单：	menu
滚动：	scroll	列表：	list	下拉：	drop	按钮：	btn
登陆：	login	登录条：	loginbar	注册：	reg	提示信息：	msg
打印：	print	地图：	map	功能区：	shop	Flash：	flash
标题：	title	更多：	more	博客：	blog	视频：	video
媒体：	media	新闻：	news	热点：	hot	评论：	review
合作：	cooperate	联系：	contact	加入我们：	joinUs	合作伙伴：	partner
友情链接：	link	论坛社区：	club	投票：	vote	摘要：	summary
服务：	service	指南：	guild	描述：	description	信息：	info
状态：	status	注释：	note	下载：	download	价格：	price
地址：	address	产品：	products	跳转：	jump	条：	bar
线：	line	小技巧：	Tips	外套：	wrap		
这基本上是每个网站常用的模块化命名。
针对我们网站的命名：
&1.网站通用模块组件使用：
   使用fn-开头来命名,例如：翻页模块命名：class=”fn-page”	
菜单模块命名：class=”fn-menu”	
&2.针对网站头部，尾部，内容部分这样框架化的层可以采用ID命名方式  例如：
 id=”header”    id=”footer”       id=”content”

&3.针对为JS预留的接口，JS组件使用如下方式：
Id=”js-show”  class=”js-hide”等方式
&4.(共同)针对模块 我们采用如下方式：模块+功能的命名方式 如：
Class=”page” class=”page-tips”  class=”page-list-news”或者class=”pageTips”驼峰式命名
&5.对我们常用的一些css采用如下命名：
p-clear  p-clearfix p-font12的方式命名
&6. 避免 css hack ， 考虑使用特定浏览器前缀表示：
.ks-ie6 p {margin: 1em 0;}
以上是大体结构上的命名方式，在一些命名的细节中我们还应该注意一些问题：
 *1.id和class使用，ID为唯一的，因此我们在大的结构上才采用ID，一般就是使用class来命名，也易于通用。
*2.我们为class命名的时候还应该注意语义化，简明化。尽量使用一些英文单词的组合(类别+功能；属性+值等) 如：
font24     width990   header  footer  js-show  .ff60cc等命名，一看就很明了，知道是什么意思。避免使用英文拼音命名。

总结：这样的css命名规范，为我们了解网站和后期维护 新同事的加入学习提供了很大的便利。如通用模块命名 fn-XXX 看到这个就知道这个是整个网站通用的css 放在global里面的  js-XX一看到这个就知道这是为JS预留的。这样就对整个网站有个很清晰的了解，通过css命名等细节问题，使开发者更有利的了解网站，维护等。较现在比较混乱无序的命名来说，在各方面都提高了不少。






Css代码书写规范
1.	css的缩写规则
a)：不同类有相同属性及属性值的书写；
如.a,.b,#c,.d{height:20px;width:20px;border:1px solid #ccc;}
b)：同一属性的缩写；
如：.font{border:1px solid #ccc;margin:0 4px;background:#fff url(imae/i.jpg);}等等。
2．选择器的使用：
 a)：避免使用ID来写全局样式 如 #main a{color:#666;} （不可取）
	因为ID的优先级高于class这样定全局样式，使得里面的样式没办法重置。
b):最后一级才可以使用标签来作为选择器；
如:.header p a{color:#fff;}(不可取) 应该.header .news a{color:#fff;}
c):尽量使用标签作为选择器 减少id class(但是遵循第2条):
如：.menu ul{}等
d):必须遵循下列书写格式：
div{font-size:14px;border:1px solid #ccc;}
杜绝：
Div{
font-size:14px;
border:1px solid #ccc;
} 
上面一种节省空间，易于压缩；结束加分号
E) 书写代码前, 考虑并提高样式重复使用率
F) 杜绝使用<meta http-equiv="X-UA-Compatible" content="IE=7" /> 兼容 ie8;


g):在css中避免使用滤镜_filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(sizingMethod=crop, src=’img/bg.png影响css执行速度
避免使用css表达式：
top:expression(documentElement.scrollTop + documentElement.clientHeight-this.offsetHeight); 影响css执行速度
f）使用css sprite来优化页面,减少http请求数，加快网站加载。
3.css hack的编写
在平时的开发中，我们经常遇到一些浏览器直接的差异问题，可能针对这类问题需要针对某类浏览器写兼容样式；
A):ie6 7 8 firefox的兼容写法
Ie都能认识 \0 
Ie 8不认识 \9
Ie 67认识*
Ie6认识_
Css hack尽量避免使用，不符合w3c标准的。
Css的优先级问题：
		！important（尽量少使用）>Id >class > 标签选择器
书写css的时候特别注意优先级问题，css按照此规则来重置。








                                                                                                     uzai前端开发小组                  2012/08/15

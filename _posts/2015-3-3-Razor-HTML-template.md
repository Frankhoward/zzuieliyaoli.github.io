---
layout: post
title:  "模板引擎 Razor 体验"
date:   2015-3-3
categories: [模板]
---


前一阶段在做外包项目的时候，累感不爱啊。

先说一下基本情况。

开发人员：我和团队里一位擅长C#、.NET语言的学长。

开发的大致流程：

1. 前端把每个页面的效果，用静态HTML将网站的效果完全呈现出来；

2. 后端用AJAX实现文章发布等动态功能。

**所以累感不爱的原因是如下问题：**

1. 静态HTML一旦发生更改，网站全部页面的代码都得一个一个手动修改，比如导航条、页面结构等。5-6个页面还好说，20+的页面实在是吃不消。
	
	比如，![My helpful screenshot](/images/posts/2015030301.png)

2. 由于春节假期的原因，无法面基、沟通不畅。在代码迭代的过程中，后端呈现效果无法与前端更新的效果保持一致。

**这样开发实在是受不了了。**

结合玩过PHP、Node的经历，问题1明显可以使用**模板引擎**解决，问题2除了GitHub一个解决办法以外，应该有其他适合中小型项目的方法，不过那就是下一篇文章啦。

首先要解决问题1。那么挑选哪一种模板引擎呢？需要既得结合后端的开发语言，也得方便后端调试效果。最后**Razor**进入视线。略去安装Visual Studio 2013的艰辛过程不说，以下是作为一个前端开发人员的使用体验。

1. 创建项目完毕后，一键本地预览sample，想要哪种浏览器自己选。 

	![My helpful screenshot](/images/posts/2015030302.png) 

	![My helpful screenshot](/images/posts/2015030303.png)

	![My helpful screenshot](/images/posts/2015030305.png)

2. sample的代码，作为前端只需要关注Images、Scripts、Content文件夹，以及根目录上的几个文件就妥。	![My helpful screenshot](/images/posts/2015030306.png)

3. 定义模板: _SiteLayout.cshtml

4. 引用模板：![My helpful screenshot](/images/posts/2015030307.png)

5. 还可以生成项目模板。

需要注意的知识点：**RenderBody()方法**（[http://www.codeproject.com/Articles/383145/RenderBody-RenderPage-and-RenderSection-methods-in](http://www.codeproject.com/Articles/383145/RenderBody-RenderPage-and-RenderSection-methods-in)）

以上。


####参考资料：
> [http://www.asp.net/web-pages/overview/getting-started/introducing-razor-syntax-(c)](http://www.asp.net/web-pages/overview/getting-started/introducing-razor-syntax-(c) "官方教程")
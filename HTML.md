# HTML #

## HTML语义化 ##

### 1. 什么是HTML语义化？ ###

　　根据内容的结构化（内容语义化），选择合适的标签（代码语义化）便于开发者阅读和写出更优雅的代码的同时让浏览器的爬虫和机器很好地解析。

### 2. 为什么要语义化？ ###

 - 为了在没有CSS的情况下，页面也能呈现出很好地内容结构、代码结构:为了裸奔时好看；

 - 用户体验：例如title、alt用于解释名词或解释图片信息、label标签的活用；

 - 有利于SEO：和搜索引擎建立良好沟通，有助于爬虫抓取更多的有效信息：爬虫依赖于标签来确定上下文和各个关键字的权重；

 - 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以意义的方式来渲染网页；

 - 便于团队开发和维护，语义化更具可读性，是下一步吧网页的重要动向，遵循W3C标准的团队都遵循这个标准，可以减少差异化。

### 3. 写HTML代码时应注意什么？ ###

 - 尽可能少的使用无语义的标签div和span；

 - 在语义不明显时，既可以使用div或者p时，尽量用p, 因为p在默认情况下有上下间距，对兼容特殊终端有利；

 - 不要使用纯样式标签，如：b、font、u等，改用css设置。

 - 需要强调的文本，可以包含在strong或者em标签中（浏览器预设样式，能用CSS指定就不用他们），strong默认样式是加粗（不要用b），em是斜体（不用i）；

 - 使用表格时，标题要用caption，表头用thead，主体部分用tbody包围，尾部用tfoot包围。表头和一般单元格要区分开，表头用th，单元格用td；

 - 表单域要用fieldset标签包起来，并用legend标签说明表单的用途；

 - 每个input标签对应的说明文本都需要使用label标签，并且通过为input设置id属性，在lable标签中设置for=someld来让说明文本和相对应的input关联起来。

## HTML和CSS的关系 ##

1. HTML是网页内容的载体。内容就是网页制作者放在页面上想要让用户浏览的信息，可以包含文字、图片、视频等。

2. CSS样式是表现。就像网页的外衣。比如，标题字体、颜色变化，或为标题加入背景图片、边框等。所有这些用来改变内容外观的东西称之为表现。

3. JavaScript是用来实现网页上的特效效果。如：鼠标滑过弹出下拉菜单。或鼠标滑过表格的背景颜色改变。还有焦点新闻（新闻图片）的轮换。可以这么理解，有动画的，有交互的一般都是用JavaScript来实现的。

## <!DOCTYPE> ##

- <!DOCTYPE> 声明必须是 HTML 文档的第一行，位于 <html> 标签之前。

- <!DOCTYPE> 声明不是 HTML 标签；它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。

- 在 HTML 4.01 中，<!DOCTYPE> 声明引用 DTD，因为 HTML 4.01 基于 SGML。DTD 规定了标记语言的规则，这样浏览器才能正确地呈现内容。

- HTML5 不基于 SGML，所以不需要引用 DTD。

**提示**：请始终向 HTML 文档添加 <!DOCTYPE> 声明，这样浏览器才能获知文档类型。

HTML:

> 过渡型：

>
	<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

> 严格型:

> 
	<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

> 框架型:

> 
	<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">

XML:

> 过渡型:

>  
	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" " http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

> 严格型:

> 
	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

> 框架型:

> 	
	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">

HTML5:

	<!DOCTYPE html>

## HTML5、HTML4.01、XHTML ##

### 什么是 HTML？ ###

HTML 是用来描述网页的一种语言。

 - HTML 指的是超文本标记语言 (Hyper Text Markup Language)

 - HTML 不是一种编程语言，而是一种标记语言 (markup language)

 - 标记语言是一套标记标签 (markup tag)

 - HTML 使用标记标签来描述网页

### 什么是 XHTML？ ###

 - XHTML 指的是可扩展超文本标记语言

 - XHTML 与 HTML 4.01 几乎是相同的

 - XHTML 是更严格更纯净的 HTML 版本

 - XHTML 是以 XML 应用的方式定义的 HTML

 - XHTML 是 2001 年 1 月发布的 W3C 推荐标准

 - XHTML 得到所有主流浏览器的支持

XHTML 是作为 XML 被重新设计的 HTML。

#### XHTML 与 HTML 相比最重要的区别 ####

**文档结构**

 - XHTML DOCTYPE 是强制性的

 - `<html>` 中的 XML namespace 属性是强制性的

 - `<html>`、`<head>`、`<title>` 以及 `<body>` 也是强制性的

**元素语法**

 - XHTML 元素必须正确嵌套

 - XHTML 元素必须始终关闭

 - XHTML 元素必须小写

 - XHTML 文档必须有一个根元素

**属性语法**

 - XHTML 属性必须使用小写

 - XHTML 属性值必须用引号包围

 - XHTML 属性最小化也是禁止的

**<!DOCTYPE ....> 是强制性的**

XHTML 文档必须进行 XHTML 文档类型声明（XHTML DOCTYPE declaration）。

`<html>`、`<head>`、`<title>` 以及 `<body>` 元素也必须存在，并且必须使用 `<html>` 中的 xmlns 属性为文档规定 xml 命名空间。

#### 如何从 HTML 转换到 XHTML ####

1. 向每张页面的第一行添加 XHTML <!DOCTYPE>

2. 向每张页面的 html 元素添加 xmlns 属性

3. 把所有元素名改为小写

4. 关闭所有空元素

5. 把所有属性名改为小写

6. 为所有属性值加引号

### 什么是 HTML5？ ###

HTML5 是下一代的 HTML。

 - HTML5 将成为 HTML、XHTML 以及 HTML DOM 的新标准。

 - HTML 的上一个版本诞生于 1999 年。自从那以后，Web 世界已经经历了巨变。

 - HTML5 仍处于完善之中。然而，大部分现代浏览器已经具备了某些 HTML5 支持。

#### HTML5 是如何起步的？ ####

HTML5 是 W3C 与 WHATWG 合作的结果。

**编者注**：W3C 指 World Wide Web Consortium，万维网联盟。

**编者注**：WHATWG 指 Web Hypertext Application Technology Working Group。

WHATWG 致力于 web 表单和应用程序，而 W3C 专注于 XHTML 2.0。在 2006 年，双方决定进行合作，来创建一个新版本的 HTML。

为 HTML5 建立的一些规则：

 - 新特性应该基于 HTML、CSS、DOM 以及 JavaScript。

 - 减少对外部插件的需求（比如 Flash）

 - 更优秀的错误处理

 - 更多取代脚本的标记

 - HTML5 应该独立于设备

 - 开发进程应对公众透明

#### HTML5 中的新内容？ ####

HTML5 的新的文档类型（DOCTYPE）声明非常简单：

	<!DOCTYPE html>
	The new character encoding (charset) declaration is also very simple:

	<meta charset="UTF-8">

HTML5 实例：

	<!DOCTYPE html>
	<html>
	<head>
	<meta charset="UTF-8">
	<title>Title of the document</title>
	</head>

	<body>
	Content of the document......
	</body>

	</html>

**注释**：HTML5 中默认的字符编码是 UTF-8。

#### HTML5 - 新的属性语法 ####

HTML5 标准允许 4 中不同的属性语法。

本例演示在 `<input>` 标签中使用的不同语法：

类型 | 示例 
- | - 
Empty | `<input type="text" value="John Doe" disabled>`
Unquoted | `<input type="text" value=John Doe>`
Double-quoted |`<input type="text" value="John Doe">`
Single-quoted | `<input type="text" value='John Doe'>`

在 HTML5 标准中，根据对属性的需求，可能会用到所有 4 种语法。

#### HTML5 - 新特性 ####

HTML5 的一些最有趣的新特性：

 - 新的语义元素，比如 `<header>`, `<footer>`, `<article>`, 和 `<section>`。

 - 新的表单控件，calendar、date、time、email、url、search

 - 强大的图像支持（借由 `<canvas>` 和 `<svg>`）

 - 强大的多媒体支持（借由 `<video>` 和 `<audio>`）

 - 强大的新 API，比如用本地存储取代 cookie。

#### HTML5 - 被删元素 ####

以下 HTML 4.01 元素已从 HTML5 中删除：

 - `<acronym>`
 - `<applet>`
 - `<basefont>` 
 - `<big>`
 - `<center>`
 - `<dir>`
 - `<font>`
 - `<frame>`
 - `<frameset>`
 - `<noframes>`
 - `<strike>`
 - `<tt>`

## HTML标签 ##

### 标签的语法 ###

1. 标签由英文尖括号<和>括起来，如<html>就是一个标签。

2. html中的标签一般都是成对出现的，分开始标签和结束标签。结束标签比开始标签多了一个/。

3. 标签与标签之间是可以嵌套的，但先后顺序必须保持一致，如：`<div>`里嵌套`<p>`，那么`</p>`必须放在`</div>`的前面。

4. HTML标签不区分大小写，`<h1>`和`<H1>`是一样的，但建议小写，因为大部分程序员都以小写为准。

标题标签:

	<h1></h1>

> 标题标签一共有6个，h1、h2、h3、h4、h5、h6分别为一级标题、二级标题、三级标题、四级标题、五级标题、六级标题。并且依据重要性递减。`<h1>`是最高的等级。

> 因为h1标签在网页中比较重要，所以一般h1标签被用在网站名称上。腾讯网站就是这样做的。如：`<h1>`腾讯网`</h1>`

段落标签：

	<p></p>

图片标签：

	<img></img>

head标签：

	<head></head>

> 文档的头部描述了文档的各种属性和信息，包括文档的标题等。绝大多数文档头部包含的数据都不会真正作为内容显示给读者。

> 下面这些标签可用在 head 部分：

>     
    <head>
    	<title>...</title>
    	<meta>
    	<link>
    	<style>...</style>
    	<script>...</script>
	</head>

`<title>`标签：在`<title>`和`</title>`标签之间的文字内容是网页的标题信息，它会出现在浏览器的标题栏中。网页的title标签用于告诉用户和搜索引擎这个网页的主要内容是什么，搜索引擎可以通过网页标题，迅速的判断出网页的主题。每个网页的内容都是不同的，每个网页都应该有一个独一无二的title。

代码注释：

	<!--注释文字 -->

> 代码注释的作用是帮助程序员标注代码的用途，过一段时间后再看你所编写的代码，就能很快想起这段代码的用途。代码注释不仅方便程序员自己回忆起以前代码的用途，还可以帮助其他程序员很快的读懂你的程序的功能，方便多人合作开发网页代码。

强调标签：

	<em></em>

----------

	<strong></strong>

> `<em>`表示强调，默认用斜体表示；`<strong>`表示更强烈的强调，默认用粗体表示。

`<span>`标签：

	<span></span>

> 设置单独的样式，没有语义。

引用标签：

- `<q>`标签，短文本引用：

		<q>短文本</q>

- `<blockquote>`标签，长文本引用：

		<blockquote>长文本<blockquote>

 `<q>`和`<blockquote>`标签会自动给文本添加双引号，语义是引用别人的话。

分行标签：

	<br />

空格标签：

	&nbsp;

`<hr />`标签

	<hr />

> 添加水平横线。

地址标签：

	<address>地址</address>

> 添加地址信息，默认为斜体表示。

代码标签：

 - 单行

        <code>代码</code>

 - 多行

	    <pre>代码</pre>

无序列表:

	<ul>
		<li>信息</li>
		<li>信息</li>
		......
	</ul>

有序列表：

	<ol>
		<li>信息</li>
		<li>信息</li>
		......
	</ol>

`<div>`标签：

	<div>内容</div>

> 容器，用来划分出独立的逻辑部分。

表格标签：

	<table summry="摘要">
		<caption>标题</caption>
		<tr>
			<th>内容</th>
			<th>内容</th>
			<th>内容</th>
			<th>内容</th>
		</tr>
		<tr>
			<td>内容</td>
			<td>内容</td>
			<td>内容</td>
			<td>内容</td>
		</tr>
		<tr>
			<td>内容</td>
			<td>内容</td>
			<td>内容</td>
			<td>内容</td>
		</tr>
	</table>

> 创建表格的四个元素：`<table>`、`<tbody>`、`<tr>`、`<th>`、`<td>`

> 1. `<table>…</table>`：整个表格以`<table>`标记开始、`</table>`标记结束。

> 2. `<tbody>…</tbody>`：如果不加`<thead>`、`<tbody>`、`<tfooter>`，表格加载完后才显示。加上这些表格结构，tbody包含行的内容下载完优先显示，不必等待表格结束后在显示，同时如果表格很长，用tbody分段，可以一部分一部分地显示。（通俗理解table可以按结构一块块的显示，不在等整个表格加载完后显示。）

> 3. `<tr>…</tr>`：表格的一行，所以有几对`<tr>…</tr>`表格就有几行。

> 4. `<td>…</td>`：表格的一个单元格，一行中包含几对`<td>...</td>`，说明一行中就有几列。

> 5. `<th>…</th>`：表格的头部的一个单元格，表格表头。

> 6. 表格中列的个数，取决于一行中数据单元格的个数。

> **摘要**

> 摘要的内容是不会在浏览器中显示出来的。它的作用是增加表格的可读性(语义化)，使搜索引擎更好的读懂表格内容，还可以使屏幕阅读器更好的帮助特殊用户读取表格内容。

> **标题**

> 用以描述表格内容，标题的显示位置：表格上方。

## html文件基本结构 ##

HTML文件是有自己固定的结构的。

	<html>
    	<head>...</head>
		<body>...</body>
	</html>

代码讲解：

1. `<html></html>`称为根标签，所有的网页标签都在`<html></html>`中。

2. `<head>`标签用于定义文档的头部，它是所有头部元素的容器。头部元素有`<title>`、`<script>`、`<style>`、`<link>`、`<meta>`等标签，头部标签在下一小节中会有详细介绍。

3. 在`<body>`和`</body>`标签之间的内容是网页的主要内容，如`<h1>`、`<p>`、`<a>`、`<img>`等网页内容标签，在这里的标签中的内容会在浏览器中显示出来。

### 块级元素和内联元素 ###

在HTML中有两种你需要知道的重要元素类别，块级元素和内联元素。

 - 块级元素在页面中以块的形式展现 —— 相对与其前面的内容它会出现在新的一行，其后的内容也会被挤到下一行展现。块级元素通常用于展示页面上结构化的内容，例如段落、列表、导航菜单、页脚等等。一个以block形式展现的块级元素不会被嵌套进内联元素中，但可以嵌套在其它块级元素中。

 - 内联元素通常出现在块级元素中并包裹文档内容的一小部分，而不是一整个段落或者一组内容。内联元素不会导致文本换行：它通常出现在一堆文字之间例如超链接元素`<a>`或者强调元素`<em>`和 `<strong>`。
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

	<img src="图片地址" alt="下载失败时的替换文本" title="提示文本" />

> 讲解：

> 1. src：标识图像的位置；

> 2. alt：指定图像的描述性文本，当图像不可见时（下载不成功时），可看到该属性指定的文本；

> 3. title：提供在图像可见时对图像的描述(鼠标滑过图片时显示的文本)；

> 4. 图像可以是GIF，PNG，JPEG格式的图像文件。

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

超链接标签：

	<a href="网址" title="鼠标滑过现实的文本">链接显示的文本</a>

> title属性会让鼠标滑过链接文字时会显示这个属性的文本内容。这个属性在实际网页开发中作用很大，主要方便搜索引擎了解链接地址的内容（语义化更友好）。

> `<a>`标签在默认情况下，链接的网页是在当前浏览器窗口中打开，有时需要在新的标签页中打开。

> 代码实现如下：

>     
     <a href="目标网址" target="_blank">链接现实的文本</a>

> `<a>`标签还可以链接E-mail地址，使用mailto能让访问者便捷向网站管理者发送电子邮件。

> 代码实现如下：

> 
    <a href="mailto:example1@emali.com;example2@emali.com?cc=example3@emali.com&bcc=example4@emali.com&subject=主题&body=内容">邮件显示文本</a>

> **注意：**如果mailto后面同时有多个参数的话，第一个参数必须以“?”开头，后面的参数每一个都以“&”分隔，cc代表抄送，bcc表示密件抄送，subject为邮件主题，body为邮件内容，发送邮件可选多个地址，每个地址之间用`;`隔开。

表单标签：

	<form method="传送方式" action="服务器文件"></form>

> 表单可以把浏览者输入的数据传送到服务器端，这样服务器端程序就可以处理表单传过来的数据。

> 讲解：

> 1. `<form>`:`<form>`标签是成对出现的，以`<form>`开始，以`</form>`结束。

> 2. action：浏览者输入的数据被传送到的地方,比如一个PHP页面(save.php)。

> 3. method：数据传送的方式（get/post）。

> 示例：

> 
	<form    method="post"    action="save.php">
		<label for="username">用户名:</label>
        <input type="text" name="username" />
        <label for="pass">密码:</label>
        <input type="password" name="pass" />
	</form>

> **注意:**

> **1. 所有表单控件（文本框、文本域、按钮、单选框、复选框等）都必须放在 `<form>``</form>` 标签之间（否则用户输入的信息可提交不到服务器上哦！）。**

> **2. method : post/get 的区别这一部分内容属于后端程序员考虑的问题。**

文本、密码输入框：

	<form>
		<input type="text/password" name="名称" value="文本" />
	</form>

> 文本输入框可以让用户在表单键入字母、数字等内容，文本输入框也可以转化为密码输入框。

> 1. type：

> > 当type="text"时，输入框为文本输入框;

> > 当type="password"时, 输入框为密码输入框。

> 2. name：为文本框命名，以备后台程序ASP 、PHP使用。

> 3. value：为文本输入框设置默认值。(一般起到提示作用)

> 示例：

> 
	<form>
  	姓名：
  	<input type="text" name="myName" />
  	<br />
  	密码：
  	<input type="password" name="pass" />
	</form>

文本域：

	<textarea rows="行数" cols="列数">文本</textarea>

> 1. `<textarea>`标签是成对出现的，以`<textarea>`开始，以`</textarea>`结束。

> 2. **cols**:多行输入域的**列数**。

> 3. **rows**：多行输入域的**行数**。

> 4. 在`<textarea>``</textarea>`标签之间可以输入**默认值**。

> 举例：

> 
	<form method="post" action="save.php">
		<label>联系我们</label>
		<textarea cols="50" rows:"10">在这里输入内容...</textarea>
	</form>

单选框、复选框：
	
	<input type="radio/checkbox" value="值" name="名称" checked="checked" />

> 1. type:

> > 当 type="radio" 时，控件为单选框。

> > 当 type="checkbox" 时，控件为复选框。

> 2. value：提交数据到服务器的值(后台程序PHP使用）。

> 3. name：为控件命名，以备后台程序 ASP、PHP使用。

> 4. checked：当设置 checked="checked" 时，该选项被默认选中。

> **注意:**同一组的单选按钮，name取值一定要一致，比如上面例子为同一个名称“radioLove”，这样同一组的单选按钮才可以起到单选的作用。

下拉列表：

	<select>
		<option value="提交值">选项</option>
		<option value="提交值">选项</option>
		<option value="提交值">选项</option>
	</select>

> 1. **value**：提交值指向服务器提交的值；选项指显示的值。

> 2. **selected="selected"**:设置**selected="selected"**属性，则该选项就被默认选中。

>在`<select>`标签中设置multiple="multiple"属性，可以实现多选功能，在 windows 操作系统下，进行多选时按下Ctrl键同时进行单击（在 Mac下使用 Command +单击），可以选择多个选项。代码如下：

>
	<select multiple="multiple">
		<option value="提交值">选项</option>
		<option value="提交值">选项</option>
		<option value="提交值">选项</option>
	</select>

提交按钮：

	<input type="submit" value="提交">

> type:**只有当type值设置为submit时，按钮才有提交作用。**

> value: 按钮上显示的文字。

重置按钮:

	<input type="reset" value="重置">

> type:**只有当type值设置为reset时，按钮才有重置作用。**

> value:按钮上显示的文字。

label标签：

	<label for="控件id名称">

> 作用：label标签不会向用户呈现任何特殊效果，它的作用是为鼠标用户改进了可用性。如果你在 label 标签内点击文本，就会触发此控件。就是说，当用户单击选中该label标签时，浏览器就会自动将焦点转到和标签相关的表单控件上（就自动选中和该label标签相关连的表单控件上）。

> **注意**：标签的 for 属性中的值应当与相关控件的 id 属性值一定要相同。

> 举例：

> 
	<form>
		<label for="male">男</label>
		<input type="ratio" name="gender" id="male" />
		<br />
		<label for="female">女</label>
		<input type="ration" name="gender" id="female" />
		<label for="email">输入你的邮箱地址</label>
		<input type="email" id="email" placeholder="Enter eamil">
	</form>

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
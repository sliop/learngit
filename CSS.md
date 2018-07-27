# CSS #

CSS全称为“层叠样式表 (Cascading Style Sheets)”，它主要是用于定义HTML内容在浏览器内的显示样式，如文字大小、颜色、字体加粗等。

使用CSS样式的一个好处是通过定义某个样式，可以让不同网页位置的文字有着统一的字体、字号或者颜色等。

## 发展历程 ##

1990年，Tim Berners-Lee和Robert Cailliau共同发明了Web。1994年，Web真正走出实验室。

从HTML被发明开始，样式就以各种形式存在。不同的浏览器结合它们各自的样式语言为用户提供页面效果的控制。最初的HTML只包含很少的显示属性。

随着HTML的成长，为了满足页面设计者的要求，HTML添加了很多显示功能。但是随着这些功能的增加，HTML变的越来越杂乱，而且HTML页面也越来越臃肿。于是CSS便诞生了。

1994年哈坤·利提出了CSS的最初建议。而当时伯特·波斯（Bert Bos）正在设计一个名为Argo的浏览器，于是他们决定一起设计CSS。

其实当时在互联网界已经有过一些统一样式表语言的建议了，但CSS是第一个含有“层叠”丰意的样式表语言。在CSS中，一个文件的样式可以从其他的样式表中继承。读者在有些地方可以使用他自己更喜欢的样式，在其他地方则继承或“层叠”作者的样式。这种层叠的方式使作者和读者都可以灵活地加入自己的设计，混合每个人的爱好。

哈坤于1994年在芝加哥的一次会议上第一次提出了CSS的建议，1995年的www网络会议上CSS又一次被提出，博斯演示了Argo浏览器支持CSS的例子，哈肯也展示了支持CSS的Arena浏览器。

同年，W3C组织（World WideWeb Consortium）成立，CSS的创作成员全部成为了W3C的工作小组并且全力以赴负责研发CSS标准，层叠样式表的开发终于走上正轨。有越来越多的成员参与其中，例如微软公司的托马斯·莱尔顿(Thomas Reaxdon)，他的努力最终令Internet Explorer浏览器支持CSS标准。哈坤、波斯和其他一些人是这个项目的主要技术负责人。1996年底，CSS初稿已经完成，同年12月，层叠样式表的第一份正式标准（Cascading style Sheets Level 1）完成，成为w3c的推荐标准。

1997年初，W3C组织负责CSS的工作组开始讨论第一版中没有涉及到的问题。其讨论结果组成了1998年5月出版的CSS规范第二版。

## CSS3 ##

CSS3是CSS（层叠样式表）技术的升级版本，于1999年开始制订，2001年5月23日W3C完成了CSS3的工作草案，主要包括盒子模型、列表模块、超链接方式、语言模块、背景和边框、文字特效、多栏布局等模块。

CSS演进的一个主要变化就是W3C决定将CSS3分成一系列模块。浏览器厂商按CSS节奏快速创新，因此通过采用模块方法，CSS3规范里的元素能以不同速度向前发展，因为不同的浏览器厂商只支持给定特性。但不同浏览器在不同时问支持不同特性，这也让跨浏览器开发变得复杂。

优势：

1、减少开发成本与维护成本

在CSS3出现之前，开发人员为了实现一个圆角效果，往往需要添加额外的HTML标签，使用一个或多个图片来完成，而使用CSS3只需要一个标签，利用CSS3中的border-radius属性就能完成。这样，CSS3技术能把人员从绘图、切图和优化图片的工作中解放出来。如果后续需要调整这个圆角的弧度或者圆角的颜色，使用CSS2.1，需要从头绘图、切图才能实现，使用CSS3只需修改border-radius属性值就可快速完成修改。
CSS3提供的动画特性，可让开发者在先实现一些动态按钮或者动态导航时远离JavaScript，让开发人员不需要花费大量的时间去写脚本或者寻找合适的脚本插件来适配一些动态网站效果。

2、提高页面性能

很多CSS3技术通过提供相同的视觉效果而成为图片的“替代品”，换句话说，在进行Web开发时，减少多余的标签嵌套以及图片的使用数量，意味着用户要下载的内容将会更少，页面加载也会更快。另外，更少的图片、脚本和Flash文件能够减少用户访问Web站点时的HTTP请求数，这是提升页面加载速度的最佳方法之一。而使用CSS3制作图形化网站无需任何图片，极大地减少了HTTP的请求数量，并且提升了页面的加载速度。例如CSS3的动画效果，能够减少对JavaScript和Flash文件的HTTP请求，但可能会要求浏览器执行很多的工作来完成这个动画效果的渲染，这有可能导致浏览器响应缓慢致使用户流失。因此，在使用一些复杂的特效时需要考虑清楚。其实很多CSS3技术能够在任何情况下都大幅提高页面的性能。

CSS3将完全向后兼容，所以没有必要修改的设计来让它们继续运作。网络浏览器也还将继续支持CSS2。

## CSS代码语法 ##

css 样式由选择符和声明组成，而声明又由属性和值组成，如下图所示：

![](https://i.imgur.com/ymMtMci.png)

选择符：又称选择器，指明网页中要应用样式规则的元素，如本例中是网页中所有的段（p）的文字将变成蓝色，而其他的元素（如ol）不会受到影响。

声明：在英文大括号“｛｝”中的的就是声明，属性和值之间用英文冒号“：”分隔。当有多条声明时，中间可以英文分号“;”分隔，如下所示：

	p{font-size:12px;color:red;}

注意：

1、最后一条声明可以没有分号，但是为了以后修改方便，一般也加上分号。

2、为了使用样式更加容易阅读，可以将每条代码写在一个新行内，如下所示：

	p{
		font-size:12px;
		color:red;
	}

## CSS注释代码 ##

就像在Html的注释一样，在CSS中也有注释语句：用/*注释语句*/来标明（Html中使用<!--注释语句-->)。就像下面代码：

![](https://i.imgur.com/H9vFT0z.png)

## CSS样式 ##

从CSS 样式代码插入的形式来看，CSS 样式基本可以分为以下3种：内联式、嵌入式和外部式三种。

### 内联式CSS样式 ###

内联式css样式表就是把css代码直接写在现有的HTML标签中，如下面代码：

	<p style="color:red">这里文字是红色。</p>

注意要写在元素的开始标签里，下面这种写法是错误的：

	<p>这里文字是红色。</p style="color:red">

并且css样式代码要写在style=""双引号中，如果有多条css样式代码设置可以写在一起，中间用分号隔开。如下代码：

	<p style="color:red;font-size:12px">这里文字是红色。</p>

### 嵌入式css样式 ###

嵌入式css样式，就是可以把css样式代码写在<style type="text/css"></style>标签之间。效果是改变整个文件内相应选择器的样式，如下面代码实现把三个<span>标签中的文字设置为红色：

	<style type="text/css">
	span{
	color:red;
	}
	</style>

嵌入式css样式必须写在<style></style>之间，并且一般情况下嵌入式css样式写在<head></head>之间。如右边编辑器中的代码。

### 外部式css样式 ###

外部式css样式(也可称为外联式)就是把css代码写一个单独的外部文件中，这个css样式文件以“.css”为扩展名，在<head>内（不是在<style>标签内）使用<link>标签将css样式文件链接到HTML文件内，如下面代码：

	<link href="base.css" rel="stylesheet" type="text/css" />

注意：

1. css样式文件名称以有意义的英文字母命名，如 main.css。

2. rel="stylesheet" type="text/css" 是固定写法不可修改。

3. <link>标签位置一般写在<head>标签之内。

### 样式优先级 ###

这三种样式是有优先级的，他们的优先级是：内联式 > 嵌入式 > 外部式

但是嵌入式>外部式有一个前提：嵌入式css样式的位置一定在外部式的后面。如右代码编辑器就是这样，<link href="style.css" ...>代码在<style type="text/css">...</style>代码的前面（实际开发中也是这么写的）。

其实总结来说，就是--就近原则（离被设置元素越近优先级别越高）。

但注意上面所总结的优先级是有一个前提：内联式、嵌入式、外部式样式表中css样式是在的相同权值的情况下。

## CSS选择器 ##

每一条css样式声明（定义）由两部分组成，形式如下：

	选择器{
    	样式;
	}
在{}之前的部分就是“选择器”，“选择器”指明了{}中的“样式”的作用对象，也就是“样式”作用于网页中的哪些元素。

### 标签选择器 ###

标签选择器其实就是html代码中的标签。如`<html>`、`<body>`、`<h1>`、`<p>`、`<img>`。例如下面代码：

	p{
		font-size:12px;
		line-height:1.6em;
	}

上面的css样式代码的作用：为p标签设置12px字号，行间距设置1.6em的样式。

### 类选择器 ###

类选择器在css样式编码中是最常用到的。

语法：

	.类选器名称{css样式代码;}

注意：

1. **英文圆点开头**

2. 其中**类选器名称**可以任意起名（但不要起中文噢）

使用方法：

第一步：使用合适的标签把要修饰的内容标记起来，如下：

	<span>胆小如鼠</span>

第二步：使用class="类选择器名称"为标签设置一个类，如下：

	<span class="stress">胆小如鼠</span>

第三步：设置类选器css样式，如下：

	.stress{color:red;}/*类前面要加入一个英文圆点*/

### ID选择器 ###

在很多方面，ID选择器都类似于类选择符，但也有一些重要的区别：

1. 为标签设置id="ID名称"，而不是class="类名称"。

2. ID选择符的前面是井号（**#**）号，而不是英文圆点（**.**）。

语法：

	#ID选择器名称{CSS样式代码;}

使用方法：

第一步：使用合适的标签把要修饰的内容标记起来，如下：

	<span>胆小如鼠</span>

第二步：使用id="ID选择器名称"为标签设置一个ID，如下：

	<span id="stress">胆小如鼠</span>

第三步：设置类选器css样式，如下：

	#stress{color:red;}/*类前面要加入一个井号*/

### 类选择器与ID选择器区别 ###

**相同点**：可以应用于任何元素

**不同点**：

1. **ID选择器只能在文档中使用一次**。与类选择器不同，在一个HTML文档中，ID选择器只能使用一次，而且仅一次。而类选择器可以使用多次。

> 下面代码是正确的：
> 
 	<p>三年级时，我还是一个<span class="stress">胆小如鼠</span>的小女孩，上课从来不敢回答老师提出的问题，生怕回答错了老师会批评我。就一直没有这个<span class="stress">勇气</span>来回答老师提出的问题。</p>

> 而下面代码是错误的：
> 
 	<p>三年级时，我还是一个<span id="stress">胆小如鼠</span>的小女孩，上课从来不敢回答老师提出的问题，生怕回答错了老师会批评我。就一直没有这个<span id="stress">勇气</span>来回答老师提出的问题。</p>

2. **可以使用类选择器词列表方法为一个元素同时设置多个样式**。我们可以为一个元素同时设多个样式，但只可以用类选择器的方法实现，ID选择器是不可以的（**不能使用 ID 词列表**）。

下面的代码是正确

	.stress{
		color:red;
	}
	.bigsize{
    	font-size:25px;
	}
	...
	<p>到了<span class="stress bigsize">三年级</span>下学期时，我们班上了一节公开课...</p>

上面代码的作用是为“三年级”三个文字设置文本颜色为红色并且字号为25px。

下面的代码是不正确的

	#stressid{
    	color:red;
	}
	#bigsizeid{
    	font-size:25px;
	}
	...
	<p>到了<span id="stressid bigsizeid">三年级</span>下学期时，我们班上了一节公开课...</p>

上面代码不可以实现为“三年级”三个文字设置文本颜色为红色并且字号为25px的作用。

### 子选择器 ###

子选择器，即大于符号(>),用于选择指定标签元素的第一代子元素。

	.food>li{border:1px solid red;}

这行代码会使class名为food下的子元素li加入红色实线边框。

### 包含(后代)选择器 ###

包含选择器，即加入空格,用于选择指定标签元素下的后辈元素。如右侧代码编辑器中的代码：

	.first span{color:red;}

这行代码会使class名为first下的子元素span字体颜色变为红色。

请注意这个选择器与子选择器的区别，子选择器（child selector）仅是指它的**直接后代**，或者你可以理解为作用于子元素的第一代后代。而后代选择器是作用于**所有子后代元素**。后代选择器通过空格来进行选择，而子选择器是通过“>”进行选择。

总结：**>**作用于元素的**第一代后代**，**空格**作用于元素的**所有后代**。

### 通用选择器 ###

通用选择器是功能最强大的选择器，它使用一个（*）号指定，它的作用是匹配html中所有标签元素，如下使用下面代码使用html中任意标签元素字体颜色全部设置为红色：

	* {color:red;}

### 伪类选择符 ###

伪类选择符允许给html不存在的标签（标签的某种状态）设置样式，比如说我们给html中一个标签元素的鼠标滑过的状态来设置字体颜色：

	a:hover{color:red;}

上面一行代码就是为 a 标签鼠标滑过的状态设置字体颜色变红。

关于伪选择符：

关于伪类选择符，到目前为止，可以兼容所有浏鉴器的“伪类选择符”就是 a 标签上使用 :hover 了（其实伪类选择符还有很多，尤其是 css3 中，但是不能兼容所有浏览器）。其实 :hover 可以放在任意的标签上，比如说 p:hover，但是它们的兼容性也是很不好的，所以现在比较常用的还是 a:hover 的组合。

### 分组选择符 ###

当你想为html中多个标签元素设置同一个样式时，可以使用分组选择符（，），如下代码为右侧代码编辑器中的h1、span标签同时设置字体颜色为红色：

	h1,span{color:red;}

它相当于下面两行代码：

	h1{color:red;}
	span{color:red;}

### 继承 ###

CSS的某些样式是具有继承性的，那么什么是继承呢？继承是一种规则，它允许样式不仅应用于某个特定html标签元素，而且应用于其后代。比如下面代码：如某种颜色应用于p标签，这个颜色设置不仅应用p标签，还应用于p标签中的所有子元素文本，这里子元素为span标签。

	p{color:red;}
	...
	<p>三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>

p中的文本与span中的文本都设置为了红色。但注意有一些css样式是不具有继承性的。如border:1px solid red;

	p{border:1px solid red;}
	...
	<p>三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>

在上面例子中它代码的作用只是给p标签设置了边框为1像素、红色、实心边框线，而对于子元素span是没用起到作用的。

### 特殊性 ###

有的时候我们为同一个元素设置了不同的CSS样式代码

	p{color:red;}
	.first{color:green;}
	...
	<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>

p和.first都匹配到了p这个标签上，green是正确的颜色，因为浏览器是根据权值来判断使用哪种css样式的，权值高的就使用哪种css样式。

下面是权值的规则：

标签的权值为1，类选择符的权值为10，ID选择符的权值最高为100。例如下面的代码：

	p{color:red;} /*权值为1*/
	p span{color:green;} /*权值为1+1=2*/
	.warning{color:white;} /*权值为10*/
	p span.warning{color:purple;} /*权值为1+1+10=12*/
	#footer .note p{color:yellow;} /*权值为100+10+1=111*/

注意：还有一个权值比较特殊--继承也有权值但很低，有的文献提出它只有0.1，所以可以理解为继承的权值最低。

### 层叠 ###

我们来思考一个问题：如果在html文件中对于同一个元素可以有多个css样式存在并且这多个css样式具有相同权重值怎么办？好，这一小节中的层叠帮你解决这个问题。

层叠就是在html文件中对于同一个元素可以有多个css样式存在，当有相同权重的样式存在时，会根据这些css样式的前后顺序来决定，处于最后面的css样式会被应用。

如下面代码:

	p{color:red;}
	p{color:green;}
	...
	<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>

最后 p 中的文本会设置为green，这个层叠很好理解，理解为后面的样式会覆盖前面的样式。

所以前面的css样式优先级就不难理解了：

内联样式表（标签内部）> 嵌入样式表（当前文件中）> 外部样式表（外部文件中）。

### 重要性 ###

我们在做网页代码的时，有些特殊的情况需要为某些样式设置具有最高权值，这时候可以使用!important来解决。

如下代码：

	p{color:red!important;}
	p{color:green;}
	...
	<p class="first">三年级时，我还是一个<span>胆小如鼠</span>的小女孩。</p>

这时 p 段落中的文本会显示的red红色。

**注意**：**!important要写在分号的前面**

这里注意当网页制作者不设置css样式时，浏览器会按照自己的一套样式来显示网页。并且用户也可以在浏览器中设置自己习惯的样式，比如有的用户习惯把字号设置为大一些，使其查看网页的文本更加清楚。这时注意样式优先级为：**浏览器默认的样式 < 网页制作者样式 < 用户自己设置的样式**，但记住**!important优先级样式是个例外，权值高于用户自己设置的样式**。

## 文字排版 ##

### 字体 ###

我们可以使用css样式为网页中的文字设置字体、字号、颜色等样式属性。下面代码实现：为网页中的文字设置字体为宋体。

	body{font-family:"宋体";}

这里注意不要设置不常用的字体，因为如果用户本地电脑上如果没有安装你设置的字体，就会显示浏览器默认的字体。（因为用户是否可以看到你设置的字体样式取决于用户本地电脑上是否安装你设置的字体。）

现在一般网页喜欢设置“微软雅黑”，如下代码：

	body{font-family:"Microsoft Yahei";}

或

	body{font-family:"微软雅黑";}

**注意**：第一种方法比第二种方法兼容性更好一些。

因为这种字体即美观又可以在客户端安全的显示出来（用户本地一般都是默认安装的）。

### 字号、颜色 ###

可以使用下面代码设置网页中文字的字号为12像素，并把字体颜色设置为#666(灰色)：

	body{font-size:12px;color:#666}

### 粗体 ###

Css样式还可以用来改变文字的样式：粗体、斜体、下划线、删除线，可以使用下面代码实现设置文字以粗体样式显示出来。

	p span{font-weight:bold;}

如果想为文字设置粗体是有单独的css样式来实现的，不用为了实现粗体样式而使用h1-h6或strong标签了。

### 斜体 ###

以下代码可以实现文字以斜体样式在浏览器中显示：

	p a{font-style:italic;}
	...
	<p>三年级时，我还是一个<a>胆小如鼠</a>的小女孩。</p>

### 下划线 ###

有些情况下想为文字设置为下划线样式，这样可以在视觉上强调文字，可以使用下面代码来实现：

	p a{text-decoration:underline;}
	...
	<p>三年级时，我还是一个<a>胆小如鼠</a>的小女孩。</p>

### 删除线 ###

删除线使用下面代码就可以实现：

	.oldPrice{text-decoration:line-through;}

### 缩进 ###

中文文字中的段前习惯空两个文字的空白，这个特殊的样式可以用下面代码来实现：

	p{text-indent:2em;}
	...
	<p>1922年的春天，一个想要成名名叫尼克卡拉威（托比?马奎尔Tobey Maguire 饰）的作家，离开了美国中西部，来到了纽约。那是一个道德感渐失，爵士乐流行，走私为王，股票飞涨的时代。为了追寻他的美国梦，他搬入纽约附近一海湾居住。</p>

**注意**：2em的意思就是文字的2倍大小。

### 行间距（行高） ###

如下代码实现设置段落行间距为1.5倍。

	p{line-height:1.5em;}
	...
	<p>菲茨杰拉德，二十世纪美国文学巨擘之一，兼具作家和编剧双重身份。他以诗人的敏感和戏剧家的想象为"爵士乐时代"吟唱华丽挽歌，其诗人和梦想家的气质亦为那个奢靡年代的不二注解。</p>

### 中文字间距、字母间距 ###

#### 中文字间隔、字母间隔设置 ####

如果想在网页排版中设置文字间隔或者字母间隔就可以使用`letter-spacing`来实现，如下面代码：

	h1{
    	letter-spacing:50px;
	}
	...
	<h1>了不起的盖茨比</h1>

**注意**：这个样式使用在英文单词时，是设置字母与字母之间的间距。

#### 单词间距设置 ####

单词间距设置可以使用 word-spacing 来实现。如下代码：

	h1{
    	word-spacing:50px;
	}
	...
	<h1>welcome to imooc!</h1>

### 对齐 ###

`text-align`样式代码可以为块状元素中的文本、图片设置居中样式，如下代码可实现文本居中显示。

	h1{
    	text-align:center;
	}
	...
	<h1>了不起的盖茨比</h1>

同样可以设置居左：

	h1{
    	text-align:left;
	}
	...
	<h1>了不起的盖茨比</h1>

还可以设置居右：

	h1{
    	text-align:right;
	}
	...
	<h1>了不起的盖茨比</h1>

## 元素分类 ##

在CSS中，html中的标签元素大体被分为三种不同的类型：块状元素、内联元素(又叫行内元素)和内联块状元素。

常用的块状元素有：

	<div>、<p>、<h1>...<h6>、<ol>、<ul>、<dl>、<table>、<address>、<blockquote> 、<form>

常用的内联元素有：

	<a>、<span>、<br>、<i>、<em>、<strong>、<label>、<q>、<var>、<cite>、<code>

常用的内联块状元素有：

	<img>、<input>

### 块级元素 ###

在html中`<div>`、 `<p>`、`<h1>`、`<form>`、`<ul>` 和 `<li>`就是块级元素。设置display:block就是将元素显示为块级元素。如下代码就是将内联元素a转换为块状元素，从而使a元素具有块状元素特点。

	a{display:block;}

块级元素特点：

1. 每个块级元素都从新的一行开始，并且其后的元素也另起一行。（一个块级元素独占一行）

2. 元素的高度、宽度、行高以及顶和底边距都可设置。

3. 元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。

### 内联元素 ###

在html中，`<span>`、`<a>`、`<label>`、 `<strong>` 和`<em>`就是典型的内联元素（行内元素）（inline）元素。当然块状元素也可以通过代码display:inline将元素设置为内联元素。如下代码就是将块状元素div转换为内联元素，从而使 div 元素具有内联元素特点。

	div{
    	display:inline;
	}
	...
	<div>我要变成内联元素</div>

内联元素特点：

1. 和其他元素都在一行上；

2. 元素的高度、宽度及顶部和底部边距不可设置；

3. 元素的宽度就是它包含的文字或图片的宽度，不可改变。

### 内联块状元素 ###

内联块状元素（inline-block）就是同时具备内联元素、块状元素的特点，代码display:inline-block就是将元素设置为内联块状元素。(css2.1新增)，`<img>`、`<input>`标签就是这种内联块状标签。

inline-block 元素特点：

1. 和其他元素都在一行上；

2. 元素的高度、宽度、行高以及顶和底边距都可设置。

## 盒模型 ##

盒模型由里向外由content,padding,border,margin组成。

盒模型是有两种标准的，一个是标准模型，一个是IE模型。

![](https://images2017.cnblogs.com/blog/1265396/201711/1265396-20171119143703656-1332857321.png)

![](https://images2017.cnblogs.com/blog/1265396/201711/1265396-20171119144229156-49945808.png)

从上面两图不难看出在标准模型中，盒模型的宽高只是内容（content）的宽高，

而在IE模型中盒模型的宽高是内容(content)+填充(padding)+边框(border)的总宽高。

### 边框 ###

盒子模型的边框就是围绕着内容及补白的线，这条线你可以设置它的粗细、样式和颜色(边框三个属性)。

如下面代码为 div 来设置边框粗细为 2px、样式为实心的、颜色为红色的边框：

	div{
    	border:2px  solid  red;
	}

上面是 border 代码的缩写形式，可以分开写：

	div{
    	border-width:2px;
    	border-style:solid;
    	border-color:red;
	}

**注意**：

1. border-style（边框样式）常见样式有：

	dashed（虚线）| dotted（点线）| solid（实线）。

2. border-color（边框颜色）中的颜色可设置为十六进制颜色，如:

	border-color:#888;//前面的井号不要忘掉。

3. border-width（边框宽度）中的宽度也可以设置为：

	thin | medium | thick（但不是很常用），最常还是用象素（px）。

CSS 样式中允许只为一个方向的边框设置样式：

	div{border-bottom:1px solid red;}

同样可以使用下面代码实现其它三边(上、右、左)边框的设置：

	border-top:1px solid red;
	border-right:1px solid red; 
	border-left:1px solid red;

### 宽度和高度 ###

盒模型宽度和高度和我们平常所说的物体的宽度和高度理解是不一样的，css内定义的宽（width）和高（height），指的是填充以里的内容范围。

因此一个元素实际宽度（盒子的宽度）=左边界+左边框+左填充+内容宽度+右填充+右边框+右边界。

![](http://img.mukewang.com/539fbb3a0001304305570259.jpg)

元素的高度也是同理。

比如：

css代码：

	div{
    	width:200px;
    	padding:20px;
    	border:1px solid red;
    	margin:10px;    
	}

html代码：

	<body>
		<div>文本内容</div>
	</body>

元素的实际长度为：10px+1px+20px+200px+20px+1px+10px=262px。在chrome浏览器下可查看元素盒模型，如下图：

![](http://img.mukewang.com/543b4cae0001b34304300350.jpg)

### 填充 ###

元素内容与边框之间是可以设置距离的，称之为“填充”。填充也可分为上、右、下、左(顺时针)。如下代码：

	div{padding:20px 10px 15px 30px;}

顺序一定不要搞混。可以分开写上面代码：

	div{
		padding-top:20px;
		padding-right:10px;
		padding-bottom:15px;
		padding-left:30px;
	}

如果上、右、下、左的填充都为10px;可以这么写

	div{padding:10px;}

如果上下填充一样为10px，左右一样为20px，可以这么写：

	div{padding:10px 20px;}

### 边界 ###

元素与其它元素之间的距离可以使用边界（margin）来设置。边界也是可分为上、右、下、左。如下代码：

	div{margin:20px 10px 15px 30px;}

也可以分开写：

	div{
		margin-top:20px;
		margin-right:10px;
		margin-bottom:15px;
		margin-left:30px;
	}

如果上右下左的边界都为10px;可以这么写：

	div{ margin:10px;}

如果上下边界一样为10px，左右一样为20px，可以这么写：

	div{ margin:10px 20px;}

总结一下：padding和margin的区别，padding在边框里，margin在边框外。

## css布局模型 ##

布局模型与盒模型一样都是 CSS 最基本、 最核心的概念。 但布局模型是建立在盒模型基础之上，又不同于我们常说的 CSS 布局样式或 CSS 布局模板。如果说布局模型是本，那么 CSS 布局模板就是末了，是外在的表现形式。 

CSS包含3种基本的布局模型，用英文概括为：Flow、Layer 和 Float。

在网页中，元素有三种布局模型：

1. 流动模型（Flow）

2. 浮动模型 (Float)

3. 层模型（Layer）

### 流动模型 ###

流动（Flow）是默认的网页布局模式。也就是说网页在默认状态下的 HTML 网页元素都是根据流动模型来分布网页内容的。

流动布局模型具有2个比较典型的特征：

第一点，块状元素都会在所处的包含元素内自上而下按顺序垂直延伸分布，因为在默认状态下，块状元素的宽度都为100%。实际上，块状元素都会以行的形式占据位置。

第二点，在流动模型下，内联元素都会在所处的包含元素内从左到右水平分布显示。

### 浮动模型 ###

设置元素浮动可以实现让两个块状元素并排显示。

任何元素在默认情况下是不能浮动的，但可以用 CSS 定义为浮动，如 div、p、table、img 等元素都可以被定义为浮动。如下代码可以实现两个 div 元素一行显示。

	div{
    	width:200px;
    	height:200px;
    	border:2px red solid;
    	float:left;
	}
	...
	<div id="div1"></div>
	<div id="div2"></div>

效果图

![](http://img.mukewang.com/540e62c60001c56a06760417.jpg)

当然你也可以同时设置两个元素右浮动也可以实现一行显示。

	div{
    	width:200px;
    	height:200px;
    	border:2px red solid;
    	float:right;
	}

效果图

![](http://img.mukewang.com/540e632b0001f5f506760417.jpg)

设置两个元素一左一右也可以实现一行显示：

	div{
    	width:200px;
    	height:200px;
    	border:2px red solid;
	}
	#div1{float:left;}
	#div2{float:right;}

效果图

![](http://img.mukewang.com/540e63b50001f6a206760417.jpg)

### 层模型 ###

层布局模型就像是图像软件PhotoShop中非常流行的图层编辑功能一样，每个图层能够精确定位操作，但在网页设计领域，由于网页大小的活动性，层布局没能受到热捧。但是在网页上局部使用层布局还是有其方便之处的。

如何让html元素在网页中精确定位，就像图像软件PhotoShop中的图层一样可以对每个图层能够精确定位操作。CSS定义了一组定位（positioning）属性来支持层布局模型。

层模型有三种形式：

1. 绝对定位(position: absolute)

2. 相对定位(position: relative)

3. 固定定位(position: fixed)

#### 绝对定位 ####

如果想为元素设置层模型中的绝对定位，需要设置position:absolute(表示绝对定位)，这条语句的作用将元素从文档流中拖出来，然后使用left、right、top、bottom属性相对于其最接近的一个具有定位属性的父包含块进行绝对定位。如果不存在这样的包含块，则相对于body元素，即相对于浏览器窗口。

如下面代码可以实现div元素相对于浏览器窗口向右移动100px，向下移动50px。

	div{
    	width:200px;
    	height:200px;
    	border:2px red solid;
    	position:absolute;
    	left:100px;
    	top:50px;
	}
	...
	<div id="div1"></div>

效果如下：

![](http://img.mukewang.com/53a00b130001e86707360547.jpg)

#### 相对定位 ####

如果想为元素设置层模型中的相对定位，需要设置position:relative（表示相对定位），它通过left、right、top、bottom属性确定元素在正常文档流中的偏移位置。相对定位完成的过程是首先按static(float)方式生成一个元素(并且元素像层一样浮动了起来)，然后相对于以前的位置移动，移动的方向和幅度由left、right、top、bottom属性确定，偏移前的位置保留不动。

如下代码实现相对于以前位置向下移动50px，向右移动100px;

	#div1{
    	width:200px;
    	height:200px;
    	border:2px red solid;
    	position:relative;
    	left:100px;
    	top:50px;
	}
	...
	<div id="div1"></div>

效果图：

![](http://img.mukewang.com/53a00d2b00015c4b06190509.jpg)

偏移前的位置保留不动:

如下代码：

	<body>
    	<div id="div1"></div><span>偏移前的位置还保留不动，覆盖不了前面的div没有偏移前的位置</span>
	</body>

效果图：

![](http://img.mukewang.com/541a4bfc0001abef05940489.jpg)

从效果图中可以明显的看出，虽然div元素相对于以前的位置产生了偏移，但是div元素以前的位置还是保留着，所以后面的span元素是显示在了div元素以前位置的后面。

#### 固定定位 ####

fixed：表示固定定位，与absolute定位类型类似，但它的相对移动的坐标是视图（**屏幕内的网页窗口**）本身。由于视图本身是固定的，它不会随浏览器窗口的滚动条滚动而变化，除非你在屏幕中移动浏览器窗口的屏幕位置，或改变浏览器窗口的显示大小，因此固定定位的元素会始终位于浏览器窗口内视图的某个位置，不会受文档流动影响，这与background-attachment:fixed;属性功能相同。以下代码可以实现相对于浏览器视图向右移动100px，向下移动50px。并且拖动滚动条时位置固定不变。

	#div1{
    	width:200px;
    	height:200px;
		border:2px red solid;
    	position:fixed;
    	left:100px;
    	top:50px;
	}
	<p>文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本。</p>
	....

#### Relative与Absolute组合使用 ####

使用position:absolute可以实现被设置元素相对于浏览器（body）设置定位以后，使用position:relative可以实现相对于其它元素进行定位，但是必须遵守下面规范：

1、参照定位的元素必须是相对定位元素的前辈元素：

	<div id="box1"><!--参照定位的元素-->
    	<div id="box2">相对参照元素进行定位</div><!--相对定位元素-->
	</div>

从上面代码可以看出box1是box2的父元素（父元素当然也是前辈元素了）。

2、参照定位的元素必须加入position:relative;

	#box1{
    	width:200px;
    	height:200px;
    	position:relative;        
	}

3、定位元素加入position:absolute，便可以使用top、bottom、left、right来进行偏移定位了。

	#box2{
    	position:absolute;
    	top:20px;
    	left:30px;         
	}

这样box2就可以相对于父元素box1定位了（这里注意参照物就可以不是浏览器了，而可以自由设置了）。

## CSS代码缩写 ##

CSS代码缩写可以占用更少的带宽。

### 盒模型代码简写 ###

盒模型外边距(margin)、内边距(padding)和边框(border)设置上下左右四个方向的边距是按照顺时针方向设置的：上右下左。具体应用在margin和padding的例子如下：

	margin:10px 15px 12px 14px;/*上设置为10px、右设置为15px、下设置为12px、左设置为14px*/

通常有下面三种缩写方法:

1、如果top、right、bottom、left的值相同，如下面代码：

	margin:10px 10px 10px 10px;

可缩写为：

	margin:10px;

2、如果top和bottom值相同、left和 right的值相同，如下面代码：

	margin:10px 20px 10px 20px;

可缩写为：

	margin:10px 20px;

3、如果left和right的值相同，如下面代码：

	margin:10px 20px 30px 20px;

可缩写为：

	margin:10px 20px 30px;

**注意**：padding、border的缩写方法和margin是一致的。

### 颜色值缩写 ###

当你设置的颜色是16进制的色彩值时，如果每两位的值相同，可以缩写一半。

例子1：

	p{color:#000000;}

可以缩写为：

	p{color: #000;}

例子2：

	p{color: #336699;}

可以缩写为：

	p{color: #369;}

### 字体缩写 ###

网页中的字体css样式代码也有他自己的缩写方式，下面是给网页设置字体的代码：

	body{
    	font-style:italic;
    	font-variant:small-caps; 
    	font-weight:bold; 
    	font-size:12px; 
    	line-height:1.5em; 
    	font-family:"宋体",sans-serif;
	}

这么多行的代码其实可以缩写为一句：

	body{
	    font:italic  small-caps  bold  12px/1.5em  "宋体",sans-serif;
	}

注意：

1. 使用这一简写方式你至少要指定 font-size 和 font-family 属性，其他的属性(如 font-weight、font-style、font-variant、line-height)如未指定将自动使用默认值。

2. 在缩写时 font-size 与 line-height 中间要加入“/”斜扛。

一般情况下因为对于中文网站，英文还是比较少的，所以下面缩写代码比较常用：

	body{
    	font:12px/1.5em  "宋体",sans-serif;
	}

只是有字号、行间距、中文字体、英文字体设置。

## 颜色值 ##

在网页中的颜色设置是非常重要，有字体颜色（color）、背景颜色（background-color）、边框颜色（border）等，设置颜色的方法也有很多种：

1、英文命令颜色

前面几个小节中经常用到的就是这种设置方法：

	p{color:red;}

2、RGB颜色

这个与 photoshop 中的 RGB 颜色是一致的，由 R(red)、G(green)、B(blue) 三种颜色的比例来配色。

	p{color:rgb(133,45,200);}

每一项的值可以是 0~255 之间的整数，也可以是 0%~100% 的百分数。如：

	p{color:rgb(20%,33%,25%);}

3、十六进制颜色

这种颜色设置方法是现在比较普遍使用的方法，其原理其实也是 RGB 设置，但是其每一项的值由 0-255 变成了十六进制 00-ff。

	p{color:#00ffff;}

配色表：

![](http://img.mukewang.com/54c5b4120001f20808000902.jpg)

## 长度值 ##

目前比较常用到的长度单位有px（像素）、em、% 百分比，要注意其实这三种单位都是**相对单位**。

1、像素

像素指的是显示器上的小点（CSS规范中假设“90像素=1英寸”），所以像素是相对单位呢。实际情况是浏览器会使用显示器的实际像素值有关，在目前大多数的设计者都倾向于使用像素（px）作为单位。

2、em

就是本元素给定字体的 font-size 值，如果元素的 font-size 为 14px ，那么 1em = 14px；如果 font-size 为 18px，那么 1em = 18px。如下代码：

	p{font-size:12px;text-indent:2em;}

上面代码就是可以实现段落首行缩进 24px（也就是两个字体大小的距离）。

下面注意一个特殊情况：

但当给 font-size 设置单位为 em 时，此时计算的标准以 p 的父元素的 font-size 为基础。如下代码：

html:

	<p>以这个<span>例子</span>为例。</p>

css:

	p{font-size:14px}
	span{font-size:0.8em;}

结果 span 中的字体“例子”字体大小就为 11.2px（14 * 0.8 = 11.2px）。

3、百分比

	p{font-size:12px;line-height:130%}

设置行高（行间距）为字体的130%（12 * 1.3 = 15.6px）。

## 水平居中 ##

### 行内元素 ###

如果被设置元素为文本、图片等行内元素时，水平居中是通过给父元素设置 text-align:center 来实现的。(父元素和子元素：如下面的html代码中，div是“我想要在父容器中水平居中显示”这个文本的父元素。反之这个文本是div的子元素 )如下代码：

html代码：

	<body>
		<div class="txtCenter">我想要在父容器中水平居中显示。</div>
	</body>

css代码：

	<style>
	.txtCenter{
    	text-align:center;
	}
	</style>

### 定宽块状元素 ###

当被设置元素为 块状元素 时用 text-align：center 就不起作用了，这时也分两种情况：定宽块状元素和不定宽块状元素。

定宽块状元素：块状元素的宽度width为固定值。

满足定宽和块状两个条件的元素是可以通过设置“左右margin”值为“auto”来实现居中的。我们来看个例子就是设置 div 这个块状元素水平居中：

html代码：

	<body>
	<div>我是定宽块状元素，哈哈，我要水平居中显示。</div>
	</body>

css代码：

	<style>
	div{
    	border:1px solid red;/*为了显示居中效果明显为 div 设置了边框*/
		width:200px;/*定宽*/
    	margin:20px auto;/* margin-left 与 margin-right 设置为 auto */
	}
	</style>
也可以写成：

	margin-left:auto;
	margin-right:auto;

注意：元素的“上下 margin” 是可以随意设置的。

### 不定宽块状元素 ###

在实际工作中我们会遇到需要为“不定宽度的块状元素”设置居中，比如网页上的分页导航，因为分页的数量是不确定的，所以我们不能通过设置宽度来限制它的弹性。(不定宽块状元素：块状元素的宽度width不固定。)

不定宽度的块状元素有三种方法居中（这三种方法目前使用的都很多）：

1. 加入 table 标签
2. 设置 display: inline 方法：与第一种类似，显示类型设为 行内元素，进行不定宽元素的属性设置
3. 设置 position:relative 和 left:50%：利用 相对定位 的方式，将元素向左偏移 50% ，即达到居中的目的

**方法一**：利用table标签的长度自适应性---即不定义其长度也不默认父元素body的长度（table其长度根据其内文本长度决定），因此可以看做一个定宽度块元素，然后再利用定宽度块状居中的margin的方法，使其水平居中。

第一步：为需要设置的居中的元素外面加入一个 table 标签 ( 包括 `<tbody>`、`<tr>`、`<td>` )。

第二步：为这个 table 设置“左右 margin 居中”（这个和定宽块状元素的方法一样）。

举例如下：

html代码：

	<div>
		<table>
			<tbody>
				<tr><td>
					<ul>
						<li>我是第一行文本</li>
						<li>我是第二行文本</li>
						<li>我是第三行文本</li>
					</ul>
				</td></tr>
			</tbody>
		</table>
	</div>

css代码：

	<style>
	table{
    	border:1px solid;
    	margin:0 auto;
	}
	</style>

**方法二**：改变块级元素的 display 为 inline 类型（设置为 行内元素 显示），然后使用 text-align:center 来实现居中效果。如下例子：

html代码：

	<body>
	<div class="container">
    	<ul>
        	<li><a href="#">1</a></li>
        	<li><a href="#">2</a></li>
        	<li><a href="#">3</a></li>
    	</ul>
	</div>
	</body>

css代码：

	<style>
	.container{
    	text-align:center;
	}
	/* margin:0;padding:0（消除文本与div边框之间的间隙）*/
	.container ul{
    	list-style:none;
    	margin:0;
    	padding:0;
    	display:inline;
	}
	/* margin-right:8px（设置li文本之间的间隔）*/
	.container li{
    	margin-right:8px;
    	display:inline;
	}
	</style>

这种方法相比第一种方法的优势是不用增加无语义标签，但也存在着一些问题：它将块状元素的 display 类型改为 inline，变成了行内元素，所以少了一些功能，比如设定长度值。

**方法三**：通过给父元素设置 float，然后给父元素设置 position:relative 和 left:50%，子元素设置 position:relative 和 left: -50% 来实现水平居中。

我们可以这样理解：假想ul层的父层（即下面例子中的div层）中间有条平分线将ul层的父层（div层）平均分为两份，ul层的css代码是将ul层的最左端与ul层的父层（div层）的平分线对齐；而li层的css代码则是将li层的平分线与ul层的最左端（也是div层的平分线）对齐，从而实现li层的居中。

代码如下：

html代码：

	<body>
	<div class="container">
    	<ul>
        	<li><a href="#">1</a></li>
        	<li><a href="#">2</a></li>
        	<li><a href="#">3</a></li>
    	</ul>
	</div>
	</body>

css代码：

	<style>
	.container{
    	float:left;
    	position:relative;
    	left:50%
	}
	.container ul{
    	list-style:none;
    	margin:0;
    	padding:0;
    	position:relative;
    	left:-50%;
	}
	.container li{float:left;display:inline;margin-right:8px;}
	</style>
 
这三种方法使用得都非常广泛，各有优缺点，具体选用哪种方法，可以视具体情况而定。

## 垂直居中 ##

### 父元素高度确定的单行文本 ###

父元素高度确定的单行文本的竖直居中的方法是通过设置父元素的 height 和 line-height 高度一致来实现的。(height: 该元素的高度，line-height: 顾名思义，行高（行间距），指在文本中，行与行之间的 基线间的距离 )。

line-height 与 font-size 的计算值之差，在 CSS 中成为“行间距”。分为两半，分别加到一个文本行内容的顶部和底部。

这种文字行高与块高一致带来了一个弊端：当文字内容的长度大于块的宽时，就有内容脱离了块。

如下代码：

	<div class="container">
    	hi,imooc!
	</div>

css代码：

	<style>
	.container{
    	height:100px;
    	line-height:100px;
    	background:#999;
	}
	</style>

### 父元素高度确定的多行文本、图片 ###

父元素高度确定的多行文本、图片等的竖直居中的方法有两种：

**方法一**：使用插入 table  (包括tbody、tr、td)标签，同时设置 vertical-align：middle。

css 中有一个用于竖直居中的属性 vertical-align，在父元素设置此样式时，会对inline-block类型的子元素都有用。下面看一下例子：

html代码：

	<body>
	<table><tbody><tr><td class="wrap">
	<div>
    	<p>看我是否可以居中。</p>
	</div>
	</td></tr></tbody></table>
	</body>

css代码：

	table td{height:500px;background:#ccc}

因为 td 标签默认情况下就默认设置了 vertical-align 为 middle，所以我们不需要显式地设置了。

**方法二**：在 chrome、firefox 及 IE8 以上的浏览器下可以设置块级元素的 display 为 table-cell（设置为表格单元显示），激活 vertical-align 属性，但注意 IE6、7 并不支持这个样式, 兼容性比较差。

html代码：

	<div class="container">
    	<div>
        	<p>看我是否可以居中。</p>
        	<p>看我是否可以居中。</p>
        	<p>看我是否可以居中。</p>
    	</div>
	</div>

css代码：

	<style>
	.container{
    	height:300px;
    	background:#ccc;
    	display:table-cell;/*IE8以上及Chrome、Firefox*/
    	vertical-align:middle;/*IE8以上及Chrome、Firefox*/
	}
	</style>

这种方法的好处是不用添加多余的无意义的标签，但缺点也很明显，它的兼容性不是很好，不兼容 IE6、7而且这样修改display的block变成了table-cell，破坏了原有的块状元素的性质。

## 隐性改变display类型 ##

当为元素（不论之前是什么类型元素，display:none 除外）设置以下 2 个句之一：

 1. position : absolute 

 2. float : left 或 float:right 

简单来说，只要html代码中出现以上两句之一，元素的display显示类型就会自动变为以 display:inline-block（块状元素）的方式显示，当然就可以设置元素的 width 和 height 了，且默认宽度不占满父元素。

如下面的代码， a 标签是 行内元素 ，所以设置它的 width 是 没有效果的，但是设置为 position:absolute 以后，就可以了。

	<div class="container">
    	<a href="#" title="">进入课程请单击这里</a>
	</div>

css代码

	<style>
	.container a{
    	position:absolute;
    	width:200px;
    	background:#ccc;
	}
	</style>



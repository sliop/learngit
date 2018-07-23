# Git #

## 全局设置 ##

输入名字：

    git config --global user.name "Your name" 

输入E-mail：

	git config --global user.email "email@example.com"

让Git显示颜色：

	git config --global color.ui true

## 其他命令 ##

添加文件到仓库：

	git add <file>

提交文件到仓库：

	git commit -m <message> 

新建文件夹：

    mkdir <file>

进入文件夹：

    cd <file name>

创建git仓库：

	git init			

查看仓库当前状态：

	git status

查看文件变化：

	git diff <file>

显示从最近到最远的提交日志：

	git log

用一行来显示从最近到最远的提交日志：
	
	git log --pretty=oneline

回退到指定版本:

	git reset --hard <Commit ID>


> 也可用"HEAD"表示当前版本，"HEAD^"表示上一版本，"HEAD^^"表示上两个版本,"HEAD~N"表示上N个版本。

查看命令历史：

	git reflog

丢弃工作区的修改：

	git checkout -- <file>

丢弃暂存区的修改，工作区的修改仍然不变，还需上一步命令来丢弃工作区修改：

	git reset HEAD <file>

用于删除文件：

	git rm <file>

创建SSH Key：

	ssh-keygen -t rsa -C "email@example.com"

> 并不是Git命令，用命令提示行运行。

关联远程库：

    git remote add origin git@server-name:path/repo-name.git

----------

    git remote add origin https://server-name/path/repo-name.git

> Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快,其中origin是远程库的名字。

删除已关联的远程库：

    git remote rm origin

> 其中origin为远程库的名字。

第一次推送master分支的所有内容并将远程与本地分支关联：

	git push -u origin

推送master分支的修改：

	git push origin master

克隆远程库：

	git clone git@server-name:path/repo-name.git

查看分支：

	git branch

创建分支：

	git branch <branchname>

切换分支：

	git checkout <branchname>

创建并切换分支：

	git checkout -b <branchname>

合并某分支到当前分支：

	git merge <branchname>

删除分支：

	git branch -d <branchname>

强制修改分支位置

	git branch -f <branchname> <Commit ID>

查看分支合并图：

	git log --graph --pretty=oneline --abbrev-commit

用普通模式合并分支，合并后的历史有分支：

	git merge --no-ff -m 'message' <branchname>

暂时储存工作现场：

	git stash

回到工作现场并删除stash内容：

	git stash pop

恢复到指定的stash N：

	git stash apply stash@{N}

查看stash内容：

	git stash list

删除stash内容：
	
	git stash drop

强行删除一个没有被合并过的分支：

	git branch -D <branchname>

查看远程库信息：

	git remote -v

从本地推送分支：

	git push origin <branchname>

抓取远程的新提交：

	git pull

在本地创建和远程分支对应的分支,本地和远程分支的名字最好一致：

	git checkout -b <branchname> origin/<branchname>

建立本地分支与远程分支的关联：

	git branch --set-upstream <branchname> origin/<branchname>

新建标签：

	git tag <tagname> <Commit ID>

> 如果不输入Commit ID,则默认为HEAD。

指定标签信息：

	git tag -a <tagname> -m 'message' <Commit ID>

查看所有标签：

	git tag

推送一个本地标签：

	git push origin <tagname>

推送全部未推送过的本地标签：

	git push origin --tags

删除一个本地标签:

	git tag -d <tagname>

删除一个远程标签:

	git push origin :refs/tags/<tagname>

## 忽略特殊文件 ##

在Git工作区的根目录下创建一个特殊的.gitignore文件，然后把要忽略的文件名填进去，Git就会自动忽略这些文件。

不需要从头写.gitignore文件，GitHub已经为我们准备了各种配置文件，只需要组合一下就可以使用了。所有配置文件可以直接在线浏览：[https://github.com/github/gitignore](https://github.com/github/gitignore)

然后把`.gitignore`提交到Git，当有文件被`.gitignore`忽略时可以使用`-f`强制添加到Git:

	git add -f <file>

当`.gitignore`写得有问题，需要找出来到底哪个规则写错了，可以用`git check-ignore`命令检查：
    
	$ git check-ignore -v App.class
    .gitignore:3:*.classApp.class

Git会告诉我们，`.gitignore`的第3行规则忽略了该文件，于是我们就可以知道应该修订哪个规则。

## 配置别名 ##

	git config --global alias.<别名> <想取代的命令>

如过想用`st`表示`status`：

	git config --global alias.st status

> 配置Git的时候，加上--global是针对当前用户起作用的，如果不加，那只针对当前的仓库起作用。

每个仓库的Git配置文件都放在`.git/config`文件中：

    $ cat .git/config 
    [core]
    	repositoryformatversion = 0
    	filemode = true
    	bare = false
    	logallrefupdates = true
    	ignorecase = true
    	precomposeunicode = true
    [remote "origin"]
    	url = git@github.com:michaelliao/learngit.git
    	fetch = +refs/heads/*:refs/remotes/origin/*
    	[branch "master"]
    	remote = origin
    merge = refs/heads/master
    [alias]
    	last = log -1

> 别名就在`[alias]`后面，要删除别名，直接把对应的行删掉即可。

> 而当前用户的Git配置文件放在用户主目录下的一个隐藏文件`.gitconfig`中：

> 	
	$ cat .gitconfig
	[alias]
    	co = checkout
    	ci = commit
    	br = branch
    	st = status
	[user]
    	name = Your Name
    	email = your@email.com

> 配置别名也可以直接修改这个文件，如果改错了，可以删掉文件重新通过命令配置。

## Git分支 ##

复制提交到当前所在的位置（`HEAD`):

	git cherry-pick <Commit ID>

合并分支2到分支1:

	git rebase <branchname1> <branchname2>

> 如果省略`<branchname2>`则表示合并当前分支到分支1。

交互式rebase:

	git rebase -i <Commit ID>

> 当 rebase UI界面打开时, 你能做3件事:

> - 调整提交记录的顺序（通过鼠标拖放来完成）

> - 删除你不想要的提交（通过切换 pick 的状态来完成，关闭就意味着你不想要这个提交记录）

> - 合并提交。 遗憾的是由于某种逻辑的原因，我们的课程不支持此功能，因此我不会详细介绍这个操作。简而言之，它允许你把多个提交记录合并成一个。

`git describe`的​​语法是：

    git describe <ref>

> `<ref>`可以是任何能被Git识别成提交记录的引用，如果你没有指定的话，Git会以你目前所检出的位置（`HEAD`）。

> 它输出的结果是这样的：

>     <tag>_<numCommits>_g<hash>

> `tag`表示的是离ref最近的标签，`numCommits`是表示这个`ref`与`tag`相差有多少个提交记录，`hash`表示的是你所给定的`ref`所表示的提交记录哈希值的前几位。

> 当ref提交记录上有某个标签时，则只输出标签名称。

拉取远程提交并rebase:

	git pull --rebase

创建一个新分支1并跟踪远程分支2

	git checkout -b <branchname1> <remote/branchname2>

分支1跟踪远程分支2

	git branch -u <remote/branchname2> <branchname1>

> 如果省略`<branchname1>`，则表示当前分支跟踪远程分支2。

**指定`git push`参数**

将指定的本地分支推送到远程库：

	git push <remote> <place>

将本地的某分支推送到远程库的某分支：

	git push <remote> <source>:<destination>

> 其中remote是远程库的名字如origin，source是Git能识别的位置如分支foo或者是HEAD^，destination是远程库中分支的名称，如果指定的分支不存在，将在远程创建该分支。 

> `git fetch`同理。当push指定的source为空时，会删除远程仓库中的分支，而当fetch指定的source为空时，将在本地创建该分支。

> 而对于

> 	git pull <remote> <source>:<destination>

> 其等效于

> 	git fetch <remote> <source>:<destination>
	git merge <destination>

# HTML #

## Html和CSS的关系 ##

1. HTML是网页内容的载体。内容就是网页制作者放在页面上想要让用户浏览的信息，可以包含文字、图片、视频等。

2. CSS样式是表现。就像网页的外衣。比如，标题字体、颜色变化，或为标题加入背景图片、边框等。所有这些用来改变内容外观的东西称之为表现。

3. JavaScript是用来实现网页上的特效效果。如：鼠标滑过弹出下拉菜单。或鼠标滑过表格的背景颜色改变。还有焦点新闻（新闻图片）的轮换。可以这么理解，有动画的，有交互的一般都是用JavaScript来实现的。

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

### html文件基本结构 ###

HTML文件是有自己固定的结构的。

	<html>
    	<head>...</head>
		<body>...</body>
	</html>

代码讲解：

1. `<html></html>`称为根标签，所有的网页标签都在`<html></html>`中。

2. `<head>`标签用于定义文档的头部，它是所有头部元素的容器。头部元素有`<title>`、`<script>`、`<style>`、`<link>`、`<meta>`等标签，头部标签在下一小节中会有详细介绍。

3. 在`<body>`和`</body>`标签之间的内容是网页的主要内容，如`<h1>`、`<p>`、`<a>`、`<img>`等网页内容标签，在这里的标签中的内容会在浏览器中显示出来。


### 语义化 ###

好处：

1. 更容易被搜索引擎收录。

2. 更容易让屏幕阅读器读出网页内容。

# CSS #

表格边框：

	<style type="text/css">
	table tr td,th{border:1px solid #000;}
	</style>

> 效果为为th，td单元格添加粗细为一个像素的黑色边框。



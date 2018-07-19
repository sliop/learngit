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

	git ssh-keyge -t rsa -C "email@example.com"

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

> 	$ cat .gitconfig
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
    git config --global user.name "Your name" 

	git config --global user.email "email@example.com"

添加文件到仓库

	git add <file>

提交文件到仓库

	git commit -m <message> 

新建文件夹

    mkdir <file>

进入文件夹

    cd <file name>

创建git仓库

	git init			

查看仓库当前状态

	git status

查看文件变化

	git diff <file>

显示从最近到最远的提交日志

	git log

用一行来显示从最近到最远的提交日志
	
	git log --pretty=oneline

回退到指定版本，版本号可以是Commit ID，也可以用"HEAD"表示当前版本，"HEAD^"表示上一版本，"HEAD^^"表示上两个版本,"HEAD~N"表示上N个版本

	git reset --hard <版本号>

查看命令历史

	git reflog

丢弃工作区的修改

	git checkout -- <file>

丢弃暂存区的修改，工作区的修改仍然不变，还需上一步命令来丢弃工作区修改

	git reset HEAD <file>

用于删除文件

	git rm <file>

创建SSH Key

	git ssh-keyge -t rsa -C "email@example.com"

关联远程库

    git remote add origin git@server-name:path/repo-name.git

----------

    git remote add origin https://server-name/path/repo-name.git

**Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。**

第一次推送master分支的所有内容并将远程与本地分支关联

	git push -u origin

推送master分支的修改

	git push origin master

克隆远程库

	git clone git@server-name:path/repo-name.git

查看分支

	git branch

创建分支

	git branch <branchname>

切换分支

	git checkout <branchname>

创建并切换分支

	git checkout -b <branchname>

合并某分支到当前分支

	git merge <branchname>

删除分支

	git branch -d <branchname>

查看分支合并图

	git log --graph --pretty=oneline --abbrev-commit

用普通模式合并分支，合并后的历史有分支

	git merge --no-ff -m 'message' <branchname>

暂时储存工作现场

	git stash

回到工作现场并删除stash内容

	git stash pop

恢复到指定的stash N

	git stash apply stash@{N}

查看stash内容

	git stash list

删除stash内容
	
	git stash drop

强行删除一个没有被合并过的分支

	git branch -D <branchname>

查看远程库信息

	git remote -v

从本地推送分支

	git push origin <branchname>

抓取远程的新提交

	git pull

在本地创建和远程分支对应的分支,本地和远程分支的名字最好一致

	git checkout -b <branchname> origin/<branchname>

建立本地分支与远程分支的关联
	git branch --set-upstream <branchname> origin/<branchname>



	git tag <tagname>
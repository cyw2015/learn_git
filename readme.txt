Git is a version control system.
Git is free software distributed under the GPL.

初始化Git仓库 git init
添加文件到Git仓库 
	1 git add <file>
	2 git commit -m  <note>

git status命令可以让我们时刻掌握仓库当前的状态
git diff这个命令查看修改了什么

HEAD指向的版本就是当前版本，
上一个版本就是HEAD^，上上一个版本就是HEAD^^ 往上100个版本 写成HEAD~100
git reset --hard HEAD^
因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。

穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。

要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本

撤销修改
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交

删除文件
git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；


创建分支 
参看图片
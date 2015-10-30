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
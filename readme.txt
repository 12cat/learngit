3.1415926  535897932  384626433  832795028  841971693  993751058
209749445  923078164  062862089  986280348  253421170  679821480
865132823  066470938  446095505  822317253  594081284  811174502
841027019  385211055  596446229  489549303  819644288  109756659

https://github.com/github/gitignore

http://git.oschina.net/progit/

http://www.liaoxuefeng.com/

http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000


第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：
	ssh-keygen -t rsa -C "youremail@example.com"
第2步：登陆GitHub，打开“Account settings”，“SSH Keys”页面：
然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容

关联远程库：
	git remote add origin git@server-name:path/repo-name.git
	git clone git@github.com:12cat/learngit.git

关联后，推送master分支
	git push -u origin master
	git push origin master

在本地建立远程分支对应的分支
	git checkout -b branch-name origin/branch-name

更新最新远程库
	git pull

建立dev和origin/dev的链接
	git branch --set-upstream dev origin/dev

创建文件夹 mkdir learngit
进入文件夹 cd learngit
显示当前目录 pwd
查看目标文件 cat readme.txt
创建文件 vi/vim readme.txt
	xxx
	按ESC
	:wq!

将目录变成Git可管理的仓库
	git init
	-Initialized empty Git repository in /Users/michael/learngit/.git/

ls －ah 可查看到.git目录

添加文件到暂存区，可添加多个
	git add readme.txt

提价文件到版本库
	git commit -m ‘备注’

查看仓库状态
	git status

查看修改内容
	git diff

查看历史记录
	git log [查看历史记录]
	git log —pretty=oneline [历史记录简略]
	git log --graph --pretty=oneline --abbrev-commit [查看分支图]
	git reflog [历史记录简略，带版本号]

回到上一个版本
	git reset —-hard HEAD^
	git reset —-hard HEAD^^^
	git reset —-hard HEAD~100
	git reset —-hard 280ab3

撤销工作区的修改
	git checkout —- readme.txt

撤销暂存区的修改
	git reset HEAD readme.txt

删除版本库的文件
	git rm test.txt

恢复版本库的文件
	git checkout —- test.txt

创建并切换分支
	git checkout -b dev

创建分支
	git branch dev

切换分支
	git checkout dev

查看当前分支
	git branch

合并分支到当前分支
	git merge dev
	git git merge --no-ff -m 'merge with no-ff' dev

删除分支
	git branch -d dev
	git branch -D dev

保存当前工作现场
	git stash

查看工作现场
	git stash list

回复工作现场
	git stash apply
	git stash apply stash@{0}

删除工作现场
	git stash drop

回复并删除工作现场
	git stash pop

查看远程库信息
	git remote
	git remote -v

创建标签
	git tag v1.0
	git tag v0.9 6224937 

查看标签
	git tag

查看标签信息
	git show v0.9

创建带有说明的标签
	git tag -a v0.1 -m '说明' 3628164
	git tag -s v0.2 -m '说明' 3628164 [私有标签，PGP秘钥]

删除标签
	git tag -d v0.1
	git push origin :refs/tags/v.01 [删除远程标签，先删除本地库]

推送标签到远程
	git push origin v1.0
	git push origin --tags [推送所有标签]


Git显示颜色
	git config --global color.ui true

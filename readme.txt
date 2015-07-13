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

创建文件夹 mkdir learngit
进入文件夹 cd learngit
显示当前目录 pwd
查看目标文件 cat readme.txt
创建文件 vi/vim readme.txt
	xxx
	按ESC
	:wq

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
	git log
	git log —pretty=oneline
	git reflog

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
 

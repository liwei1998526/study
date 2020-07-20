#Git学习

##一、git的作用
 在团队合作中能快速定位问题和解决才是重要的

##二、git基本用法及指令

###一、创建本地仓库用以储存项目文件
1. 在一个空文件夹下用gitbush输入指令`git init`
2. 直接使用gitGUI直接选择所要用作工作区的空文件夹，将其转换为工作区
3. 使用tortoise右击点击git直接在这里创建版本库。

###二、提交文件
要求：所要提交的文件必须在工作区内（及包含.git的文件夹内）

1. 直接用gitbush输入指令`git add 文件名.拓展名`将文件提交到暂存区。后输入指令`git commit -m "日志信息"`将暂存区文件存入本地仓库。
2. 使用sourcetree工具打开本地的github仓库在文件状态中点击暂存并写明日志信息后提交到本地仓库。 
3. 使用tortoiseGit工具选中需要提交的文件或文件夹右击选择tortoiseGit->添加，将文件加入暂存区。后再次点击git提交
->"master"将暂存区内文件提交到本地仓库。

###三、查看日志
1. 使用指令观看
	1. 用gitbush输入指令`git log`查看总的日志信息。
	2. `git log xxx`用于查看指定文件的日志信息。
	3. `git log -p`查看提交所带来的改动。
	4. `git log -p xxx`查看指定文件提交所带来的改动。
2. 使用sourcetree查看：打开sourcetree点击History可以查看日志信息。
3. 使用tortoiseGit：右击选择tortoiseGit->显示日志。

###四、上传至远程仓库
要求：在github网站中建立账户
- 建立远程仓库在网站右上角 **+** 号处选择new repository新建一个远程仓库

- 连接本地仓库与远程仓库方法
	1. 使用编程连接
		1. 使用ssh连接
			 >新建ssh密钥：`ssh-keygen -t rsa`生成密钥
			 >>把带有.pub的公钥加入到github中去。
		
			 >使用命令
			 >>`git remote add 远端名称 
			 >git@github.com:github用户名/远程库名.git`
			 >>`git push -u 远端名称 master(要传入的分支)`
		2. 使用http连接
			 >使用命令
			 >>`git remote add 远端名称 https://github.com/用户名/远程库民.git` 
			 >>`git push -u 远端名称 master（要传入的分支）`
	2. 使用sourcetree软件
		>点击clone 登入本地仓库 ->新的远程仓库，填入所需传入到github远程仓库网址完成添加。点击推送寻则远程远端名称（只需要推送到自己的github上即可）。完成本地仓库上传。

###五、github常用指令
- madir xxx :创建一个新的文件夹

- git init：初始化仓库

- git status：查看仓库状态

- git add 文件名.拓展名：上传至暂存区

- git commit -m "文件名.拓展名"：将暂存区的内容提交到仓库中

- git log xxx：用于查看指定文件的日志信息

- git log -p：查看提交所带来的改动。

- git log -p xxx：查看指定文件提交所带来的改动。

- git diff ：查看工作树，暂存区，最新提交间的差别。

- git diff HEAD ：查看工作树与最新提交的差别。

- git branch ：显示分支一览表

- git branch xxx:创建一个新的分支。

- git branch -d xxx:删除一个分支。

- git branch -D xxx:强制删除一个分支。

- git checkout xxx :切换到xxx分支。

- git checkout - ：切换到上一分支。

- git checkout -b xxx :创建并切换到xxx分支。

- git fetch[remote]：同步远程仓库的所有更新。

- git remote -v :显示所有远程仓库。

- git pull 仓库名 分支名 ：拉取远端分支并与本地分支合并。

- git push 仓库名 分支名 ：上传本地分支到远端。

- git reset --soft:重置提交，将版本退回到某一个commit记录上，所有修改退回暂存区。

- git reset --hard:重置提交，所有修改直接丢弃。

- git reflog:记录所有git操作。

- git revert：还原提交，将某个commit还原并新建一个新的还原commit。

- 开发分支（develop）
	1. 功能分支（feature）
	2. 修bug分支（hotfix或者fix）
	3. 预发布分支（release）

![干的漂亮](http://img2.biaoqingjia.com/biaoqing/201710/05990b97fbf03990ec0b6882acf0ecbf.gif)

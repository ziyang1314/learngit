创建本地的git仓库；

mkdir 文件夹

cd  文件夹

git init

添加你要上擦昏倒本地仓库的代码文件；

git add .  添加全部

或者

git add  filename 添加指定的文件


git commit -m '描述这次提交的内容' 形式将代码提交到本地的代码库；

版本回退：

git log 可以查看commit的提交记录

git log --pretty=online 可以精简log输出内容

SHA1计算 出来的长的数字字母串就是每次提交形成的版本号也叫 commit—id

git reset --hard HEAD^ 可以将commit后的代码回退到上一个版本

^^ 可以回退到上上一个版本 但是这样的都不好

git reset --head  commit—id  这样可以回退到指定的版本

git reflog 可以查看log输出，这样就可以避免代码回退之后找不到之前最新的commit—id了

工作区->暂存区->当前的分支；

git add    工作区-->暂存区

git commit 暂存区-->当前分支

git add 之后git commit 也完成之后，工作区和暂存区应该都是干净的；

可以通过 git status 进行查看当前的提交状况

注意：git 管理的是修改，而不是文件，第一次修改提交，add ，第二次修改，add ,commit，那么版本库的是第二次的提交

可以通过 git diff  HEAD -- filename 来查看工作区和代码库最新代码的区别；


工作区修改撤销；

通过命令 git checkout -- filename 来完成

分两种情况：

1.暂存区无修改；

  撤销的只是工作区的修改，到和版本库一致；

2.暂存区有修改，工作区无改动，或者有改动

  撤销的都是工作区的修改，代码和暂存区保持一致；

文件删除操作

1.直接删除

2.命令行的方式 rm filename

无论哪种方式，git status  都可以查看到文件的状态

确定要进行删除的话，就用git rm filename 然后 commit 完成删除仓库中的文件操作

关联远程库；

github创建仓库

之后push an existing repository from the command line

git remote add origin https://github.com/ziyang1314/learngit.git

然后将本地的内容推送上去；

git push -u origin master

以上是关联本地仓库创建新仓库；

也可以远程克隆；

git clone 仓库地址就可以了

分支管理：

创建分支和合并分支；

创建分支： git checkout -b 分支名称 这里是创建并切换分支

相当于

git branch dev  然后 git checkout dev

单独的git branch 可以查看分支列表 以及*标注的当前分支

内容修改之后切换到master

然后git merge 要合并的分支

这种方式的合并是fast forward 模式；通常不会这样；

删除分支

git branch -d 分支名称分支名

最新的创建和切换分支的方式：

git switch -c <name>  我的git好像不太支持




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

注意：git 管理的是修改，而不是文件，第一次修改提交，add ，第二次修改，commit，那么版本库的是第一次的提交

可以通过 git diff  HEAD -- filename 来查看工作区和代码库最新代码的区别；

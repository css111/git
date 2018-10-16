git stash:可以把当前工作现场储藏起来；

git stash list:git把stash存放在某个地方；

git stash apply:恢复先前储藏起来的工作现场，但是恢复后，stash内容并不删除，需要用git stash drop来删除；

git stash drop：恢复的同时把stash内容也删除了；

git branch -d 分支名：删除分支；

git branch -D 分支名：强行删除分支；

git checkout -b 新分支名：创建并切换到新分支；

git checkout 分支名：切换分支；

git branch:查看所用的分支；

git merge --no-ff -m '注释' 分支名：分支合并；

git remote:查看远程库的信息，默认名称为origin;

git remote -v:显示更详细的信息，显示可以抓取和推送的origin的地址，如果没有推送权限，就看不到push地州；

git push origin 本地分支名：就是把该分支上的所有本地推送到远程库，这样git就会把该分支推送到远程库对应的远程分支上；

git remote add origin git@github.com:github库地址：git与github上的仓库进行关联；

git push -u origin master：第一次推送master时，加上-u参数，git不仅会把master的内容推送到远程的新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或拉取时就可以简化命令；

git checkout -- 文件名：把文件在工作区的修改全部撤销，让文件回到最近一次git commit或git add时的状态

git reset Head 文件名：可以把暂存区的修改回退到工作区。

git branch --set-upstream-to=origin/分支名 分支名：建立本地分支与远程分支的链接（如果git pull之后提示no tracking information,则用此命令）；

git pull：把最新的提交从远程抓下来（当git push origin 分支名：不成功时）；

git clone git@github.com:github库地址：克隆github上的仓库到本地（只克隆master分支）；

git checkout -b 分支名 origin/分支名：把远程仓库的分支创建到本地来；

git tag 标签名：打一个新标签（默认标签是打在最新提交的commit上）；
 
git tag 标签名 commit id值：在commit id值上打标签；
git tag:查看标签；
git show 标签名：查看标签信息；

git tag -a 标签名 -m ‘注释’：创建带有说明的标签；

git tag -d 标签名：删除标签；

git push origin 标签名：推送标签到远程；

git push origin --tags:一次性推送全部尚未推送到远程的本地标签；

git tag -d 标签名:先从本地删除，再git push origin :refs/tags/标签名：删除远程标签；  

git init:通过git init命令把这个目录变成Git可以管理的仓库：

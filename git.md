##关键名词 
1. 工作区(Working area)：就是咱们刚才创建的mygit文件夹。
2. 暂存区(Staging area)：对文件操作(也就是需要提交的文件修改)的地方就叫暂存区。--注意：这里的修改包括对文件的增删改。
3. 版本库(Repository)：就是你所看到的的那个隐藏的“.git”目录，它就是咱们的版本(仓)库。
##常用命令
1. git config --global user.name "your name"     配置用户名
2. git config --global user.email "email@example.com" 配置用户邮箱
3. mkdir mygit && cd mygit && git init 初始化空的git仓库
4. git status && git add && git commit 增加文件到暂存区
5. git diff 查看差异文件
6. git log 查看提交记录
7. git reflog 查看你每次提交的记录 包含commit ID
8. git reset --hard HEAD^ && git reset --hard commitId回退到原来的版本
9. git checkout -- file 丢弃工作区的修改
10. git reset HEAD file 已经add到暂存区的文件返回到工作区
11. git rm 1.txt && git commit 删除版本库中得文件
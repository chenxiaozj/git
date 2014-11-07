##关键名词 
* 工作区(Working area)：就是咱们刚才创建的mygit文件夹。
* 暂存区(Staging area)：对文件操作(也就是需要提交的文件修改)的地方就叫暂存区。--注意：这里的修改包括对文件的增删改。
* 版本库(Repository)：就是你所看到的的那个隐藏的“.git”目录，它就是咱们的版本(仓)库。

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
12. git remote add origin git@github.com:chenxiao/git.git && git push -u origin master
13. git clone git@github.com:chenxiao/git.git 会多出一个目录。
14. git branch -a 查看所有分支
15. git branch develop 创建develop分支
16. git checkout develop 切换到develop分支
17. git merge develop 合并分支 (正常开发的时候merge需要权限，不能随便merge)
18. git branch -d develop 删除分支，也可以使用-D强制删除
19. git checkout -b develop 创建分支并切换到develop分支
20. git merge --no-ff -m "no off" develop 使用--no-ff参数(表示禁用“Fast forward”)
21. git log --graph --pretty=oneline --abbrev-commit 查看分支历史
22. git stash 保存改动
23. git stash list 显示stash列表
24. git stash apply stash@{0}恢复现场,stash@{0}可以省略表示恢复第一个
25. git stash drop stash@{0} 删除保存的改动
26. git stash pop 恢复并删除stash
27. git tag v0.1 打标 （根据commit ID）
28. git tag 查看tag
29. git tag v0.3 1a7db230cbeacde746d8eb58cf882ac34c36636e 补充打标
30. git tag -d v0.1 删除tag
31. git config --global  alias.st status设置别名
32. git log --author="xxx@xxx.com" 查询某人提交的记录
33. git fetch 从远程获取最新版本到本地，不会自动merge
34. git pull 相当于是从远程获取最新版本并merge到本地
35. git rebase develop 给现有分支打补丁，跟merge不一样
36. git rebase -continue 修复完冲突之后使用
37. git rebase --abort 放弃rebase过程
38. git rebase --skip 直接用test分支取代当前分支代码
39. git cherry-pick commitId把另一个本地分支的commit修改应用到当前分支


相关网站：http://git-scm.com/docs

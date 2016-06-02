初始化一个Git仓库: 	git init.
***
添加文件到Git仓库:

    1.git add <file>  
    2.git commit(后缀 -m 加相应提交描述).
***
查看工作区和暂存区状态:  `git status`.
***
对比修改文件内容:  `git diff(后缀 <file> 查看对应文件)`.
***
查看提交历史:  `git log`.
***
查看命令历史:  `git reflog`.
***
回退到版本库的某一历史(回退后暂存区和工作区都将clean):  
* `git reset --hard HEAD^  一个"^"代表回退一个版本`.
* `git reset --hard HEAD~100  回退100个版本`.
* `git reset --hard commitId  回退到commitId代表的版本`.

***
改乱了工作区某个文件的内容，想直接丢弃工作区的修改:  `git checkout -- <file>`.
***
改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改:

    1.git reset HEAD <file>.
    2.git reset checkout -- <file>.
***
删除一个文件:  `git rm`.
***
创建SSH Key:  `ssh -t rsa -C "youremail@example.com"`.
***
关联github远程库:  `git add remote <remote-name> <远程库地址(git@github.com:3Liang/learngit.git)>`
***
第一次推送本地到远程库:  `git push -u <remote-name> master,master代表分支<master>`.  
非第一次推送:  `git push <remote-name> master`.
***
克隆远程库:  `git clone <远程库地址(git@github.com:3Liang/learngit.git)>`
***
查看分支:  `git branch`.
***
创建分支:  `git branch <branch-name>`.
***
切换分支:  `git checkout <branch-name>`.
***
创建+切换分支:  `git checkout -b <branch-name>`.
***
采用快速模式(fast forward)合并指定分支到当前分支:  `git merge <branch-name>`.
***
删除分支:  `git branch -d <branch-name>`.
***
查看分支合并图:  `git log -graph`.
***
采用普通模式(--no-ff)合并指定分支到当前分支(会有合并提交历史):  `git merge --no-ff -m <commit-description> <branch-name>`.
***
创建stash:  `git stash`.
***
查看stash集合:  `git stash list`.
***
恢复某个指定stash:  `git stash applay`.
***
删除stash:  `git stash drop`.
***
恢复并删除stash:  `git stash pop`.
***
丢弃一个没有被合并过的分支:  `git branch -D <branch-name>`.
***
查看远程库信息:  `git remote -v`.
***
推送分支:  `git push <remote-name> <branch-name>`.
***
建立本地分支和远程分支的关联:  `git branch --set-upstream-to <remote-name>/<branch-name>`.
***
新建一个轻量标签:  `git tag <tag-name> (可加commitId指定需要打标签的历史版本)`.
***
创建带注释标签:  `git tag -a <tag-name> -m <description> (可加commitId指定需要打标签的历史版本)`.
***
创建GPG签名标签:  `git tag -s <tag-name> -m <description> (可加commitId指定需要打标签的历史版本)`.
***
查看所有标签:  `git tag (后缀标签名可指定查看该标签)`.
***
查看标签信息:  `git show tag`.
***
删除标签:  `git tag -d <tag-name>`.
***
推送指定标签:  `git push <remote-name> <tag-name>`.
***
推送所有标签:  `git push <remote-name> --tags`.
***
删除远程库标签:  
* `git tag -d <tag-name>`.
* `git push <remote-name> :refs/tags/<tag-name>`.

***
查看文件因.gitignore不能提交原因:  `git check-ignore -v <file>`.
***
配置别名:  
* `git config --global alias.<abbreviated-name> <replaced-character>  配置全局的别名,存放在用户主目录下的.gitconfig里面`.
* `git config --local alias.<abbreviated-name> <replaced-character>  配置当前repository的别名，存放在工作区的.git/config里面`.

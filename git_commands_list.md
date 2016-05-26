初始化一个Git仓库: 	git init.

添加文件到Git仓库:

    1.git add <file>  
    2.git commit(后缀 -m 加相应提交描述).

查看工作区和暂存区状态:  `git status`.

对比修改文件内容:  `git diff(后缀 <file> 查看对应文件)`.

查看提交历史: `git log`.

查看命令历史: `git reflog`.

回退到版本库的某一历史(回退后暂存区和工作区都将clean):  
* `git reset --hard HEAD^  一个"^"代表回退一个版本`.
* `git reset --hard HEAD~100  回退100个版本`.
* `git reset --hard commitId  回退到commitId代表的版本`.


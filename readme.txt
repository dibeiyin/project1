1.通过git init命令把这个目录变成Git可以管理的仓库
2.用命令git add告诉Git，把文件添加到仓库,可添加多个文件
3.用命令git commit [-m "说明"] 告诉Git，把文件提交到仓库

4.git status命令可以让我们时刻掌握仓库当前的状态
5.如果git status告诉你有文件被修改过，用git diff可以查看修改内容

6.Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id
7.穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本
8.要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本
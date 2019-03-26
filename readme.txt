1. 通过git init命令把这个目录变成Git可以管理的仓库
  用命令git add告诉Git，把文件添加到仓库,可添加多个文件
  用命令git commit [-m "说明"] 告诉Git，把文件提交到仓库

2.  git status命令可以让我们时刻掌握仓库当前的状态
  如果git status告诉你有文件被修改过，用git diff可以查看修改内容

3.  Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id
  穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本
  要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本

4. 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file
    场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第       二步按场景1操作
    命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，git checkout --file只能恢复文件到最新版本，    你会丢失最近一次提交后你修改的内容)

5.要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git
  关联后，使用命令git push -u origin master第一次推送master分支的所有内容
  此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改

6.要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆. Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快

7.Git鼓励大量使用分支：
查看分支：git branch
创建分支：git branch <name>
切换分支：git checkout <name>
创建+切换分支：git checkout -b <name>
合并某分支到当前分支：git merge <name>
删除分支：git branch -d <name>
Creating a new branch is quick and simple.

8.当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。
解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交。
用git log --graph命令可以看到分支合并图。
合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并

9.修复bug时，我们会通过创建新的bug分支进行修复，然后合并，最后删除；
当手头工作没有完成时，先把工作现场git stash一下，然后去修复bug，修复后，再git stash pop，回到工作现场
  开发一个新feature，最好新建一个分支；
如果要丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除。

10.多人协作
查看远程库信息，使用git remote -v；
本地新建的分支如果不推送到远程，对其他人就是不可见的；
从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。

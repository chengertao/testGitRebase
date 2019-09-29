# testGitRebase
测试rebase与merge区别 ，以及git cherry-pick 合并

------------------------------------------
git merge的使用非常简单


1.拉取你要合并的远程分支到本地 ---- dev分支
2.在dev分支上直接合并（git merge 分支名）你的本地开发分支（local分支）
如果 合并出现冲突则解决冲突 
    >>>HEAD  冲突代码
    ====以下是你本次提交代码
3.最后git push 到远程分支即可

-------------------------------------------
git rebase 合并分支


1.拉取你要合并的远程分支到本地 ---- dev分支
2.在dev分支上直接合并（git rebase 分支名）你的本地开发分支（local分支）
  如果有冲突则解决冲突
  解决完以后执行git rebase continue 即可
  
  如果想要把多个commit 合并  可以执行git rebase HEAD~3


3.最后git push 到远程分支即可

-------------------------------------------
git cherry-pick  一个个筛选合并

1.拉取你要合并的远程分支到本地 ---- dev分支
2.在你本地开发分支（local）使用git log 查看提交
3.打开新窗口  切换到dev分支  使用git cherry-pick 将每一次提交 添加
4.使用git push 提交即可







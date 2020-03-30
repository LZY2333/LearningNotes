
# 工作区>>>>暂存区>>>>仓库

> Git管理的文件分为：工作区，版本库，版本库又分为暂存区stage和暂存区分支master(仓库)

git add 把文件从工作区>>>>暂存区，git commit把文件从暂存区>>>>仓库，

git diff 查看工作区和暂存区差异，

git diff --cached 查看暂存区和仓库差异，

git diff HEAD 查看工作区和仓库的差异，

git add的反向命令git checkout，撤销工作区修改，即把暂存区最新版本转移到工作区，

git commit的反向命令git reset HEAD，就是把仓库最新版本转移到暂存区。


# 版本回退

### git restore -- readme

 (原git checkout -- readme.txt) 
 丢弃工作区的修改 回到最近一次git commit或git add时的状态。

### git restore --staged readme

 (原git reset HEAD readme.txt)
 丢弃暂存区的修改 回到上一次git commit

### git reset --hard commit_id

 丢弃仓库的修改 回到任意版本
 配合git log 查看提交历史，确认回退之前的版本
 配合git reflog 查看命令历史，确认回退未来的版本(已回退过老版本)

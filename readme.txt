设置仓库的用户名和Email
git  config --global user.name 'jjc314'
git config --global 'jjc314@126.com'
初始化文件夹为一个仓库
git init 
添加文件到暂存区
git add filename
提交暂存区文件到分支上
git commit -m '备注说明'
查看仓库状态
git status
查看具体文件修改的内容
git diff  filename 
查看提交版本记录
git log
git log --pretty=oneline
记录每一次命令
git reflog
回退到上一个版本
git reset --hard HEAD^
回退到上上个版本
git reset --hard HEAD^^
回退到相应的版本号 git log 可以查看版本号
git reset --hard 对应的版本号
对比暂存区根工作区的区别
git diff HEAD -- readme.txt
丢掉工作区的修改
git checkout -- readme.txt
撤销暂存区的修改
git reset HEAD readme.txt
删除版本中的文件
git rm filename
git commit 
创建本地计算机的公钥跟私钥
ssh-keygen -t rsa -C 'jjc314@126.com'
会在当前用户的家目录中生成.ssh的目录
id_rsa 是私钥  id_rsa.pub是公钥
将本地仓库与远程仓库进行关联
git remote add origin https://github.com/jjc314/learngit
推送本地仓库的master分支到远程仓库的master上
git push -u origin master
之后再提交
git push origin master
创建新的分支 -b 参数表示创建并切换
git switch  -c dev
git checkout -b '分支name'
查看当前分支
git branch
切换分支
git checkout main
合并分支
git merge dev
删除分支
git branch -d dev
强制删除没有合并的分支
git branch -D feature-vulcan
合并冲突解决冲突之后 查看合并情况
git log --graph
git log --graph --pretty=oneline --abbrev-commit
禁用fast  forward
git merge --no-ff -m "merge with no-ff" dev 
启用临时工作区
git stash
查看临时工作区
git stash list
恢复工作区两种方式
git stash apply  恢复 但是不删除stash
git stash drop 来删除stash
直接恢复并删除stash
git stash pop
可以多次stash 使用git stash list查看
使用命令恢复指定的stash
git stash apply stash@{0}
复制一个特定的提交到当前分支
git cherry-pick  <commit>






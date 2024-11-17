<!-- 初始化仓库： -->
git init           创建仓库

<!-- 配置： -->
git config         查看和设置配置选项。

<!-- 添加文件： -->
git add <file>     添加指定文件到暂存区。
git add .          添加当前目录的所有文件到暂存区。

<!-- 提交更改： -->
git commit -m "message"

<!-- 显示当前的工作区状态 -->
git status：

<!-- 查看提交日志： -->
git log                 显示提交日志。
git log --oneline       以简化的方式显示提交日志。

<!-- 查看所有操作日志  -->
git reflog

<!-- 撤销操作： -->
git reset <file>         将文件从暂存区撤回到工作区。
git reset --hard         将暂存区和工作区都重置到最后一次提交的状态。
git revert <commit>      撤销某次提交。

<!-- 推送到仓库 -->
git push
git push -u origin1 master        会覆盖原来的默认仓库
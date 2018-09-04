# gitTest
学习使用git与github

建立一个库：
  1.drag
  2.git clone [url]
  3.设置贡献者：
     1).name:git config --global user.name "wangjing1125"  
     2).email:git config --global user.email "35488****@qq.com"
  4.查看贡献者：
     1).name:git config --global user.name 
     2).email:git config --global user.email
  5.查看所有配置项：
    git config --list
    
 git命令：
   1.查看当前工作区与暂存区的状态：git status
   2.将本地工作区改动的内容添加到暂存区:1).提交单个文件：git add [文件名]    2).提交全部文件：git add .
   3.将暂存区改动的内容提交到版本库：git commit -m "change one" (-m后面的内容为提交时的注释)
   4.直接将工作区的修改提交到版本库：git commit -am "" (-a是add的简写，这样就省略了add那一步)
   5.查看谁在什么时候修改了什么内容：git log
   差异对比：
   1.工作区与暂存区差异对比：git diff
   2.暂存区与版本库差异对比：git diff --cached(--staged)
   3.工作区与版本库差异对比：git diff master
   撤销：
   1.把提交到暂存区的更新从暂存区撤销回工作区：git reset HEAD drag.js
   2.把工作区最新改动的内容还原到上次提交到暂存区或者版本区的状态：git checkout --drag.js
   3.把上一次提交到版本区的内容撤回与其他内容重新一起提交：git commit -m "change3 drag.js and demo1.html" --amend
   删除：
      1.在工作区删除了一个文件，可以用此命令把对应的暂存区的这个文件删除：git rm drag.js
      2.强制的把工作区跟暂存区的某个文件一起删除：git rm -f drag.js
      3.只删除暂存区的某个文件，工作区中该文件不会变：git rm --cached drag.js
    恢复：
      1.恢复被删除的单个文件：git checkout id drag.js
      2.恢复被删除的某个版本：git reset --hard id
      3.恢复到前一个版本：git reset --hard HEAD^
        恢复到前两个版本：git reset --hard HEAD~2
      4.显示最近几次的操作:git reflog
      5.恢复到前一个版本后再恢复回现在的状态：git reset --hard id (从git relog显示中查看对应的id)
    上传到github:
      1.查看当前的远程仓库：git remote  (git remote -v)    会显示出该远程仓库的名称origin
      2.将本地的更新上传到远程仓库github:git push origin master
    从远程仓库更新到本地文件：
      1.从远程仓库下载新分支与数据：git fetch origin
      2.查看本地与远程的冲突：git diff master origin/master
      3.从远端仓库提取数据并尝试合并到当前分支：git merge origin/master
      4.直接从远端仓库提取数据并合并到当前分支：git pull
    git分支：
      1.查看所有分支：git branch
      2.新建分支：git branch new1
      3.切换到new1分支：git checkout new1
      4.直接新建分支并切换到新建的分支：git checkout -b new2
   

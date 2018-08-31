# gitTest
学习使用git与github

建立一个库：
  1.drag
  2.git clone [url]
  3.设置贡献者：
     1).name:git config --global user.name "wangjing1125"  
     2).email:git config --global user.email "354884012@qq.com"
  4.查看贡献者：
     1).name:git config --global user.name 
     2).email:git config --global user.email
  5.查看所有配置项：
    git config --list
    
 git命令：
   1.查看当前工作区与暂存区的状态：git status
   2.将本地工作区改动的内容添加到暂存区:1).提交单个文件：git add [文件名]    2).提交全部文件：git add .
   3.将暂存区改动的内容提交到版本库：git commit -m "change one" (-m后面的内容为提交时的注释)
   4.直接将工作区的修改提交到版本库：git commit -a -m "" (-a是add的简写，这样就省略了add那一步)
   5.查看谁在什么时候修改了什么内容：git log
   6.工作区与暂存区差异对比：git diff
   7.暂存区与版本库差异对比：git diff --cached(--staged)
   8.工作区与版本库差异对比：git diff master
   

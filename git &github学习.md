## git &github学习

### 	创建版本库

+ mkdir创建空目录

+ cd进入空目录

+ pwd显示当前目录

+ 写文件

+ git init  初始化，让git 管理当前文件夹

+ git status  检测当前目录下的文件状态

+ 个人信息配置：用户名、邮箱（最开始的时候执行一次即可）

+ 三种状态的变化
  + 红色：新增的文件或修改了原来的老文件   git add 文件名/.
  + 绿色：git 已经管理起来   git commit -m'描述信息'
  + 生成版本

+ git log查看版本记录

  | 工作区                        | 暂存区                                  | 版本库                      |
  | ----------------------------- | --------------------------------------- | --------------------------- |
  | 已管      新文件/修改过的文件 | git add .可以将工作区的文件提交到暂存区 | git commit -m''提交到版本库 |

  ###回滚至之前版本

  + git log

  + git reset --hard 版本号（git reset --hard HARD^回退到上一版本）

    

  ### 回滚至之后版本

  + git reflog
  + git reset --hard 版本号

  ### 撤销修改

  git checkout -- <file>

  + 若文件自修改后还没有被存放到暂存区，撤销修改就回到和版本库一模一样的状态；
  + 若文件已经添加到暂存区后，又做了修改，撤销修改就回到添加到暂存区后的状态。

  ###删除修改

  git rm 用于删除一个文件

  ### 关联远程仓库与本地仓库

  ```
  git remote add origin git@github.com:<user's name>/learngit.git
  ```

  远程库的名字默认叫origin

  提交代码：git push -u origin master(把本地库的所有内容推送到远程库上)

  只要做了提交，就可以通过git push origin master把本地master分支的最新修改推送至Github

  + 删除远程库与本地的绑定关系：
    + git remote -v
    + git remote rm <name>

  ### 从远程库克隆

  git clone git@github.com:<user's name>/gitskills.git

  ### 拉取远程代码

  git pull origin master(将远程主机的master分支最新内容拉下来后与当前本地分支直接合并）

  git pull <远程主机名><远程分支名>：<本地分支名>

  ### 分支

  查看分支：git branch

  创建分支：git branch 分支名称

  切换分支：git checkout 分支名称

  分支合并：git merge 要合并的分支（注意：切换分支再合并）

  ​					可能产生冲突，需找到冲突的文件手动修改

  删除分支：git branch -d 分支名称

  ### 工作流

  

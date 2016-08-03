## 时光机穿梭
- `git status`: 让我们时刻掌握仓库当前的状态，上面的命令告诉我们，readme.txt被修改过了，但还没有准备提交的修改。
- `git diff`: 查看difference
- `git add`: 提交修改
- `git add .` 提交全部修改
- `git commit`: 提交全部文件

### 版本退回
- `git log`: 显示从最近到最远的提交日志，
- `git log --pretty=oneline`: 以一行显示提交日志
- `git reset --hard HEAD^`: 退回上一个版本
- `git reset --hard HEAD^^`: 退回上上个版本
- `git reset --hard <提交编号>`: 退回到提交编号所代表的版本
- 'git reflog': 显示每一次提交操作

### 工作区和暂缓区
![图片 | left | 458*234](http://www.liaoxuefeng.com/files/attachments/001384907702917346729e9afbf4127b6dfbae9207af016000/0)

### 撤销修改
- `git checkout -- file`: 把`file`文件在**工作区**的修改全部撤销，这里有两种情况：
  >一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

  >一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
- `git reset HEAD file`: 把暂存区的修改撤销掉（unstage），重新放回工作区

### 删除文件
- `rm test.txt`: 终端指令，删除文件
- `git rm`: 删掉版本库中的文件，之后需要提交

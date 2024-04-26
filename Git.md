# Git

## 配置信息

###### 查看本地仓库配置

    git config --local --list

###### 查看全局配置

    git config --list

###### 设置用户名和邮箱

    git config --global user.name "username"

    git config --global user.email  useremail@qq.com

###### 查看用户名和邮箱

    git config user.name

    git config user.email

## git status

    git status

    git status -s

## git add

**添加一个或多个文件到暂存区：**

    git add [file1] [file2]

**添加指定目录到暂存区，包括子目录：**

    git add [dir]

**添加当前目录下的所有文件到暂存区：**

    git add .

## git commit

**提交暂存区到本地仓库中:**

    git commit -m [message]

**-a 参数设置修改文件后不需要执行 git add 命令，直接来提交**

    git commit -a

## git remote

**列出当前仓库中已配置的远程仓库。**

    git remote

**列出当前仓库中已配置的远程仓库,并显示它们的 URL。**

    git remote -v

**添加一个新的远程仓库。指定一个远程仓库的名称和 URL，将其添加到当前仓库中。**

    git remote add <remote_name> <remote_url>

**将已配置的远程仓库重命名。**

    git remote rename <old_name> <new_name>

**从当前仓库中删除指定的远程仓库。**

    git remote remove <remote_name>

**修改指定远程仓库的 URL。**

    git remote set-url <remote_name> <new_url>

**显示指定远程仓库的详细信息，包括 URL 和跟踪分支。**

    git remote show <remote_name>

## git push

    git push <远程主机名> <本地分支名>:<远程分支名>

**如果本地分支名与远程分支名相同，则可以省略冒号**

    git push <远程主机名> <本地分支名>

**实例**

    git push origin master

## git pull

**git pull 命令用于从远程获取代码并合并本地的版本。**

    git pull <远程主机名> <远程分支名>:<本地分支名>

**实例**

    git pull

    git pull origin

## git clone

**git clone 是一个用于克隆（clone）远程 Git 仓库到本地的命令。**

    git clone [url]

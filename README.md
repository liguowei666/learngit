# Git基本操作
## 1.状态查看
* 查看工作区、暂存区状态

  ```
  git status
  ```

## 2.添加
* 将工作区的“新建/修改”添加到暂存区

  ```
  git add $file_name 
  ```

## 3.提交
* 将暂存区的内容提交到本地库

  ```
  git commit -m "commit message" $file_name
  ```

## 4.查看历史记录
* 查看版本历史记录(方式一)

  ```
  git log
  ```
* 查看版本历史记录(方式二)

  ```
  git log --pretty=oneline
  ```
* 查看版本历史记录(方式一)

  ```
  git log --oneline
  ```
* 查看版本历史记录(方式一)

  ```
  git reflog
  ```

# 本地库与远程库建立连接

- 初始化本地库
  ```
  git init
  ```

- 假如要上传一个文本文件git.txt，将git.txt提交到暂存区
  ```
  git add git.txt
  ```

- 把暂存区的内容(git.txt文件)提交到本地库
  ```
  git commit -m "my first commit" git.txt
  ```

- 将本地库推送到远程库
  ```
  git push origin master
  ```
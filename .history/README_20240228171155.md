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

- 讲本地和远程仓库进行关联
  ```
  git remote add origin $远程仓库网址
  ```

- 将本地库推送到远程库
  ```
  git push origin master
  ```

# git push免密码
## 使用ssh协议
- 生成密钥对：
  ```
  ssh-keygen -t ras -C $your_email
  ```
- 将`~/.ssh`下`id_rsa.pub`中的内容复制到github setting里的ssh key 中
- 如果没有克隆仓库，配置ssh远程项目地址
  ```
  git remote add origin git@github.com:yourusername/yourrepositoryname.git
  ```
- 如果已经使用https协议克隆, 那么按照如下方法更改协议：
  ```
  git remote set-url origin git@github.com:yourusername/yourrepositoryname.git
  ```
title: git 使用指南
author: daidai
date: 2018-07-15 11:30:50
tags:
---
#### 创建账号

创建一个Github或者Gitee账号

#### 本地安装Git

前往 Git 根据操作系统下载Git并安装到本地

#### ssh密钥

##### 本地生成秘钥

右击桌面打开你的git bash,第一次使用Git时,需要先生成ssh

```
ssh-keygen -t rsa -C "your_email@youremail.com"
```

生成的秘钥一般在你操作系统用户下的.ssh目录中

##### 告诉本地系统

将密钥告诉本地系统

```
ssh-add ~/.ssh/id_rsa
```

（此处如果出现Could not open a connection to your authentication agent. 则先执行 ``ssh-agent bash``）

##### 查看生成的公钥

```
cat ~/.ssh/id_rsa.pub
```

##### 上传公钥

- 复制该公钥粘贴到你的Github或者Gitee的SSH公钥页面
- 使用SSH公钥可以让你在你的电脑和码云通讯的时候使用安全连接（Git的Remote要使用SSH地址）

#### 配置User

打开 git bash 需要配置:

```
git config --global user.name "Your Name"
git config --global user.email"email@example.com"
```

#### 初始化本地Git仓库

```
git init
```

这条命令执行完毕后会多出一个.git文件夹

#### 添加变更文件

```
git add .
```

#### 提交文件

```
git commmit -am "message"
```

#### 添加远程地址

```
git remote add origin git@github.com/你的github用户名/仓库名.git
```

可能出现的错误

如果出现 fatal: remote origin already exists. 则执行 ``git remote rm origin``

首次提交

第一次提交可能会出现如下错误``error: failed to push some refs to 'https://gitee.com/tomFat/interview.git'``
所以需要在提交前执行``git pull``

#### 合并两个版本库

```
git pull origin master --allow-unrelated-histories
```

#### 向Github或Gitee推送

```
git push -u origin master
```

#### git命令速查
![你想输入的替代文字](git-使用指南/git-速查表.png)
---
title: Git的使用流程
---
### Git的使用流程
#### 1.安装Git
https://git-scm.com/
#### 2.配置Git

```
git config --global user.name "Your Name"  
git config --global user.email "your.email@example.com"
```
#### 3.创建仓库
###### 有两种方式可以开始使用 Git：
1）创建一个新的仓库：
###### 如果你正在开始一个新的项目，你可以通过 Git 初始化一个新的仓库
`git init`
2）克隆一个已存在的仓库：
###### 如果你想要为已经存在的项目贡献代码，或者查看其历史记录，你可以克隆这个仓库到你的本地计算机
`git clone https://github.com/user/repo.git`
#### 4.添加文件到仓库
###### 将你的项目文件添加到 Git 仓库中。首先，你需要将文件添加到暂存区（Staging Area），然后才能提交到仓库中。

```
git add .  # 添加所有修改过的文件到暂存区  
# 或者  
git add filename # 添加指定文件到暂存区
```
#### 5.提交文件
###### 将暂存区的文件提交到仓库中，并附上提交信息。
`git commit -m "Initial commit"`
#### 6.查看提交历史
###### 你可以查看仓库的提交历史，来回顾项目的变更记录。
`git log`
#### 7.标签
###### 为特定的提交打上标签，以便于版本管理和发布。

```
git tag -a v1.0 -m "Version 1.0"  
git push origin --tags
```



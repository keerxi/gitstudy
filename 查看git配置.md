### 查看git配置

```
git config -l

查看系统配置
git config --system --list
配置文件在安装目录下的 etc\gitconfig

查看本地配置
git config --global --list
配置文件在C\用户名\.gitconfig
```



### 清屏

```
clear
```



### 设置用户名和email

```
git config --global user.name "nyx-keerxi"
git config --global user.email "2468846563@qq.com"
```



### 查看提交日志

```
git log
```





## GIT核心

### 1. git本地有三个工作区域和一个远程仓库

- *工作目录 (项目目录)
- 暂存区 (只是一些文件, 项目目录的.git)
- 资源库 (.git 中 HEAD指向的)
- *远程仓库 (github, gitee)

### 2. 基本操作

```
先通过git add files 将本地(工作目录)添加到 暂存区
然后用git commit 提交到本地仓库
再用 git push 提交到远程仓库

用git pull 从远程仓库将代码拉到本地仓库
再用git reset 从本地仓库拉到暂存区
再用git checkout 从暂存区拉到工作目录
```



## 工作流程

### 1. 第一种初始化git仓库

```
在空文件夹 git init
之后会多一个 .git隐藏文件
```

### 2. 第二种初始化git仓库

```
git clone [url]
从远程仓库拉到本地

git clone --depth=1 [url]
只克隆最近一次的提交, 体积更小
```



### 3. git文件状态

```
untracked状态: 未跟踪, 在文件夹中不在git库
git add . 将所有文件添加到暂存区 状态变为 staged

unmodify状态: 文件未修改
git rm 移出版本库, 变为untracked状态

modified状态: 文件已经修改了
通过git add 进入staged状态
通过git checkout 丢弃修改, 变为 unmodify状态
git checkout从库中取出文件, 覆盖当前修改

staged状态: 
使用git commit 提交到库中

```



### 4. 工作流程

```
1. git init
2. git status查看状态, 没有git add的时候是未被跟踪的, 红色的, git add后是绿色的
3. git add . 将所有文件添加到暂存区
4. git commit -m 提交暂存区的内容到本地仓库

前端node_modules不用提交, 具体需要gitignore文件配置
```



## 远程仓库

### 1. SSH公钥

```
到C盘用户目录下.ssh文件夹
生成公钥
ssh-keygen -t 加密算法rsa
会生成对应的两个文件
pub是公钥
不带pub的是私钥

将公钥添加到远程仓库
```

### 2. clone到本地
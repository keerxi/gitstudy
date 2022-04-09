## git 试错

### 1.  git pull ssh / url.

```js
要先git init 初始化个仓库, 有 .get文件夹
否则会报错

这个是在有 .get文件夹 之后将远程仓库其余文件拉下来
将远程主机的最新内容拉下来后直接合并
即：git pull = git fetch + git merge，这样可能会产生冲突
```



### 2. git clone ssh / url

```js
这个是直接拉一个项目下来
可以在没有 .git文件夹 情况下

git clone 指定分支
    git clone -b anan http://xxxxxx/service
		其中 anan 为分支名  根据实际情况更改
git clone 不指定分支
		git clone  http://xxxxxx/service
```



### 3. clone 和 pull

```
有权限无文件
pull clone
有权限有文件
pull
无权限
clone
```



### 4. 查看修改状态

- git status



### 5. 执行commit的文件

- git add



### 6. 提交到本地仓库

- git commit -m "message"



### 7. 查看提交日志

- git log



### 8. 回滚提交

- git reset --hard id



### 9. git push ssh / url
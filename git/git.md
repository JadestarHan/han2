## 合并分支
```
git使用步骤大概是这样的

add->commit->fetch->pull->push-添加代码->提交代码->抓取代码->拉取代码->推送代码

git代码合并使用步骤思路
1 git fetch origin 同步所有线上分支
2.git pull origin home --allow-unrelated-history
    在当前分支下pull需要合并到的那个分支,后面参数是干掉报错的
     refusing to merge unrelated histories
3.git status 查看差异化
    git add *
    git commit -m""
4. git checkout home--合并到哪的那个总分支
5.git merge 当前分支
6. git push origin home
git fetch origin # 同步所有线上分支
```

## 本地:远程
`git push origin master:home`

## 合并分支2

```
add->commit->fetch->pull->push
add->commit->fetch->pull->push

1.	git fetch origin 
2. 	git pull origin home --allow-unrelated-histories
3.	git status 
	git add *
	git add commit
4. 	git checkout home
5. 	git merge git
6.	git push origin home
```



## git撤销操作[网址](https://www.cnblogs.com/liangzhixiaolaohu/p/14977650.html)







## 合并分支

- `git fetch origin` # 同步所有线上分支
- `git branch`# 查看有多少本地分支
- fatal: refusing to merge unrelated histories  因为切换到远程分支,而本地并没有该分支,意思时候拒绝合并不相关的历史
  - 需要把该远程分支pull下来
  - `git pull origin home --allow-unrelated-histories`

- you need to resolve your current index first---解决git reset --merge


## git 删除远程分支

- `git push origin --delete branch_name`

## git拉取指定分支

- `git clone -b js codeRepoURL.git`
- [拉取指定分支](https://www.jianshu.com/p/856ce249ed78)

gitbook 与node的转换以及gitbook build 构建文件的排除问题

## [git push常用命令](https://www.cnblogs.com/qianqiannian/p/6008140.html)

## [git push -u问题 追踪](https://www.cnblogs.com/dyh-air/p/9257237.html)

## git origin 已存在问题

- 

##  git 初始化后 连接远程仓库

- git remote add origin https://github.com/JadestarHan/book.git
- git remote -v  查看origin连接的是那个仓库
- 然后git branch 
- 然后就可以推送了 push 

## git 问题 [Everything up-to-date解决](https://blog.csdn.net/myhuashengmi/article/details/52197566)

## git 问题 fatal: Not a valid object name: 'master'.

- 描述  一个非法的master 本地还没有创建master

- `add file`

- `add commit -m"msg"`

- 此时本地仓库主干master创建成功

- 创建新分支`git branch dev`

- 切换分支`git checkout dev`

- `git push origin dev`

- [git push问题](https://www.cnblogs.com/qianqiannian/p/6008140.html)

  ``````
  $ git push s10
  fatal: 's10' does not appear to be a git repository
  fatal: Could not read from remote repository.
  
  Please make sure you have the correct access rights
  and the repository exists.
  错误是因为 应该是git push origin s10,因为是远程,命令少写了一个origin标识符
  ``````





## git quit<enter> 同 exit vim怎么退出

- :qa!  按回车  退出vim



## git合并分支合并冲突问题

- merge



## git fork是啥



## git分支的新建和删除

- `git branch dev`



## git tag的新建和删除

- [创建tag](https://www.cnblogs.com/senlinyang/p/8527764.html)((本地)) ```git tag -a  v1.0 -m "msg"```
- 查看tag ```git tag```
  - 要显示附注信息使用show指令`git show v1.0`
- 创建tag(远程)`git push origin --tags`
- 删除tag(本地)`git tag -d v1.0`
- 删除tag(远程) `git push origin :refs/tags/v1.0`
- 获取远程版本 `git fetch origin tag v1.0`



## git的安装配置使用

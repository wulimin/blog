---
layout : post
title : git使用方法
category : git
tag : git
---

### 基本使用
>git branch 分支名                    //新建分支  <br>
>git push origin 分支名              //把分支推送到远程  <br>
>git checkout -b 分支名             //创建并切换分支  <br>
>git add -i                                //查看已经add的文件  <br>
>git log                                    //查看已经commit的文件  <br>
>git show  hashcommitID      //查看某次提交改过的内容  <br>
>git log -n 1 --stat                   //查看最后一次提交所有更改过的文件  <br>
>git log online -pretty   <br>

>git branch  -r  -d 分支名           //删除本地分支  <br>
>git push origin  :分支名           //删除远程分支名  <br>
>git rm -rf 文件名                      //删除git版本的文件  <br>
>git rm -r --cached  某个目录    //删除多个git版本的文件  <br>

>git reset HEAD^                    //回退所有内容到上一个版本  <br>
>git reset 057d                      //回退到某个版本   <br>
>git revert HEAD                    //撤销前一次 commit  <br>
>git revert commit-id             //撤销指定的版本，撤销也会作为一次提交进行保存  <br>
>git revert是用一次新的commit来回滚之前的commit，git reset是直接删除指定的commit
看似达到的效果是一样的,其实完全不同.  <br>
第一 : 
上面我们说的如果你已经push到线上代码库, reset 删除指定commit以后,你git push可能导致一大堆冲突.但是revert 并不会.  <br>
第二 : 
如果在日后现有分支和历史分支需要合并的时候,reset 恢复部分的代码依然会出现在历史分支里.但是revert 方向提交的commit 并不会出现在历史分支里.  <br>
第三 : 
reset 是在正常的commit历史中,删除了指定的commit,这时 HEAD 是向后移动了,而 revert 是在正常的commit历史中再commit一次,只不过是反向提交,他的 HEAD 是一直向前的.  <br>


### 避免git pull提示      git pull <remote> <branch>
* git branch --set-upstream-to=origin/po_project_1

### git设置远程ssh:
* ssh-keygen -t rsa -C "xiaoxiao@gmail.cn"

### git删除未跟踪文件 删除 untracked files
* git clean -f
* git clean -d -fx
* git clean -fd   //连untracked 的目录也一起删掉
* git clean -xfd  // 连gitignore 的untrack 文件/目录也一起删掉 （慎用，一般这个是用来删掉编译出来的 .o之类的文件用的）
* git clean -nxfd
* git clean -nf
* git clean -nfd
（注 ： 在用上述 git clean 前，墙裂建议加上 -n 参数来先看看会删掉哪些文件，防止重要文件被误删）

### git stash使用 
简而言之就是帮助开发人员暂时搁置当前已做的改动，倒退到改动前的状态，进行其他的必要操作（比如发布，或者解决一个bug，或者branch，等等），之后还可以重新载入之前搁置的改动

```javascript
git add .   //用git add把所有的改动加到staging area
git stash   //把这些改动搁置
git stash apply  //找回之前搁置的改动继续先前的工作
git stash list  //查看所有的_搁置版本
git stash pop //在搁置栈想找回第1个
git stash apply stash@{1} //在搁置栈想找回第2个
git stash drop stash@{1}  //删除一个stash
git stash clear  //删除所有stash
```

### git tag使用
tag是对历史commitID做的标记，如果想切换到tag,可以使用git checkout tag
其实切换到tag历史记录，在切换回主线时如果没有合并，之前的修改提交基本都会丢失。
如果需要修改，可以创建基于tag的一个分支，git checkout -b branch tag,此时便会在分支上开发，之后切换到主线合并。


### git submodule子模块
* 添加  <br>
git submodule add 仓库地址 路径
* 删除  <br>
a.在.gitmodules删除相应配置信息    <br>
b.执行git rm -cached 将子模块从git中删除
* 更新  <br>
git submodule update --init --recursive




















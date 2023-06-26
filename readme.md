# Readme This is Git Test
---
## 基础提交 日志查看 回退
`git add textName` : 提交至暂存区
`git commit -m "xx" testName` : 提交至本地库
`git status`: 查看工作区和暂存区状态

`git log`:查看提交日志  
(分页情况 `spacebar` 下一页 `b` 上一页)
`git reflog`: 查看指针回到历史版本步数
  
`git reset`  
- `git reset --hard 索引号`:前进或者后退历史版本 （当前暂存区内容会因为回退消失）
- `git reset --mixed 索引号`:本地库的指针移动的同时，重置暂存区，但是工作区不动 
- `git reset --soft 索引号`:本地库的指针移动的时候，暂存区，工作区都不动  
   
<br/>
## diff区分

`git diff` : 比较工作区中和暂存区中 所有文件的差异 
- `git diff .\readme.md` ：将工作区中的文件和暂存区中文件进行比较  
- `git diff 17bcf00 .\readme.md` ：比较暂存区和本地库中内容
- `git diff HEAD .\readme.md` : 比较暂存区和本地库中内容

<br/>
## 分支
`git branch 分支名` :创建分支
`git branch -v` :查看分支
`git checkout 分支名` :切换分支  
`git merge 分支名` :合并分支(处于主分支时使用指令)

<br/>

## 添加远程库
`git remote -v`:远程库信息查看
`git remote 远程库名 add 远程库地址`: 添加远程库
`git push 远程库名 分支名`: 推送至远程库
`git clone 远程库地址`: 远程库内容同步到本地
```console
admin@DESKTOP-8HMQAG5 MINGW64 /d/Download_Browser/mashibing/工具/Git资料和软件/git_test/test1 (master)
$ git remote add origin https://github.com/CrowYao/Test.git

admin@DESKTOP-8HMQAG5 MINGW64 /d/Download_Browser/mashibing/工具/Git资料和软件/git_test/test1 (master)
$ git remote -v
origin  https://github.com/CrowYao/Test.git (fetch)
origin  https://github.com/CrowYao/Test.git (push)

$ git push origin master
```

<br/>

## 拉取至本地
`git fetch 远程别名 远程分支`: 将远程代码拉至本地暂存区
`git merge 远程别名/远程分支名`: 将远程指定分支代码合并到本地(确认在本地master分支进行操作)
`git pull 远程别名/远程分支名`： 将 fetch + merge 一次性做完（存在风险）
```console
$ git fetch origin master

$ git merge origin/master

$ git merge origin/master --allow-unrelated-histories (出现unrelated hisory报错可以使用该代码)


```




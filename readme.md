# Readme This is Git Test
---
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


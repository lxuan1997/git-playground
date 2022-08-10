# git-playground
for git practice

## Merge 测试
## git Commits 提交记录出现 Merge branch 'main' of ...
### 原因
当多人合作开发一个项目时，本地仓库落后于远程仓库，执行 `git push`
### 场景还原
1. user1 和 user2 各拉取master分支至本地进行开发
2. user1 比 user2 先提交代码
3. user2 执行`git push` 时，提示需要先进行 `git pull` 操作
4. user2 以此执行 `git pull` 、 `git push`
5. 发现提交记录显示 `user2 Merge branch 'main' of ...`

### 如何避免
``` bash
# 拉取
git pull --rebase

# 提交
git push
```

# git-practice

文章參考：[【Git 教學】分支合併: merge 與 rebase 差異](https://www.maxlist.xyz/2020/05/02/git-merge-rebase/)

### 分支 branch 合併操作

#### merge 篇

在使用 merge 合併分支的時候，git 預設會以 fast-forward 的模式進行，那什麼是 fast-forward 和 no-fast-forward 呢？

> fast-forward

git checkout master //先切換到主分支
git merge <branch> //使用 fast-forward

> no-fast-forward

git checkout master //先切換到主分支
git merge <branch> --no-ff //使用 no-fast-forward

使用 no-fast-forward 的版本會留下原先的歷程，但過多也會造成混亂，
因此就會使用 fast-forward 來 merge 比較不重要的 commit，如零碎的 bug fix，使版面較為乾淨。

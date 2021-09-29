# git-training

### 1,準備編

```bash
$ mkdir git-training
$ git init
$ git config --local user.name ""
$ git config --local user.email ""
$ git remote add origin git@github.com:Iovesophy/git-training.git
$ touch README.md
$ git add .
$ git commit -m "ADD README"
$ git push origin master
```

## 18, git resetを行う

操作記録

```
$ git add .
$ git commit -m "ADD usecase 6"
$ touch hoge
$ git reset HEAD^
$ git add README.md
$ git reflog
$ git reset --hard HEAD@{1}
$ git reset --mixed HEAD^
$ git reflog
$ git reset --hard HEAD@{3}
$ git reset --soft HEAD^
$ git restore --staged diff1.patch diff2.patch usecase5.txt
$ git reflog
$ git add .
$ git commit README.md
$ git restore --staged .
```

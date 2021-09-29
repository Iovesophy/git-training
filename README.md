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

### 5, インデックスに記録されているファイルとリモートトラッキングブランチとの差分を見る

```bash
$ git diff --cached origin/<branch_name>
```

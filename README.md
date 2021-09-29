# git-training

### 0,準備編

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

### 1,現在参照しているブランチ名を変更する

```bash
$ git checkout -b branch1
$ git checkout master
$ git checkout branch1
```

### 2,ブランチを特定のブランチをベースにして新規作成する

```bash
$ git checkout -b <new_branch_name> <target_branch>
```




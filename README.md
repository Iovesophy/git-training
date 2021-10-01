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

### 9, ファイルの行単位で最終変更がどのコミットで行われたのか確認する

```bash
$ git blame <filename>
```


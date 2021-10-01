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

## 7, インデックスに記録されている変更を直前のコミットに混ぜる

```bash
$ git commit
$ git rebase -i HEAD~~
(squashする)
```


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

## 6, プルリクエストで発生したコンフリクトを修正する

rebaseで解決
```bash
$ git pull --rebase origin <to_merge_branch_name>
$ git add <filename>
$ git rebase --continue
```

pullで解決
```bash
$ git pull origin <to_merge_branch_name>
$ git add <filename>
$ git rebase --continue
```

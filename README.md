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
$ git checkout -b <to_change_branch_name>
$ git branch -m <new_branch_name>
```

### 2,ブランチを任意のブランチをベースにして新規作成する

```bash
$ git checkout -b <new_branch_name> <target_branch>
```

### 3, ブランチを強制的に変更(checkout)する

```bash
$ git checkout -f <target_branch>
```

## 4, インデックスに記録されているファイルをインデックスから解除する

```bash
$ git restore --staged <filename>
```

### 5, インデックスに記録されているファイルとリモートトラッキングブランチとの差分を見る

```bash
$ git diff --cached origin/<branch_name>
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

## 7, インデックスに記録されている変更を直前のコミットに混ぜる

```bash
$ git commit
$ git rebase -i HEAD~~
(squashする)
```

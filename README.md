# git-training

0. 準備編
    - mkdir git-training
    - git init
    - git config --local user.name ""
    - git config --local user.email ""
    - git remote add origin git@github.com:Iovesophy/git-training.git
    - touch README.md
    - git add .
    - git commit -m "ADD README"
    - git push origin master

1. 現在参照しているブランチ名を変更する
    - git branch -m <new_branch_name>

2. ブランチを任意のブランチをベースにして新規作成する
    - git checkout -b <new_branch_name> <target_branch>

3. ブランチを強制的に変更(checkout)する
    - git checkout -f <target_branch>

4. インデックスに記録されているファイルをインデックスから解除する
    - git restore --staged <filename>

5. インデックスに記録されているファイルとリモートトラッキングブランチとの差分を見る
    - git diff --cached origin/<branch_name>

6. プルリクエストで発生したコンフリクトを修正する
    - mergeで解決
        - git merge <to_merge_branch_name>
        - git add <filename>
        - git merge --continue
    - rebaseで解決
        - git pull --rebase origin <to_merge_branch_name>
        - git add <filename>
        - git rebase --continue
    - pullで解決
        - git pull origin <to_merge_branch_name>
        - git add <filename>
        - git rebase --continue

7. インデックスに記録されている変更を直前のコミットに混ぜる
    - git commit --amend

8. 前にいたブランチに戻る
    - git checkout -

9. ファイルの行単位で最終変更がどのコミットで行われたのか確認する
    - git blame <filename>

10. 直前のコミットで変更したファイルの内容を見る
    - git show

11. コミット対象外のファイルを削除する
    - git clean -f
    - option
        - d: ディレクトリも含める
        - f: 削除する
        - n: Dry-run

12. ワーキングツリーの変更を元に戻す
    - git checkout .

13. ワーキングツリーとインデックスの変更を元に戻す
    - git checkout -f .

14. リベースをキャンセルする
    - git rebase --abort

15. cherry-pickをキャンセルする
    - git cherry-pick --abort

16. マージをキャンセルする
    - git merge --abort

17. 特定のファイルだけインデックスに追加する
    - git add <filename>

18. HEADの状態をインデックスに戻す
    - git reset --mixed HEAD^

19. HEADの状態をワーキングツリーに戻す
    - git reset --hard HEAD

20. 特定のファイルのブロックだけインデックスに追加する
    - git add -p <filename>

21. ワーキングツリーとインデックスの更新差分をインデックスに追加する
    - git add -u

22. インデックスとHEADの差分を表示する
    - git diff --cached

23. コミットを強制的にプッシュする
    - git push -f <repository_name> <branch_name>

24. リモートブランチの更新を取り込んで特定のブランチをベースにリベースする
    - git pull --rebase <repository_name> <branch_name>

25. HEADのコミットメッセージを変更する
    - git commit --amend -a
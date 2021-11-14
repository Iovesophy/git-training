# git-training

0. 準備編
    - git clone git@github.com:Iovesophy/git-training.git
    - git config --local user.name `"<name>"`
    - git config --local user.email `"<email>"`
    - git config --local color.ui true

1. 現在参照しているブランチ名を変更
    - git branch -m `<new_branch_name>`

2. 新規ブランチを任意のブランチをベースにして作成
    - git checkout -b `<new_branch_name>` `<base_branch_name>`

3. ブランチを強制的に変更(checkout)
    - git checkout -f `<target_branch_name>`

4. インデックスに記録されているファイルをインデックスから解除
    - git restore --staged `<filename>`

5. インデックスに記録されているファイルとリモートトラッキングブランチとの差分
    - git diff --cached origin/`<branch_name>`

6. プルリクエストで発生したコンフリクトを修正
    - mergeで解決
        - git merge `<to_merge_branch_name>`
        - git add `<filename>`
        - git merge --continue
    - rebaseで解決
        - git pull --rebase origin `<to_merge_branch_name>`
        - git add `<filename>`
        - git rebase --continue
    - pullで解決
        - git pull origin `<to_merge_branch_name>`
        - git add `<filename>`
        - git merge --continue

7. インデックスに記録されている変更を直前のコミットに混ぜる
    - git commit --amend

8. 前にいたブランチに戻る
    - git checkout -

9. ファイルの行単位で最終変更がどのコミットで行われたのか確認
    - git blame `<filename>`

10. 直前のコミットで変更したファイルの内容を見る
    - git show

11. コミット対象外のファイルを削除
    - git clean -f
    - option
        - d: ディレクトリも含める
        - f: 削除
        - n: Dry-run

12. ワーキングツリーの変更を元に戻す
    - git checkout .

13. ワーキングツリーとインデックスの変更を元に戻す
    - git checkout -f

14. リベースをキャンセル
    - git rebase --abort

15. cherry-pickをキャンセル
    - git cherry-pick --abort

16. マージをキャンセル
    - git merge --abort

17. 特定のファイルをインデックスに追加
    - git add `<filename>`

18. HEADの状態をインデックスに戻す
    - git reset --mixed HEAD^

19. ワーキングツリーとインデックスの状態をHEADに戻す
    - git reset --hard HEAD

20. 特定のファイルのブロックだけインデックスに追加
    - git add -p `<filename>`

21. ワーキングツリーとインデックスの差分をインデックスに追加
    - git add -u

22. インデックスとHEADの差分を表示
    - git diff --cached

23. 強制的にプッシュ
    - git push -f `<repository_name>` `<branch_name>`

24. リモートブランチの更新を取り込んで特定のブランチをベースにリベース
    - git pull --rebase `<repository_name>` `<branch_name>`

25. HEADのコミットメッセージを変更
    - git commit --amend -m `"<message>"`
    - git rebase -i HEAD~`<number>`
        - r, reword `<commit>` = use commit, but edit the commit message

26. Gitの操作履歴を閲覧
    - git reflog

27. 前のブランチに強制的にチェックアウト
    - git checkout - -f
        
28. ワーキングツリーとインデックスの変更を直前のコミットに混ぜる
    - git commit -a --amend
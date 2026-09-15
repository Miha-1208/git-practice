# git-practice
git練習用
川﨑晴輝
VScode上で開いた。
`git status` `git add .` `git commit -m` `git push` `git pull` のコマンドを実際に使い役割を覚えた。  
git commit -amが　add+commitと知った。
※一度もaddされたことのないファイルには使用できない
git commitを抜いてgit push した羅どうなるか確認。
# 詰まった点と解決

- push が rejected (fetch first) になった。
  GitHub側に手元にない変更があると拒否される安全装置。git pull で解決。
- コミットメッセージの引用符が全角になり、`>` が出て入力が終わらなくなった。
  Ctrl+C で中断。引用符とハイフンは必ず半角。
- GitHub上で編集した内容がVS Codeに反映されない。
  push は手元→GitHub、pull は GitHub→手元。自動同期ではないので pull が必要。
- ブランチを切ると手元の見え方が変わる。git branch で現在地を確認できる。
- git add だけして git push すると「Everything up-to-date」と出る。
  push が送るのはコミットなので、commit していないと送るものがない。

# 学んだ仕組み

- Gitには4つの場所がある
  ワークツリー →(add)→ インデックス →(commit)→ ローカルリポジトリ →(push)→ GitHub
  各コマンドは1区間ずつしか動かさない。
- add が分かれている理由は、編集が終わった後から記録する範囲を選べるようにするため。
  1人・1ファイルの練習では必要性が薄いので、今は add . で全部でよい。
- Git と GitHub は別物。Git は手元の仕組み、GitHub は置き場所。
- リポジトリ = フォルダ1個。README.md はその中のただのファイル。

# 環境

- Windows / Git Bash / VS Code
- Git Bash では貼り付けが右クリック
- push はパスワードではなく Personal Access Token が必要
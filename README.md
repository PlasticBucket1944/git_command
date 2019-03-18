# README

## 開発中の基本の流れ
現在のブランチの確認
git branch

新規ブランチの作成
git branch <ブランチ名>

ブランチの変更
git checkout <ブランチ名>

変更箇所のステージング
git add .

ステージングしたファイルの確認
git status

コミット
git commit -m 'コメント'

変更箇所の取り消し
git checkout .

ローカルのブランチをリモートにプッシュする
git push -u origin <プッシュしたいローカルのブランチ名>

リモートのブランチを削除する、上げ直す時にやる
git push origin :<消したいリモートのブランチ名>

リモートのマスターから最新の物を取ってくる(ローカルのmasterのブランチで行う)
git pull

現在のブランチにローカルのマスターのブランチの変更を反映する
git marge master

## 開発が始まった時にする事

プロジェクトをgitで管理しますよって宣言
git init

リモートリポジトリを指定する
git remote add origin https://github.com/<ユーザー名>/<リモートリポジトリ名>.git

git push -u origin master

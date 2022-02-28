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

## コンフリしたらする事
1.リモートのmasterをローカルのmasterに引っ張ってくる  
git checkout master  
git pull  

2.作業中のブランチに最新のmasterの変更を反映させる  
git checkout <作業中のブランチ名>  
git marge master  

3.ここでコンフリが起きるので修正する、修正したらコミット  
git add .  
git commit -m '競合を解消'  

## 開発が始まった時にする事

プロジェクトをgitで管理しますよって宣言  
git init  

リモートリポジトリを指定する  
git remote add origin https://github.com/<ユーザー名>/<リモートリポジトリ名>.git  

とりあえずプッシュしとけ  
git add .  
git commit -m 'first commit'  
git push -u origin master  

2021/10/25：masterからmainへ主リポジトリ名が変わっているので注意  
メインのリポジトリ名を変更  
git branch -M main  
git push -u origin main  

**その他、githubのアクセストークンの有効期限にも注意**  
https://qiita.com/kz800/items/497ec70bff3e555dacd0  

## その他使うコマンド

ローカルブランチの削除  
git branch -D <削除したいブランチ名>  

ローカルブランチの一括削除  
git branch | grep <削除したいブランチ名が入った文字列> | xargs git branch -d  

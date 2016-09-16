# ニコ生駆動開発の成果物  

ニコ生駆動開発で作成されたゲームを公開するリポジトリです

- 20160929放送分  
(まだ無いようだ)

## ゲームのアップロード手順
1. リポジトリをクローンする  
コマンドプロンプトを開き、クローンするフォルダに移動  
```
cd　c:\  
mkdir projects
cd projects
git clone git@github.com:nikonamakudou/games.git
```  

2.  放送日のフォルダに作成したゲームを格納する  
フォルダの構成は放送日フォルダの下に個人のアカウント名でフォルダを作り、  
その中にビルドしたゲームを保存する。  
```
nikonamakudou/games/(放送日)/(名前)  
```

3. GitHubにPushする  
再びコマンドプロンプトを開き、ゲームを格納したフォルダに移動する。  
```
cd nikonamakudou/games/(放送日)/(名前)
```
ブランチを確認する
```
git branch
```
masterにいることを確認する
```
*master
```  
gh-pagesブランチにチェックアウトする  
```  
git checkout -b gh-pages  
git branch
```
gh-pagesに切り替わったことを確認する
```
*gh-pages
master
```
gh-pagesブランチに変更をコミットする
```
git add .
git commit -m "ゲーム作ったよ"
```
GitHubにプッシュする
```
git push origin gh-pages
```

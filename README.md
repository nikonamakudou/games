# ニコ生駆動開発の成果物  

ニコ生駆動開発で作成されたゲームを公開するリポジトリです

- 20160929放送分  
[配信枠 http://live.nicovideo.jp/gate/lv277158737](http://live.nicovideo.jp/gate/lv277158737)  
 - その１  
 https://nikonamakudou.github.io/games/20160929/t-zouchi/

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
ローカル環境のgh-pages ブランチを最新にする   
・ gh-pagesがない場合
```
git fetch
git checkout -b gh-pages
git pull orogin gh-pages
```
・gh-pagesがある場合
```
git checkout gh-pages
git pull origin gh-pages
```  
プルリク作る用ブランチにチェックアウトする  
```  
git checkout -b (hogehoge)  
git branch
```
作ったブランチに切り替わったことを確認する
```
*hogehoge
gh-pages
master
```
作ったブランチに変更をコミットする
```
git add .
git commit -m "ゲーム作ったよ"
```
GitHubにプッシュする
```
git push origin hogehoge
```
GitHub上でgh-pagesにプルリクを作る  

4. READMEのアップデート  
masterブランチを最新にする
```
git checkout master
git pull origin master
```
アップデート用のブランチにチェックアウトする
```
git checkout -b (fugafuga)
```
移動したことを確認する
```
*fugafuga
master
gh-pages
```
`README.md`をテキストエディターで開く  
ゲームのURLは以下のように作る  
```
https://nikonamakudou.github.io/games/(放送日)/(名前)  
```
ブラウザで開けることを確認したら`README.md`に書き足す  
変更をコミットする  
```
git add README.md
git commit -m "いい感じのコミットメッセージを書く"
git push origin fugafuga
```
GitHubでプルリクを作って完了

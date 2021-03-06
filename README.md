# Wordpress 環境構築(Mac)

## Docker Desktopのインストール

https://docs.docker.com/docker-for-mac/install/
ここ参照

※Dockerとは

仮想環境を構築するツール。PCの上にもう1台PCを構築するイメージ。

環境構築の情報を設定ファイルで定義する。OSとかに左右されずに同じ環境でプログラムが実行できたりするメリットがある。

今の開発現場ではめちゃくちゃ使うので余裕があったら覚えておくと良い。


https://kitsune.blog/docker-summary

## ターミナルを起動

アプリケーションの中にターミナルってやつがあるはずなのでそれを選択して起動

ここからはコマンドを使っていく

## 開発用ディレクトリに移動

ターミナルは自分が今いるフォルダ(ターミナルで操作するときはディレクトリと呼ぶのが一般的)でコマンドを実行していく
まずはWordpressを使うディレクトリまで移動する

`cd /適当なところ`

cd コマンドについて

https://webkaru.net/linux/cd-command/

## このリポジトリをclone

`git clone https://github.com/tshackstream/wordpress-build-with-docker.git`

※git とは

プログラムソースの変更履歴とかを確認するためのツール

複数人で開発するときとかは必ずといっていいほど使うのでほぼマストで覚えるべき


https://kitsune.blog/git-summary

ディレクトリができる

## Wordpressを起動

`cd wordpress-build-with-docker`

`docker-compose up -d`

終わったら

`docker-compose ps`

↓のように表示されればOK

```
            Name                          Command               State          Ports
--------------------------------------------------------------------------------------------
word-press-build_db_1          docker-entrypoint.sh mysqld      Up      3306/tcp, 33060/tcp
word-press-build_wordpress_1   docker-entrypoint.sh apach ...   Up      0.0.0.0:8000->80/tcp
```

## Wordpressにアクセス

chromeとかSafariとかのブラウザで

http://localhost:8000

にアクセス。表示されればOK。

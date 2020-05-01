# Wordpress 環境構築(Mac)

## Docker Desktopのインストール

https://docs.docker.com/docker-for-mac/install/
ここ参照

## ターミナルを起動

アプリケーションの中にターミナルってやつがあるはずなのでそれを選択して起動

ここからはコマンドを使っていく

## 開発用ディレクトリに移動

ターミナルは自分が今いるフォルダ(ターミナルで操作するときはディレクトリと呼ぶのが一般的)でコマンドを実行していく
まずはWordpressを使うディレクトリまで移動する

cd /適当なところ

cd コマンドについて
https://webkaru.net/linux/cd-command/

## このリポジトリをclone

git clone https://github.com/tshackstream/wordpress-build-with-docker.git

ディレクトリができる

## Wordpressを起動

cd wordpress-build-with-docker

docker-compose up -d

終わったら
docker-compose ps

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
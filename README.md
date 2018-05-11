# Java8 + Embulk (日本環境） #

オフィシャルのjava8を元に日本環境の調整を行いました。

### 調整内容 ###

* locale設定 (ja.utf-8)
* タイムゾーン （Asia/Tokyo）
* 必要なツールのインストール  
※ less vim git zip unzip git
* embulk version 0.8.32

### 使い方 ###

下記のコマンドにてコンテナを起動します

```
$ docker pull reflet/embulk
$ docker run -d --name embulk reflet/embulk
$ docker exec -it embulk bash
# embulk
Embulk v0.8.32
...
```

### メンテナンス ###

下記のコマンドにてソースのダウンロードとイメージの構築を実行します。

```
$ git clone git@github.com:reflet/docker-embulk.git .
$ docker build -t reflet/embulk .
$ docker login
$ docker tag reflet/embulk reflet/embulk:{タグ}
$ docker push reflet/embulk
```


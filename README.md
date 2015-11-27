## [RocketChat](https://github.com/RocketChat/Rocket.Chat) を nginx で reverse proxy するサンプル

※ 注意事項
- 今のところ、サブフォルダでの指定は [ Issue #1434 · RocketChat/Rocket.Chat](https://github.com/RocketChat/Rocket.Chat/issues/1434) があるのでちゃんと動かないようだ...
- mongo 使ったことないから設定が適当です。特にレプリケーション周りが怪しい。

### 使い方

- docker をインストールしてください
- docker-compose をインストールしてください
- 以下の作業をしてください

```console
$ git clone https://github.com/mapk0y/docker-nginx-sample-publish
$ cd docker-nginx-sample-publish
$ # docker-compose と nginx/rocketchat.conf の URL(www.example.com) を環境に合わせて修正する
$ docker-compose build
$ docker-compose up -d 
$ #ログを眺める
$ docker-compose logs
```

### 色々試すときやること

```console
$ # コンテナを止める
$ docker-compose stop
$ # コンテナを削除する
$ docker-compose rm
$ # 色々変える

$ # 必要なら build する
$ docker-compose build
$ docker-compose up -d
```


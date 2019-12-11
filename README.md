# Docker Rails Starter
Docker上で動作するRails web application のボイラープレート

## 環境構築

dockerビルド
```
$ cd docker
$ docker-compose build --no-cache
```

bashターミナルを起動
```
$ docker-compose run --rm --service-ports rails
```

Rails applicationに移動
```
# rails new app
$ cd app
```

gemの更新とインストール
```
$ bundle update && bundle install
```

Rails起動
```
$ rails server -p $PORT -b 0.0.0.0
```

起動したら http://localhost:3000/ にアクセスすると確認ができます。

dockerコンテナから抜ける
```
$ exit
```

作業が完了したらクリーンアップ
```
$ docker-compose down
```

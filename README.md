# db-index-demo
インデックスを試すための検証用Dockerコンテナ

## 環境構築の手順
1. docker-composeでコンテナを立ち上げておく

```
$ docker-compose up -d
```

2. 2でcloneした中から、使用したいSQLファイルを実行してデータをDBコンテナに挿入する

```
$ docker-compose exec -it db bash

// 以下よりDockerコンテナ内で実行
$ cd /test_db
$ mysql -u root -p < employees.sql // パスワードには password と入力
```

## その他
テストデータのSQLは、MySQL公式で提供されている以下のリポジトリの内容をコピペしています。
https://github.com/datacharmer/test_db
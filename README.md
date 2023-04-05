# Mysql Container

## Description

Mysql 単体のコンテナです。

試しでバックエンドを組んでいる時等に使い捨て DB として使用する用途を想定しています。

## Usage

1. Clone 後に`docker compose up -d --build`を実行

2. コンテナの再起動

起動後、30 秒くらいで一度停止してしまうバグがあります。

3. Mysql へのログイン

CLI からのアクセス方法は以下のコマンドです。

```
mysql -h 127.0.0.1 -u root -p
```

パスワードは、`password`です。

4. 起動時に作成される database 名は laravel です。

## Laravel User

.env ファイルの該当箇所を以下のようにしてください。

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=password
```

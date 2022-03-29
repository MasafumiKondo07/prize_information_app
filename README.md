# プライズ情報横断アプリ

## 環境構築手順

```
docker-compose build

docker-compose up

docker-compose exec web rails db:create
```

## デプロイ手順

```
heroku container:login

heroku container:push web -a prize-information-app

heroku container:release web

heroku addons:create heroku-postgresql:hobby-dev

heroku run rails db:migrate
```
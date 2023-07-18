# はじめかた

## ビルド & 起動

立ち上がらない場合があるため、その場合は一度キャンセルして、再度 up コマンドを入力する。

```
docker-compose build ;
docker-compose up --scale web=2 -d ;
```

## マイグレーション

```
docker exec -it django-lb-sample-web-1 bash ;

~~~/app# python manage.py migrate ;
~~~/app# python manage.py createsuperuser ;
~~~/app# exit
```

## サイトアクセス

http://localhost:18081/

# 留意事項

- クッキーの取り扱い等、セキュリティ的に不十分な可能性があるので、要調査。

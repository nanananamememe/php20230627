# php20230627

``` bash
$ git clone https://github.com/nanananamememe/php20230627.git
$ docker volume create mysql
$ docker volume create redis
$ docker volume create minio
$ docker-compose up -d --build
$ docker-compose exec app composer create-project laravel/laravel example-pj
$ docker-compose restart
```

※/var/www/example-pj/storage/logs/laravel.log で Permission denied が発生するようであれば、 example-pj/storage の権限を変更してください。
``` bash
$ docker-compose exec app chmod 777 example-pj/storage;
```


``` bash
$ docker-compose exec app bash
# docker-php-ext-install pdo_mysql
# php example-pj/artisan migrate
# php example-jp/artisan db:seed
```

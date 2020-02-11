# Laravel 6

- Création d'un nouveau projet :
```shell
laravel new AppName
```
- Lancer le serveur :
``php artisan valet`` ou http://AppName.test

## Routes :
```php
#./routes/web.php

Route::get('/', function () {
    return view('welcome');
});
```

## Views :
./resources/views/welcome.blade.php


- Créé un model post :
```shell
php artisan make:model Post
```

- Créé un controller :
```shell
php artisan make:controller PostsController
```

- Créé une migration :
```shell
php artisan make:migration create_posts_table
```
./database/migrations/...create_posts_table.php

## Créé une base de donnée :
```shell
mysql -u root
create database database_name
```
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
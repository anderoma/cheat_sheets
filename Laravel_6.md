# Laravel 6
- [Routes](#routes-)
- [Views](#views-)
- [Créé une base de donnée](#créé-une-base-de-donnée-)
- [Migrations](#migrations-)
- [Liens utiles](#liens-utiles-)

## Start :
- Création d'un nouveau projet :
```shell
laravel new AppName
```
- Lancer le serveur :
``php artisan serve`` ou utilise valet ``valet install`` et http://AppName.test

## Routes :

- Pour voir toutes les routes :
```shell
php artisan route:list
```
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

## Créé une base de donnée :
```shell
mysql -u root
create database database_name
```

## Migrations :
- Créé une migration :
```shell
php artisan make:migration create_posts_table
```
./database/migrations/...create_posts_table.php

- Passe toutes les migrations en attente <strong>(= les mets en up)</strong>
```shell
php artisan migrate
````

- Status des migrations (te sort un joli tableau pour voir où tu en es dans tes migrations entre les up et les down)
```shell
php artisan migrate:status
```

## Authentification user :
```shell
composer require laravel/ui --dev
```
```shell
php artisan ui vue --auth
```
```shell
npm install && npm run dev
```

## Liens utiles :

### Formulaire de contact :
- https://www.baymediasoft.com/blog/laravel/a-complete-guide-10-steps-for-creating-contact-form-in-laravel-5-7

### Heroku  :
- https://medium.com/swlh/how-to-host-your-laravel-application-for-free-on-heroku-4789688d444b
- https://medium.com/@juangsalazprabowo/how-to-deploy-a-laravel-app-into-heroku-df55efbf8e4e
- https://devcenter.heroku.com/articles/getting-started-with-laravel

### Flash message :
- https://codesource.io/work-with-laravel-flash-messages/
- https://www.itsolutionstuff.com/post/laravel-6-flash-message-tutorialexample.html

### E-commerce :
- https://www.codementor.io/@pknerd/develop-an-e-commerce-website-with-laravel-5-4-part-7-bdy55gwxe
- https://github.com/kadnan/golmarket
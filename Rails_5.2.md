# Démarer avec ruby on rails 5.2

J'utilise un alias 
``
rn='rails new -d postgresql'
``
pour crée un nouveau projet ruby on rails avec une base de donnée postgresql pour permettre de déployer plus facilement sur Heroku.

- Crée ton projet :
```shell
rn AppName
```
- Va dans le projet :
```shell
cd AppName
```
$ rails g model User name:string email:string (Singulier):
$ rails db:create 
$ rails db:migrate
$ rails g controller Users index show

# Démarer avec ruby on rails 5.2

J'utilise un alias pour crée un nouveau projet ruby on rails avec une base de donnée postgresql pour permettre de déployer plus facilement sur Heroku.
``
rn='rails new -d postgresql'
``
rn app
$ rails g model User name:string email:string (Singulier):
$ rails db:create 
$ rails db:migrate
$ rails g controller Users index show

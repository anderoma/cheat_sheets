# Déployer une application heroku avec ruby on rails 

## 1. Lancement
Commencer par créer une nouvelle appli rails : 
```shell
$ rails new nom_de_mon_app
```
! Attention de créer une app rails avec une base de donnée PostGreSQL parce que Heroku utilise cette base de donnée.

## 2. First commit
En théorie, installer une app rails initialize un git, donc pas besoin de `git commit`. On va donc faire le premier commit. Si l'on veut lier son application Rails à un remote, c'est possible avec `git remote add origin blabla_nom_origine`.

```shell
git add .
git commit -m "premier commit"
```

## Git push heroku master
Maintenant il ne reste plus qu'à commiter, et pousser ça chez heroku.
```shell
$ git add .
$ git commit -m "Gemfile OK"
$ heroku create
$ git push heroku master
```
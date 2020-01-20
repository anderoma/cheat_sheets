# Déployer une application Heroku avec Ruby on Rails 

## 1. Lancement
Commencer par créer une nouvelle appli Rails.

! Attention de créer une app rails avec une base de donnée PostGreSQL parce que Heroku utilise cette base de donnée.

```shell
rails new -d postgresql
```

## 2. First commit
En théorie, installer une app rails initialize un git, donc pas besoin de `git commit`. On va donc faire le premier commit. Si l'on veut lier son application Rails à un remote, c'est possible avec `git remote add origin blabla_nom_origine`.

```shell
git add .
git commit -m "premier commit"
```

## 3. Git push heroku master
Maintenant il ne reste plus qu'à commiter, et pousser ça chez heroku.
```shell
git add .
git commit -m "Heroku"
heroku create
git push heroku master
```

## Stop Heroku app from sleeping
Si vous utilisez gratuitement heroku, l'hébergeur de votre site se met en veille au bout de 30 min.
Pour remedier à ça et, garder disponible votre site web à tout moment, utiliser [Heroku Scheduler](https://devcenter.heroku.com/articles/scheduler).

Commence par créer une Rake task dans ton app Rails, 
dans `lib/tasks` créer un fichier schedule.rake

```desc "Pings PING_URL to keep a dyno alive"
task :dyno_ping do
  require "net/http"

  if ENV['PING_URL']
    uri = URI(ENV['PING_URL'])
    Net::HTTP.get_response(uri)
  end
end
```

Ajoute PING_URL à ton environnement Heroku: 

```
heroku config:add PING_URL=http://my-app.herokuapp.com
```
Configure un planificateur:

```
heroku addons:add scheduler:standard
heroku addons:open scheduler
```

Cette dernière commande devrait ouvrir l'interface du planificateur dans votre navigateur. Vous pouvez maintenant configurer votre tâche dyno_ping en cliquant sur `Add Job` pour qu'elle s'exécute une fois toute les 10 min:

```
rake dyno_ping
```

C'est bon votre app reste dispo à tout moment et c'est gratuit 👍
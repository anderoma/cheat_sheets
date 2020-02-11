# Démarer avec ruby on rails 5.2
- [Migration](#migration-)
- [Insérer une Image](#insérer-une-image-)
- [Ajouter un thème](#ajouter-un-thème-)

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

- Pour créer un <strong>model</strong> User <strong>(User au Singulier)</strong>:
```shell
rails g model User name:string email:string 
```

- Créer la base de donnée :
```shell
rails db:create 
````

- Création de la table avec les critères ci-dessus :
```shell
rails db:migrate
````

- Pour créer le <strong>controller</strong> User <strong>(Users au Pluriel)</strong> avec deux méthode show et index :
```shell
rails g controller Users index show
```

## Migration :
- Création d'une migration :
```shell
rails generate migration nom_de_ta_migration
```

- Status des migrations (te sort un joli tableau pour voir où tu en es dans tes migrations entre les up et les down)
```shell
rails db:migrate:status
```

- Passe toutes les migrations en attente <strong>(= les mets en up)</strong>
```shell
rails db:migrate
```

- Supprime une migration **(= supprime une migration, que si elle est DOWN)** :
```shell
rails d migration nom_de_ta_migration 
```

- Revient en arrière sur la dernière migration **(= la met en down)** :
```shell
rails db:rollback STEP=1
```

## Insérer une image :
```ruby
<%= image_tag "event.jpg", width: 500 %>
```

## Ajouter un thème :
Commence par télécharger le thème de ton choix.
Ajoute dans le dossier vendor les fichiers du thème (fichiers css, js, ...)
Ajouter dans `config/initializers/assets.rb`
```ruby
Rails.application.config.assets.paths << Rails.root.join('vendor')
Rails.application.config.assets.paths << Rails.root.join(‘lib')
````

Ajouter dans `app/assets/stylesheets/application.css`
```css
*= require bootstrap/bootstrap.min
```

Ajouter dans `app/assets/javascripts/application.js`
```js
*= require bootstrap/js/bootstrap.bundle.min
```


<p align="center"> 
Merci <a href="https://www.thehackingproject.org/">THP</a> ❤️ 
</p>

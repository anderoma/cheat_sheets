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

- Pour créer un model User <strong>(User au Singulier)</strong>:
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

- Pour créer le <span style="color:blue">controller</span> User <strong>(Users au Pluriel)</strong> :
```shell
rails g controller Users index show
```




<p align="center"> 
Merci <a href="https://www.thehackingproject.org/">THP</a> ❤️ 
</p>

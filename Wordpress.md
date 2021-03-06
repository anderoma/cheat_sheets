# WordPress

- [Template](#template)
- [Customization](#customization)
- [Tuto](#tuto)
- [Extensions](#extensions)
- [Securité](#securité)
- [Heroku](#heroku)

## Template
[Divi by elegant theme best page builder](https://www.elegantthemes.com/)
- https://www.elegantthemes.com/layouts/
- https://divi.express/

## Customization
- Changer le logo , page de connexion Admin :
modifier url de l'image dans wp-admin/css/login.min.css

- Changer social icon divi :
modifier le fichier wp-content/themes/Divi/includes/social_icons.php :
```php
<?php if ( 'on' === et_get_option( 'divi_show_linkedin_icon', 'on' ) ) : ?>
	<li class="et-social-icon et-social-linkedin">
		<a href="<?php echo esc_url( et_get_option( 'divi_twitter_url', '#' ) ); ?>" class="icon">
			<span><?php esc_html_e( 'Linkedin', 'Divi' ); ?></span>
		</a>
	</li>
<?php endif; ?>
```

## Tuto
- [Migrer un site WordPress all-in-one-plugin](https://www.creaweb2b.com/migrer-site-wordpress-all-in-one-wp-migration/)

## Extensions
- Yoast SEO : Pour optimiser son référencement ;
- Monarch : Pour ajouter des boutons de partage sociaux ;
- WP Super Cache : Pour accélérer le chargement de votre blog ;
- Cerber Security : Pour protéger votre site ;
- MonsterInsights : Pour connecter Google Analytics à son site ;
- All-in-One WP Migration : Exporter ou importer votre site wordpress;
- GDPR Cookie Consent Banner : Bannière cookie ;
- Really Simple SSL : Passer son site en <strong>https</strong> ;
- WP Mail SMTP : Envoie mail du Formulaire de contact plus rapide ;
- WPS Hide Login : Change ton Url de connexion ;
- Ultimate member : Meilleur extension de profil utilisateur et d'espace membre pour wordpress;

- UpdraftPlus : Pour sauvegarder son site régulièrement ;
- Loco Translate : Pour traduire votre thème ou vos extensions ;
- DeliPress: Pour envoyer des newsletters directement depuis WordPress ;



## Securité
- [securisé-wordpress](https://www.hostinger.fr/tutoriels/securiser-wordpress/)(https://kinsta.com/blog/wordpress-security/)

#### 1. Invest in Secure WordPress Hosting
www.infomaniak.com bon hébergeur avec : 
- Sauvegarde integré (Base de donneé et hébergeur) Backup facile et rapide
- Template Elegant theme
- Extension prenium integré ( Divi bulder, Monarch, Bloom)
#### 2. Use Latest PHP Version
#### 3. Supprimer les plugins et theme inutile
#### 4. Change Your WordPress Login URL
utilise le plugin [WPS Hide login](https://wordpress.org/plugins/wps-hide-login/)
#### 5. Limit Login Attempts
utilise le plugin [Cerber security](https://wordpress.org/plugins/wp-cerber/)
#### 6. Use HTTPS for Encrypted Connections
#### 7. Utilisez le htaccess à son plein potentiel
```
AuthUserFile /dev/null
AuthGroupFile /dev/null
AuthName "WordPress Admin Access Control"
AuthType Basic
<LIMIT GET>
order deny,allow
deny from all
allow from xx.xx.xx.xxx
allow from xx.xx.xx.xxx
</LIMIT>
```
[trouve ton adress ip](https://www.whatismyip.com/) 


## Heroku
- [Download your code from heroku](https://help.heroku.com/FZDDCBLB/how-can-i-download-my-code-from-heroku)

- [Crée une App Wordpress avec Heroku](https://dashboard.heroku.com/new?button-url=http%3A%2F%2Ftechnomile.github.io%2Fwordpress%2Fsetup.html&template=https%3A%2F%2Fgithub.com%2Ftechnomile%2FHeroku-WordPress)



# Nouveau projet laravel

## Créer le projet

`$ composer create-project --prefer-dist laravel/laravel projetlei`

## Dans phpMyAdmin

Créer une nouvelle base de données avec le nom correspondant.

## Dans le dossier "projetlei"

#### .env

+ `$ mv .env.example .env`

+ `$ subl .env` ou `$ vim .env`

+ Entrer les informations concernant la database ... 
..+ **DB_DATABASE** -> nom donné à la database dans PhpMyAdmin
..+ **DB_USERNAME** -> username phpMyAdmin
..+ **DB_PASSWORD** -> password phpMyAdmin

+ Enregistrer le fichier.

#### chmod

Modifier les droits sur les dossiers storage/ et bootstrap/ ...

`$ chmod -R a+w storage/ bootstrap/`

#### clé

Générer la clé d'application ...

`$ php artisan key:generate`

Et vérifier dans le fichier .env  ( **APP_KEY** )

#### initier git

`$ git init`

`$ git add .`

`$ git commit -m "premier commit"`

#### créer et basculer sur la branche develop (git-flow)

`$ gitk --all` 

`$ git checkout -b nomdelabranche` 

*checkout -b permet de basculer directement sur la nouvelle branche créée*

*nom de la branche : develop*

`$ gitk --all` pour vérifier

#### système d'authentification

`$ php artisan make:auth` 

`$ php artisan migrate` 

#### sauvegarder l'authentification

** sur la branche develop ou sur la branche master ??? **

`$ git add .`

`$ git commit -m "auth_scaffolding"`

** ... ??? **

#### merge

retourner sur la branche develop
puis git merge --no -ff nomdelabranche (vers branche nommée depuis branche courante) (ctrl^X pour quitter)
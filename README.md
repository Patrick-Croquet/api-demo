# api-demo
 API Platform Symfony
symfony new my_api_activities --version="6.0.*" --webapp

cd my_api_activities 

** composer install **
composer require api

php bin/console debug:router

symfony server:start

# Désactiver webby dans config/packages/api_platform.yaml
    show_webby: false

# Création de la base de données
php bin/console doctrine:database:create   

php bin/console make:user

Next: When you're ready, create a migration with 
php bin/console make:migration

Then: Run the migration with 
php bin/console doctrine:migrations:migrate

php bin/console make:entity

 Class name of the entity to create or update (e.g. GentleKangaroo): > detail

 Mark this class as an API Platform resource (expose a CRUD API for 
it) (yes/no) [no]:
 > yes

# Fixtures user
composer require doctrine/doctrine-fixtures-bundle --dev
php bin/console doctrine:fixtures:load

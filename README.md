# api-demo
 API Platform Symfony

composer create-project symfony/skeleton api-demo

composer require api

# Créer la base de données
php bin/console doctrine:database:create
php bin/console doctrine:schema:create

composer require symfony/maker-bundle --dev

php bin/console make:entity Post

symfony serve -d
http://127.0.0.1:8000/api

php bin/console make:migration
php bin/console doctrine:migrations:migrate

php bin/console make:entity Category
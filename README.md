-setup
symfony new testingapp --webapp
composer require maker 
symfony console make:controller dashboard


-security
composer require symfony/security-bundle
symfony console security:hash-password

-migration
symfony console make:migration


-doctrine
symfony console doctrine:database:create
symfony console doctrine:database:drop --force
symfony console doctrine:fixtures:load --append (safe)
symfony console doctrine:fixtures:load
symfony console doctrine:migrations:migrate
symfony console make:crud

-forms
symfony console make:registration-form
symfony console make:user
symfony console make:auth 

-fixtures
composer require --dev doctrine/doctrine-fixtures-bundle
symfony console make:fixture AdminFixture


-docker 
docker compose up -d
docker compose down -v
docker ps

-email
composer require symfonycasts/verify-email-bundle


-cache 
symfony console cache:clear



-api
composer require api symfony/orm-pack doctrine/doctrine-migrations-bundle
composer require symfony/maker-bundle --dev
composer require api

-jwt
composer require lexik/jwt-authentication-bundle
symfony console lexik:jwt:generate-keypair

-Oauthbundle 
composer require knpuniversity/oauth2-client-bundle
composer require league/oauth2-google

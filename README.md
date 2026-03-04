
# Symfony Full Setup - All Commands

```bash
# --------------------
# Setup Project
# --------------------
symfony new yourAppName --webapp
composer require maker
symfony console make:controller DashboardController

# --------------------
# Docker
# --------------------
docker compose up -d
docker compose down -v
docker ps

# --------------------
# Database Tables
# --------------------
php bin/console make:entity 
symfony console make:crud

# --------------------
# Migration
# --------------------
symfony console make:migration
symfony console docktrine:migrations:migrate

# --------------------
# Doctrine
# --------------------
symfony console doctrine:database:create
symfony console doctrine:database:drop --force
symfony console doctrine:fixtures:load --append   # safe
symfony console doctrine:fixtures:load
symfony console doctrine:migrations:migrate

# --------------------
# Forms & Authentication
# --------------------
symfony console make:registration-form
symfony console make:user
symfony console make:auth

# --------------------
# Fixtures
# --------------------
composer require --dev orm-fixtures #shortcut
composer require --dev doctrine/doctrine-fixtures-bundle
symfony console make:fixture YourFixture

# --------------------
# Email Verification
# --------------------
composer require symfonycasts/verify-email-bundle

# --------------------
# Security
# --------------------
composer require symfony/security-bundle
symfony console security:hash-password

# --------------------
# Cache
# --------------------
symfony console cache:clear

# --------------------
# API Setup
# --------------------
composer require api symfony/orm-pack doctrine/doctrine-migrations-bundle
composer require symfony/maker-bundle --dev
composer require api

# --------------------
# JWT Authentication
# --------------------
composer require lexik/jwt-authentication-bundle
$env:OPENSSL_CONF="C:\Program Files\Git\usr\ssl\openssl.cnf"  
symfony console lexik:jwt:generate-keypair

# --------------------
# OAuth Bundle
# --------------------
composer require knpuniversity/oauth2-client-bundle
composer require league/oauth2-google

# --------------------
# https/http error
# --------------------
symfony serve --no-tls

# --------------------
# Running and Stopping
# --------------------
symfony serve
symfony server:start
symfony server:stop
symfony server:stop --all

# --------------------
# csrf no secret keys error
# --------------------
php bin/console secrets:generate-keys

```


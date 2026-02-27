```symfony
# Symfony Full Setup - All Commands

```bash
# --------------------
# Setup Project
# --------------------
symfony new testingapp --webapp
composer require maker
symfony console make:controller DashboardController

# --------------------
# Security
# --------------------
composer require symfony/security-bundle
symfony console security:hash-password

# --------------------
# Migration
# --------------------
symfony console make:migration

# --------------------
# Doctrine
# --------------------
symfony console doctrine:database:create
symfony console doctrine:database:drop --force
symfony console doctrine:fixtures:load --append   # safe
symfony console doctrine:fixtures:load
symfony console doctrine:migrations:migrate
symfony console make:crud

# --------------------
# Forms & Authentication
# --------------------
symfony console make:registration-form
symfony console make:user
symfony console make:auth

# --------------------
# Fixtures
# --------------------
composer require --dev doctrine/doctrine-fixtures-bundle
symfony console make:fixture AdminFixture

# --------------------
# Docker
# --------------------
docker compose up -d
docker compose down -v
docker ps

# --------------------
# Email Verification
# --------------------
composer require symfonycasts/verify-email-bundle

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
```


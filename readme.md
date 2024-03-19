# Technical test for HelloCSE

Hi. You'll find in this repository my work for HelloCSE technical test.

## Structure

- /backend (git submodule)
    - Laravel 10.X Application
- /frontend (git submodule)
    - Nuxt 3.X Application

## Instructions

### Backend

- You need PHP ^8.1
- You need following php extensions (php.ini)
    * gd
    * curl
    * fileinfo
    * openssl
    * pdo_sqlite
    * sqlite3
    * zip
- You need Composer

```bash
# Copy .env
mv .env.example .env

# Intall dependencies
composer install

# Generate app key
php artisan key:generate

# Migrate db
php artisan migrate

# (optional) run tests
php artisan test

# Start app on port 8000
php artisan serve
```

### Frontend

- You need nodejs 18 with npm

```bash
# Copy .env
mv .env.example .env

# Install dependencies
npm i

# (For production) Build app then you'll be able to launch (https://nuxt.com/docs/getting-started/deployment#entry-point)
npm run build 
node .output/server/index.mjs

# (Dev mode) Start command dev
npm run dev
```
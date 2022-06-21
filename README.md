# LEMP-Stack-Docker

Docker has become a frequently used solution for deploying applications thanks to how it simplifies running and deploying applications in ephemeral containers. When you are using a LEMP application stack, for example, with PHP, Nginx, MariaDB and the Laravel framework, Docker can significantly streamline the setup process.

## Version

## V.1 | Require Laravel Framework v9.x

> PHP v8.1-fpm\
> Nginx v1.21-alpine\
> MariaDB v10.8

## V.2 | Require Laravel Framework v9.x

> PHP v8.1-fpm\
> Nginx v1.21-alpine\
> MariaDB v10.8\
> phpMyAdmin v5.2

## Laravel Installation Via Composer

```bash
composer create-project laravel/laravel example-app

cd example-app
```

## Setting up .env.example file

> APP_NAME=Laravel\
> APP_ENV=local\
> APP_KEY=\
> APP_DEBUG=true\
> APP_URL=http://localhost:8100

> DB_CONNECTION=mysql\
> DB_HOST=db\
> DB_PORT=3306\
> DB_DATABASE=laravel\
> DB_USERNAME=root\
> DB_PASSWORD=

## Running Docker

```bash
cp .env.example .env

docker-compose up -d

docker-compose exec app bash

php artisan key:generate
```

## Running Migrations

Run all of your outstanding migrations with seeder:

```bash
php artisan migrate --seed
```

If you would like to see which migrations have run thus far:

```bash
php artisan migrate:status
```

Roll back the latest migration operation. This command will rolls back the last "batch" of migrations, which may include multiple migration files:

```bash
php artisan migrate:rollback
```

Roll back all of your application's migrations:

```bash
php artisan migrate:reset
```

If you want to drop all table before seeding, you can use this command:

```bash
php artisan migrate:fresh --seed
```

## License

[MIT](https://choosealicense.com/licenses/mit/)

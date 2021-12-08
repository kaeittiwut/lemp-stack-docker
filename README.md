# LEMP-Stack-Docker

Docker has become a frequently used solution for deploying applications thanks to how it simplifies running and deploying applications in ephemeral containers. When you are using a LEMP application stack, for example, with PHP, Nginx, MariaDB and the Laravel framework, Docker can significantly streamline the setup process.

## Version

### V.1

> Nginx v1.21.x\
> MariaDB v10.5.x\
> PHP v7.4-fpm\
> Laravel Framework v8.x

### V.2

> Nginx v1.21.x\
> MariaDB v10.5.x\
> PHP v7.4-fpm\
> Laravel Framework v8.x\
> phpMyAdmin v5.1.x

## Install all dependencies and migrate database

```bash
$ cp .env.example .env

$ composer install

$ php artisan key:generate

$ php artisan migrate --seed

$ php artisan serve
```

## Running Migrations

Run all of your outstanding migrations with seeder:

```bash
$ php artisan migrate --seed
```

If you would like to see which migrations have run thus far:

```bash
$ php artisan migrate:status
```

Roll back the latest migration operation. This command will rolls back the last "batch" of migrations, which may include multiple migration files:

```bash
$ php artisan migrate:rollback
```

Roll back all of your application's migrations:

```bash
$ php artisan migrate:reset
```

If you want to drop all table before seeding, you can use this command:

```bash
$ php artisan migrate:fresh --seed
```

## License

[MIT](https://choosealicense.com/licenses/mit/)

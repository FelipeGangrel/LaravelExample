## Database

Before creating or running a migration, run the artisan command to create the migrations table

```sh
$ php artisan migrate:install
```

## Using Docker

If you are using Docker with a different docker-compose.yml file, please make sure to add
a link between the webserver and database services

```yml
...
services:
    webserver:
        ...
        links:
            - <name_of_your_database_service>
    name_of_your_database_service:
        ...

```

And on your .env file, set the DB_HOST variable as follows

DB_HOST=<name_of_your_database_service>

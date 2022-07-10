# Docker Laravel 9 Dev environments
[This docker compose file](docker-compose.yml) is made for Laravel setups that are present in an folder called ```backend```
and a frontend (like vue for example) in the ```frontend``` folder.
It provides the following containers:
- Mysql 8
- Php 8.1
- Node.js + Dart Sass
- Mailhog

# How to use
Clone this repo. And in the root folder, you need to make 2 folders called ```backend``` and ```frontend```.
In the backend folder you'll need to put your Laravel project. In the ```frontend``` folder, a vue project for example.

## Command setup.
If you look inside the [docker compose file](docker-compose.yml), you'll see that the php service will run ```php artisan serve``` in the backend folder.
This wil, like normal start Laravel's development server.

In that same file you'll see that the node image runs ```npm run serve```. In vue setups this will
start another server, just for vue. Feel free to modify those commands to suit your needs.

## Docker compose
Make sure you have docker installed and run ```docker compose up``` in this directory.

## Laravel environment setup
Make sure that at least these codes are present in your .env file 

```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=docker
DB_USERNAME=docker
DB_PASSWORD=secret
```

```
MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
```


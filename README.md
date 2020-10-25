# README

## Introduction

Docker environment for AMP project: `httpd:latest`, `php:7.4-fpm`, `mysql:8.0.19`, `phpmyadmin/phpmyadmin:latest`.

Installed PHP extensions: `pdo_mysql`, `intl`, `opcache`, `gd`, `bcmath`, `mysqli`, `xdebug`.

## Config

Open `.env` file to change your project name / Web Port / PMA Port / MySQL Password.

When you change `COMPOSE_PROJECT_NAME` value in `.env` file, please also change `ProxyPassMatch` value in `conf/apache/httpd.conf` file to match with new PHP container name.

## Start / Stop

Create containers: `docker-compose up -d`.

Remove containers: `docker-compose down --remove-orphans`.

Start containers: `docker-compose start`.

Stop containers: `docker-compose stop`.

## Rebuild

After you changed content of `php.dockerfile`, you need to rebuild image before restart containers with command: `docker-compose build`.


## Source

Just put your project in `src` folder.

## pimcore-dock
- this is a docker / docker-compose environment to run pimcore5 prealpha

## prerequisites
- linux 
- installed docker
- installed docker-compose version 2 (>1.6)
- composer

## usage
- clone project

```sh
docker-compose-up -d
```
- change to 
```sh
composer install
```

## create database
- login to mysql container and create database 
```sh
docker exec-it pimcore-doc-mysql /bin/bash
mysql -u root -p
CREATE DATABASE pimcore charset=utf8mb4;
```



- surf to http://localhost:8181/install.php
- type in your databaseconfig:
user: root
pass: root
database: pimcore

Thats it.

Please note, to change your databaseconnection to your credentials.
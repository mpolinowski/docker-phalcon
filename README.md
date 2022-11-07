# Phalcon Framework with Docker

> Based on [Working with Phalcon Framework and Docker](https://medium.com/@rogsilva/working-with-phalcon-framework-and-docker-fef3fe5b85c8) by [Rogério Silva](https://medium.com/@rogsilva).


## Build

```bash
docker pull mariadb:latest
docker pull webdevops/php-nginx:7.4
mkdir html
docker-compose build app
```


## Run the Service

```bash
docker-compose up -d
```


## Configure the Phalcon App

Initialize the application by generating a `composer.json`:

```bash
docker exec -ti phalcon_app composer init
```

Create a default Phalcon project using the [Phalcon Devtools](https://github.com/phalcon/phalcon-devtools):


```bash
docker exec -ti phalcon_app composer require --dev phalcon/devtools
```


```bash
docker exec -ti phalcon_app ./vendor/bin/phalcon project application simple
```
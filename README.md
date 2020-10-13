## Introduction

Build a simple laravel development environment with docker-compose.
*git remote set-url 

## Usage

```bash
$ git clone https://github.com/gekiwason/laravel-project.git
$ cd laravel-project
$ docker-compose up -d
$ docker-compose exec app bash
$ composer create-project --prefer-dist "laravel/laravel=[version]" my-laravel-app
$ cd my-laravel-app
$ cp ../docker/laravel/.env .env
$ chmod 777 -R storage/ 
$ php artisan key:generate && php artisan config:cache && php artisan migrate 
$ exit
$ docker-compose down && docker-compose up -d
```

## EC2

```bash
#!/bin/bash
sudo yum update -y
sudo yum install -y docker
sudo service docker start
sudo chkconfig docker on
sudo usermod -a -G docker ec2-user
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo yum install -y git
```

## Container structure

```bash
├── web
├── app
├── mysql
└── phpmyadmin
```

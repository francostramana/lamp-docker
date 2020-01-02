# Docker LAMP Web Server

Simple LAMP Web Server using multiple containers.

## Services

* PHP 7.0 & Apache Web Server (php:7.0-apache)
* MYSQL (mysql:latest)
* PHPMyAdmin (phpmyadmin/phpmyadmin)
* Adminer (adminer)

## Usage

The app must be in the same directory level that this repo. 

```
app
|_ /lamp-server-docker
|_ hello_world.php
```

Run compose command inside *repo folder* (sudo is probably required)

```
docker-compose up
```

Open `localhost:8080` and walah :)

### MySQL Access
These are the database access data. These can be changed from *.yml* file.

```
MYSQL_HOST: mysqldb
MYSQL_ROOT_PASSWORD: root
```

For example, if you want to connect from PHP using PDO:

```
$this->db_connection = new PDO('mysql:host=mysqldb;dbname=db_name;charset=utf8', 'root', 'root');
```

## Database Management 
Both database managers are exposed in different ports:

* PHPMyAdmin: `localhost:8081`
* Adminer: `localhost:8083`



This project was created for educational purposes. Any contribution is welcome!

Happy coding! 💙
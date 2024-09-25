# Laravel Application Setup Guide

# Project Overview

Laravel is a free, open-source PHP web framework designed to make web development more efficient and enjoyable. It was created by Taylor Otwell in 2011 and follows the Model-View-Controller (MVC) architectural pattern. Laravel provides a robust set of tools and features to simplify tasks such as routing, authentication, session management, caching, and database interactions. Here's an overview of its main features:

# prerequisites

Before you begin, ensure you have the following installed on your Linux system:

* Update your package list and install curl and git

```bash
sudo apt update
sudo apt install curl git -y
```

## How to Set Up and Run the Laravel Application

* Clone the repository

```bash
https://github.com/rsingh0706/Laravel.git
```

## Linux Essentials

Update your package list and install need Lamp server

1. Install Nginx the process depends on the operating system you're using. Below are   the steps

* Update the package list

```bash
sudo apt update
```
* Install Nginx

```bash
sudo apt install nginx
```
* Start and enable Nginx

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```
* Verify Nginx is running

```bash
sudo systemctl status nginx
```

2. install a database server on Ubuntu, the steps depend on which database you want    to use. 

* Update your Package Index

```bash
sudo apt update
```
* Install MySQL server:

```bash
sudo apt install mysql-server
```
* Start and enable MySQL service:

```bash
sudo systemctl start mysql
sudo systemctl enable mysql
```

* Run the MySQL security script

```bash
sudo mysql_secure_installation
```
* Check MySQL status:

```bash
sudo systemctl status mysql
```
* password reset 

```bash 
sudo mysql -u root -p
```

```bash
ALTER USER 'root'@'localhost' IDENTIFIED BY 'new_password';
FLUSH PRIVILEGES;
```

3. Install PHP on an Ubuntu system, follow these steps:

* Start by ensuring your package manager is up to date.

```bash
sudo apt update
```

* install PHP

```bash
sudo apt install php-fpm php-mysql php-curl php-gd php-xml php-mbstring php-xmlrpc php-soap php-intl php-zip -y
```
* Start and enable PHP

```bash
sudo systemctl start php7.4-fpm
sudo systemctl enable php7.4-fpm
```
* Verify PHP is running

```bash
sudo systemctl status php7.4-fpm
```
* Verify PHP Installation

```bash
php -v
```
* Finally restart Nginx

```bash
sudo systemctl restart nginx
```
* Configure Web Server 
If you're using a web server Nginx, you'll need to install PHP integration modules.

```bash
location ~ \.php$ {
    include snippets/fastcgi-php.conf;
    fastcgi_pass unix:/run/php/php8.1-fpm.sock;
}
```
* Testing PHP with a Web Server

```bash
sudo /var/www/html/index.php
```
* Add the following PHP code to the file:

* Finally restart Nginx

```bash
sudo systemctl restart nginx
```


# VLEMP - Vagrant LEMP

## Overview
This is a seeder to build a simple **L**inux **E**ngine x (nginx) **M**ySQL **P**HP Vagrant stack for development.

The goal of this project is to create a virtual machine that can be installed once and reused by any number of PHP applications.

## Included Software

 * [Ubuntu](http://ubuntu.com/) 14.04
 * [PHP5-FPM](http://php-fpm.org/)
 * [MCrypt](http://mcrypt.sourceforge.net/)
 * [Composer](https://getcomposer.org/)
 * [Nginx](http://nginx.org/)
 * [MySQL](https://www.mysql.com/)
 * [Sqlite](http://www.sqlite.org/)
 * [Redis](http://redis.io/)
 * [RabbitMQ](https://www.rabbitmq.com/)
 * [NodeJS](https://nodejs.org/)
 * [Bower](http://bower.io/)
 * [Grunt](http://gruntjs.com/)
 * [Gulp](http://gulpjs.com/)

## Requirements

* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](http://www.vagrantup.com/)

## Installation

  1. Confirm the requirements above are installed.
  2. Clone this repo by opening a terminal:
    $ cd /path/you/want/to/develop/in
    $ git clone https://github.com/dereknutile/lemp-vagrant
    $ cd lemp-vagrant
  3. Provision and boot the vagrant server:
    $ `vagrant up`
  4. Once the server is provisioned and running, visit the test page: [http://localhost:8080](http://localhost:8080).

## Default MySQL Database

User: `root`
Password: `root`
Database: `appdb`

## Accessing your server

  1. Open a terminal:
    $ cd /path/to/your/lemp-vagrant/
    $ vagrant ssh

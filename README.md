# SMR Lamp Setup

This is a basic LAMP stack environment built using Docker Compose. It consists of the following:

* PHP 7.1
* Apache 2.4
* MySQL 5.7
* phpMyAdmin

## Installation

Clone this repository. Run the `docker-compose up -d`.

```shell
git clone git@gitlab.com:schumacher-visuell/smr_lamp_setup.git
cd smr-lamp-setup/
docker-compose up -d
```

Your LAMP stack is now ready to go!! You can access it via `http://localhost`.

## CMS

In `./www/cms` you can add your chosen CMS and access it via apache. The Document root is currently configured to look at `./www` but you can change this if you like in the `docker-compose.yml` file.

## Web Server

Apache is configured to run on port 80. So, you can access it via `http://localhost`.

#### Apache Modules

By default the following modules are enabled.

* rewrite

> If you want to enable more modules, just update `./bin/webserver/Dockerfile`.
> You have to rebuild the docker image by running `docker-compose build` and restart the docker containers.

## PHP

The installed version of PHP is 7.1.

#### Extensions

By default the following extensions are installed.

* mysqli
* mbstring
* zip
* intl
* mcrypt
* curl
* json
* iconv
* xml
* xmlrpc
* gd

> If you want to install more extension, just update `./bin/webserver/Dockerfile`.
> You have to rebuild the docker image by running `docker-compose build` and restart the docker containers.

## phpMyAdmin

phpMyAdmin is configured to run on port 8080. Use the following default credentials.

http://localhost:8080/  
username: root  
password: root

# linux-server-config-project
The purpose of this project is to learn how to set up and configure a linux server to host a web application using Amazon Lightsail.

The application that will be hosted on this server is my [catalog-project](https://github.com/Justin-Tadlock/catalog-project).

## Server Configuration
#### Server Applications
The following packages have been installed using apt-get:
* apache2
* libapache2-mod-wsgi
* libapache2-mod-wsgi-py3
* postgresql
* postgresql-contrib
* python3-dev 
* python3-pip 
* python3-venv
* libpq-dev

#### Python3 Configuration
The following packages have been installed using pip:
1. setuptools
2. wheel
2. flask

#### General Settings Configuration
* Made three users for the server.
* Disabled remote root login access
  Added public keys for key authentication access where appropriate.
* Enabled key authentication only access
* Removed the default 'ubuntu' user that is made by Amazon LightSail
* Created UFW rules for SSH, HTTP, NTP connections
* Configured a non-default port for SSH connections
* Configured apache2 to host WSGI applications via the WSGIScriptAlias with python3
* Configured PostgreSQL to provide the hosted application CRUD functionality
* Updated files in catalog-project to work with WSGI hosting


## Accessing the Server
The server IP is: 34.198.251.47
The domain the server is mapped to is: [catalog.justin-tadlock.com](catalog.justin-tadlock.com)

This IP address/domain will be used to browse the application.


## Authors

* **[Justin-Tadlock](https://github.com/Justin-Tadlock)** - *Initial work*


## Acknowledgments
* [Set up PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04)
* [Deploying Flask Application with WSGI server using apache2 on AWS Cloud Ubuntu Machine](https://medium.com/@satyavinay456/deploying-flask-application-using-wsgi-server-with-apache2-on-aws-cloud-ubuntu-machine-b7a15ca25cff)

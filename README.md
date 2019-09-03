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
* python3-virtualenv

#### Python3 Configuration
The following packages have been installed using pip:
1. setuptools
2. wheel
2. flask

#### General Settings Configuration
* Made two users for the server.
  Added public keys for key authentication access.
* Removed the default 'ubuntu' user that is made by Amazon LightSail
* Disabled remote root login access
* Enabled key authentication only access
* Created UFW rules for SSH, HTTP, NTP connections
* Configured a non-default port for SSH connections
* Configured apache2 to host WSGI applications via the WSGIScriptAlias with python3
* Configured PostgreSQL to provide the hosted application CRUD functionality


## Accessing the Server
The server IP is: 34.198.251.47

This IP address will be used ot browse the application.


## Authors

* **[Justin-Tadlock](https://github.com/Justin-Tadlock)** - *Initial work*


## Acknowledgments
* [Set up PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04)
* [Configure Ubuntu 18.04 for Python3 and Flask](https://www.fullstackpython.com/blog/python-3-flask-gunicorn-ubuntu-1804-bionic-beaver.html)

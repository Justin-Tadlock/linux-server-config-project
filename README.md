# linux-server-config-project
The purpose of this project is to learn how to set up and configure a linux server and host a web application using it with Amazon Lightsail.

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
* postgresql-client 
* postgresql-client-common
* virtualenv

#### Python3 Configuration
The following is the pip list:
* bleach==3.1.0
* cachetools==3.1.1
* certifi==2019.6.16
* chardet==3.0.4
* Click==7.0
* Flask==1.0.2
* google-auth==1.6.3
* idna==2.8
* itsdangerous==1.1.0
* Jinja2==2.10.1
* MarkupSafe==1.1.1
* psycopg2==2.8.3
* pyasn1==0.4.7
* pyasn1-modules==0.2.6
* requests==2.22.0
* rsa==4.0
* six==1.12.0
* SQLAlchemy==1.3.6
* urllib3==1.25.3
* webencodings==0.5.1
* Werkzeug==0.15.5


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
The SSH Port is: 2200

NOTE: The domain the server is also mapped to: 
* [catalog.justin-tadlock.com](http://catalog.justin-tadlock.com)

This IP address/domain will be used to browse the application.


## Authors

* **[Justin-Tadlock](https://github.com/Justin-Tadlock)** - *Initial work*


## Acknowledgments
* [Set up PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04)
* [Deploying Flask Application with WSGI server using apache2 on AWS Cloud Ubuntu Machine](https://medium.com/@satyavinay456/deploying-flask-application-using-wsgi-server-with-apache2-on-aws-cloud-ubuntu-machine-b7a15ca25cff)
* [Global Variables with WSGI hosted applications](https://www.pythonanywhere.com/forums/topic/3801/)

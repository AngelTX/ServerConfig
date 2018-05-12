# Linux Server Configuration

##### Access

  ```
    IP Address:18.191.85.1
    SSH Port: 2200
  ```

### Summary of Changes Made
#### Port:
* changed default port to 2200.

#### Fire Wall Settings

* Block all incoming connections.
* Allow all outgoing connections
* Allow SSH
* Set firewall to allow default HTTP (port 80) connections.
* Allow connections to port 2200
* Allow NTP
* Deny default SSH (from 22)
* Enabled firewall with the above modifications.

#### Created User: Grader

* user: grader
* password: udacity
* Has sudo access
* Authentication with public key encryption enabled.
* PKE passphrase: udacity

#### Applications Installed

* Apache2
* mod_wsgi
* PostgreSQL

#### PostgreSQL Configuration

* By default, remote connections are disabled.
* Created database user `catalog`
* set a password for `catalog`: `udacity`
* catalog has sudo access.
* created a database and assigned it to catalog

#### eSports App Setup
* Installed git
* Cloned repository `https://github.com/AngelTX/CatalogProject` into my `/var/www/` directory.
* Installed the following programs:
* flask
* httplib2
* sqlalchemy
* requests
* oauth2client
* psycopg2
* google
* google_auth_oauthlib
* Changed application to __init__.py

#### Virtual Host

* created `esports.conf` file under the `/etc/apache2/sites-avaiable/` directory
* Updated the contents of the config file to run my application.
* created a wsgi file and configured to run my application

### Third Party Resources
* [PostgreSQL Docs](https://www.postgresql.org/docs/9.4/static/index.html)
* [Flask Docs](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/#working-with-virtual-environments)
* [SQLAlchemy Docs - Engine Configuration](http://docs.sqlalchemy.org/en/latest/core/engines.html)
* [Digital Ocean - How To Secure PostgreSQL on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps#do-not-allow-remote-connections)
* [Digital Ocean - How To Use Roles and Manage Grant Permissions in PostgreSQL on a VPS](https://www.digitalocean.com/community/tutorials/how-to-use-roles-and-manage-grant-permissions-in-postgresql-on-a-vps--2#how-to-log-in-as-a-different-user-in-postgresql)
* [Digital Ocean - An Introduction to Linux Permissions](https://www.digitalocean.com/community/tutorials/an-introduction-to-linux-permissions)
* [Digital Ocean - How To Deploy a Flask Application on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
* [Digital Ocean - How To Configure SSH Key-Based Authentication on a Linux Server](https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server)
* [Ubuntu Docs - Changing the Timezone](https://help.ubuntu.com/community/UbuntuTime)
* [Amazon Lightsail Docs](https://aws.amazon.com/documentation/lightsail/)

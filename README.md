# Linux Server Configuration

## Server Information
* IP Address - 34.236.148.127
* ssh port - 2200
* URL to application - http://34.236.148.127

## Software Installed
* Apache 2.4
* libapache2-mod-wsgi 4.3
* Postgresql 9.5
* git 2.7
* Flask 0.12
* SQLAlchemy 1.1.15

## Configurations
* Apache has been configured to use mod_wsgi and point to myapp.wsgi in the html directory.
* myapp.wsgi imports the catalog application from a directory not served by the apache web server.
* ssh connections are accepted on port 2200 not port 20.
* All users are required to use ssh keys.
* Remote root login has been disabled.
* The ufw firewall will allow incoming requests to ports 80, 123 and 2200 only.
* All server packages have been upgraded.
* User 'catalog' has been created in Postgresql with limited permissions to the tables used by the the catalog application. The catalog application uses this account.

## Notes
Notes from the Udacity classes were used for most of the work.  I referred to Flask documentation for help with the mod_wsgi configuration.  Postgresql documentation was used to help with permissions for the catalog user.  stackoverflow.com was used to fill in information I could not find in the documentation.

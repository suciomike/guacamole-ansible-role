# guacamole-ansible-role
Ansible role to install and configure Guacamole with MySQL/MariaDB


Requirements
------------
* centos/rhel 7
* ansible >= 2.9

Installation
------------
```
$ ansible-galaxy install suciomike.guacamole-ansible-role
```


Role Variables
--------------
Some variables that require review:
- `guacamole_version`: Guacamole version to be installed. Currently, latest version is "1.1.0".
- `guacamole_mysql_root_password`: Password for root user to be created for local mariadb installation. For existing installation, just enter the password of user "root".
- `guacamole_db_name`: Database name used by guacamole. Default is "guac_db".
- `guacamole_db_username`: Database user used by guacamole. Default is "guac_user".
- `guacamole_db_password`: Database user password used by guacamole. Default is "PASSword1234".
- `guacamole_configure_firewalld`: If set to "True", firewalld will be installed and properly configured. Default value is "True".



Usage
-----
After installation, point your browser to: `http://IP_or_FQDN:8080/(whatever you name guacamole)`  
Default username and password is: `guacadmin`  
*(Don't forget to change it)*

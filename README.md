# P5
# ip : 52.37.44.87
# http://ec2-52-37-44-87.us-west-2.compute.amazonaws.com
# the full url may not work due to your local dns
# software installed: postgresql python-psycopg2, python-flask python-sqlalchemy, python-pip, bleach, oauth2client, requests, httplib2, redis, passlib, itsdangerous, flask-httpauth
# apache conf:
"""
<VirtualHost *:80>
        ServerName http://ec2-52-37-44-87.us-west-2.compute.amazonaws.com/
        ServerAdmin linmao.project@gmail.com
        WSGIScriptAlias / /var/www/catalogweb/catalogweb.wsgi
        <Directory /var/www/catalogweb/catalogweb/>
            Order allow,deny
            Allow from all
        </Directory>
        Alias /static /var/www/catalogweb/catalogweb/static
        <Directory /var/www/catalogweb/catalogweb/static/>
            Order allow,deny
            Allow from all
        </Directory>
        ErrorLog ${APACHE_LOG_DIR}/error.log
        LogLevel warn
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
"""

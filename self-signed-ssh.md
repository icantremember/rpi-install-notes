generate the self signed certificate

````sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/apache-selfsigned.key -out /etc/ssl/certs/apache-selfsigned.crt````

Configure Your Web Server:
For Apache:
Enable the SSL Module.
Code

    sudo a2enmod ssl
Edit the SSL Configuration: Create or modify a virtual host configuration file for SSL (e.g., /etc/apache2/sites-available/default-ssl.conf).
Code
```
    <VirtualHost *:443>
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined

        SSLEngine on
        SSLCertificateFile /etc/ssl/certs/apache-selfsigned.crt
        SSLCertificateKeyFile /etc/ssl/private/apache-selfsigned.key
    </VirtualHost>
```

Enable the SSL Virtual Host.
Code
```
    sudo a2ensite default-ssl.conf
```
Restart Apache.
Code
```
    sudo systemctl restart apache2
```

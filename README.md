# rpi-nextcloud-install-notes

from
https://raspberrytips.com/install-nextcloud-raspberry-pi/

Install preqs:  
```sudo apt install apache2 mariadb-server libapache2-mod-php```  
```sudo apt install php-gd php-json php-mysql php-curl php-mbstring php-intl php-imagick php-xml php-zip```  
```sudo apt install php-apcu php-memcached php-redis php-gmp```

```sudo service apache2 restart```  

```wget https://download.nextcloud.com/server/releases/latest.zip```  

Unzip latest.zip into /var/www/html as root  

```sudo chmod 750 nextcloud -R```  
```sudo chown www-data:www-data nextcloud -R```  

Create the db:    
```mike@raspberrypi:/var/www/html $ sudo mysql```  
Welcome to the MariaDB monitor.  Commands end with ; or \g.  
Your MariaDB connection id is 31  
Server version: 10.11.11-MariaDB-0+deb12u1 Debian 12   
Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.  
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.  
MariaDB [(none)]> CREATE USER 'nextcloud' IDENTIFIED BY 'passwd';  
Query OK, 0 rows affected (0.016 sec)  
MariaDB [(none)]> CREATE DATABASE nextcloud;  
Query OK, 1 row affected (0.000 sec)  
MariaDB [(none)]> GRANT ALL PRIVILEGES ON nextcloud.* TO 'nextcloud'@localhost IDENTIFIED BY 'passwd';  
Query OK, 0 rows affected (0.014 sec)  
MariaDB [(none)]> FLUSH PRIVILEGES;  
Query OK, 0 rows affected (0.001 sec)  
MariaDB [(none)]>   

http://192.168.68.142/nextcloud/index.php  


wait a few minutes  

if redirect doesn't work, go to  
http://192.168.68.142/nextcloud/index.php/core/apps/recommended  

change php stuff  
```nano /etc/php/8.2/apache2/php.ini```  
change php memory limit to 2G  
change output_buffering to 0  
upload_max_filesize = 2G   
post_max_size = 4G  
interned_strings_buffer = 16  

extra php modules:  
moved above to preqs

cron job:  
```crontab -u www-data -e```  
*/5  *  *  *  * php -f /var/www/html/nextcloud/cron.php  

occ commands:  
```sudo -u www-data php /var/www/html/nextcloud/occ maintenance:mode --on```  
occ files:scan --all  



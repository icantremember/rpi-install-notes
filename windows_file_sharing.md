# Samba

from https://pimylifeup.com/raspberry-pi-samba/  

# Install samba from apt
```sudo apt install samba``` will install a bunch of stuff, make sure it includes samba-common-bin

under the [homes] section, change  
```browsable = yes```  
```read only = no```  

restart the samba service  
```sudo systemctl restart smbd```

add *your* user to smb  
```sudo smbpasswd -a youractualuser```

check to make sure the user was added  
```sudo pdbedit -L``` add -v for verbose  

add your user to the www-data group so you can access nextcloud data  
```sudo usermod -a -G www-data mike```

add a section to smb.conf for your files
```
[instantuploads]
path = /mnt/nextcloud_data/data/mikep/files/
readonly = yes
browsable = yes
public = no
```

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


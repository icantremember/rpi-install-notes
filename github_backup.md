getgits.sh  
```
#!/bin/bash

rm -rf /mnt/nextcloud_data/github_backups/*

cd /mnt/nextcloud_data/github_backups

git clone https://github.com/icantremember/rpi-install-notes/

git clone https://github.com/icantremember/minecraft_stuff
 
git clone https://github.com/icantremember/texts

git clone https://github.com/icantremember/needful_things
```

cron entry:  
```0 2 * * * /usr/local/bin/getgits.sh```

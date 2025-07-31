# raspiBackup

https://github.com/framps/raspiBackup

https://www.linux-tips-and-tricks.de/en/


# compress, archive, split
```tar cz my_large_file_1 my_large_file_2 | split -b 1024MiB - myfiles_split.tgz_```

```tar cz /mnt/nextcloud_data/backups/raspberrypi/raspberrypi@debian12-rsync-backup-20250730-040053 | split -b 1024MiB - rpi_backup_20250730.tgz_```

# uncompress
```cat myfiles_split.tgz_* | tar xz```

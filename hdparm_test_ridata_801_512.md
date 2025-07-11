```
mike@raspberrypi:~ $ sudo hdparm -TtIv /dev/nvme0n1

/dev/nvme0n1:
 readonly      =  0 (off)
 readahead     = 256 (on)
 geometry      = 488386/64/32, sectors = 1000215216, start = 0
 Timing cached reads:   10788 MB in  2.00 seconds = 5400.02 MB/sec
 Timing buffered disk reads: 1194 MB in  3.01 seconds = 396.97 MB/sec
mike@raspberrypi:~ $ sudo hdparm -Tt /dev/nvme0n1

/dev/nvme0n1:
 Timing cached reads:   11646 MB in  2.00 seconds = 5830.51 MB/sec
 Timing buffered disk reads: 1192 MB in  3.01 seconds = 396.64 MB/sec
mike@raspberrypi:~ $ sudo hdparm -Tt /dev/nvme0n1

/dev/nvme0n1:
 Timing cached reads:   12646 MB in  2.00 seconds = 6331.37 MB/sec
 Timing buffered disk reads: 1194 MB in  3.01 seconds = 397.20 MB/sec


```

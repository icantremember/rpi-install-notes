```
mike@raspberrypi:~ $ sudo hdparm -TtIv /dev/sda

/dev/sda:
 multcount     =  0 (off)
 readonly      =  0 (off)
 readahead     = 256 (on)
 geometry      = 15600/255/63, sectors = 250626566, start = 0

ATA device, with removable media
	Firmware Revision:  I

Standards:
	Likely used: 1
Configuration:
	fixed drive
	removable drive
	disk xfer rate <= 5Mbs
	disk xfer rate > 5Mbs, <= 10Mbs
	rotational speed tol.
	data strobe offset option
	track offset option
	Logical		max	current
	cylinders	38969	0
	heads		256	0
	sectors/track	32769	0
	--
	bytes/track: 0	bytes/sector: 58860
	Logical/Physical Sector size:           512 bytes
	device size with M = 1024*1024:   159621895 MBytes
	device size with M = 1000*1000:   167375688 MBytes (167375 GB)
	cache/buffer size  = unknown
Capabilities:
	IORDY not likely
	bytes avail on r/w long: 32769
	Cannot perform double-word IO
	R/W multiple sector transfer: not supported
	DMA: not supported
	PIO: pio0 
 Timing cached reads:   11382 MB in  2.00 seconds = 5697.83 MB/sec
 Timing buffered disk reads:  90 MB in  3.10 seconds =  29.07 MB/sec
mike@raspberrypi:~ $ sudo hdparm -Tt /dev/sda

/dev/sda:
 Timing cached reads:   11198 MB in  2.00 seconds = 5605.48 MB/sec
 Timing buffered disk reads:  86 MB in  3.13 seconds =  27.49 MB/sec
mike@raspberrypi:~ $ sudo hdparm -Tt /dev/sda

/dev/sda:
 Timing cached reads:   11502 MB in  2.00 seconds = 5758.30 MB/sec
 Timing buffered disk reads:  86 MB in  3.15 seconds =  27.33 MB/sec
mike@raspberrypi:~ $ 




```

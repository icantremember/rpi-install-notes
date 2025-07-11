```

mike@raspberrypi:~ $ sudo hdparm -tTIv /dev/sda

/dev/sda:
 multcount     = 16 (on)
 readonly      =  0 (off)
 readahead     = 256 (on)
 geometry      = 7630853/64/32, sectors = 15627986944, start = 0

ATA device, with non-removable media
	Model Number:       WDC WD80EMZZ-11B4FB0                    
	Serial Number:      WD-CA2ZZEUK
	Firmware Revision:  81.00A81
	Transport:          Serial, SATA 1.0a, SATA II Extensions, SATA Rev 2.5, SATA Rev 2.6, SATA Rev 3.0
Standards:
	Used: unknown (minor revision code 0x006d) 
	Supported: 10 9 8 7 6 5 
	Likely used: 10
Configuration:
	Logical		max	current
	cylinders	16383	0
	heads		16	0
	sectors/track	63	0
	--
	LBA    user addressable sectors:   268435455
	LBA48  user addressable sectors: 15628053168
	Logical  Sector size:                   512 bytes
	Physical Sector size:                  4096 bytes
	Logical Sector-0 offset:                  0 bytes
	device size with M = 1024*1024:     7630885 MBytes
	device size with M = 1000*1000:     8001563 MBytes (8001 GB)
	cache/buffer size  = unknown
	Form Factor: 3.5 inch
	Nominal Media Rotation Rate: 5640
Capabilities:
	LBA, IORDY(can be disabled)
	Queue depth: 32
	Standby timer values: spec'd by Standard, with device specific minimum
	R/W multiple sector transfer: Max = 16	Current = 16
	DMA: *mdma0 mdma1 mdma2 udma0 udma1 udma2 udma3 udma4 udma5 udma6 
	     Cycle time: min=120ns recommended=120ns
	PIO: pio0 pio1 pio2 pio3 pio4 
	     Cycle time: no flow control=120ns  IORDY flow control=120ns
Commands/features:
	Enabled	Supported:
	   *	SMART feature set
	    	Security Mode feature set
	   *	Power Management feature set
	   *	Write cache
	   *	Look-ahead
	   *	WRITE_BUFFER command
	   *	READ_BUFFER command
	   *	NOP cmd
	   *	DOWNLOAD_MICROCODE
	   *	48-bit Address feature set
	   *	Device Configuration Overlay feature set
	   *	Mandatory FLUSH_CACHE
	   *	FLUSH_CACHE_EXT
	   *	SMART error logging
	   *	SMART self-test
	   *	General Purpose Logging feature set
	   *	64-bit World wide name
	   *	WRITE_UNCORRECTABLE_EXT command
	   *	{READ,WRITE}_DMA_EXT_GPL commands
	   *	Segmented DOWNLOAD_MICROCODE
	   *	Gen1 signaling speed (1.5Gb/s)
	   *	Gen2 signaling speed (3.0Gb/s)
	   *	Gen3 signaling speed (6.0Gb/s)
	   *	Native Command Queueing (NCQ)
	   *	Host-initiated interface power management
	   *	Phy event counters
	   *	NCQ priority information
	   *	READ_LOG_DMA_EXT equivalent to READ_LOG_EXT
	    	DMA Setup Auto-Activate optimization
	    	Device-initiated interface power management
	    	Software settings preservation
	   *	SMART Command Transport (SCT) feature set
	   *	SCT Write Same (AC2)
	   *	SCT Features Control (AC4)
	   *	SCT Data Tables (AC5)
	    	unknown 206[12] (vendor specific)
	    	unknown 206[13] (vendor specific)
	   *	DOWNLOAD MICROCODE DMA command
	   *	WRITE BUFFER DMA command
	   *	READ BUFFER DMA command
Security: 
	Master password revision code = 65534
		supported
	not	enabled
	not	locked
	not	frozen
	not	expired: security count
		supported: enhanced erase
	888min for SECURITY ERASE UNIT. 888min for ENHANCED SECURITY ERASE UNIT.
Logical Unit WWN Device Identifier: 50014ee215c896e7
	NAA		: 5
	IEEE OUI	: 0014ee
	Unique ID	: 215c896e7
Checksum: correct
 Timing cached reads:   11462 MB in  2.00 seconds = 5737.78 MB/sec
 Timing buffered disk reads: 628 MB in  3.00 seconds = 209.33 MB/sec
mike@raspberrypi:~ $ sudo hdparm -tT /dev/sda

/dev/sda:
 Timing cached reads:   11248 MB in  2.00 seconds = 5630.41 MB/sec
 Timing buffered disk reads: 556 MB in  3.01 seconds = 184.78 MB/sec
mike@raspberrypi:~ $ sudo hdparm -tT /dev/sda

/dev/sda:
 Timing cached reads:   11476 MB in  2.00 seconds = 5745.25 MB/sec
 Timing buffered disk reads: 554 MB in  3.00 seconds = 184.37 MB/sec


```

# Standard Raspberry Pi Firmware
This repository contains the file and programs you would find in the boot partition of a micro SD card with Raspberry Pi OS Lite Bullseye 32-bit released 2022-04-04 installed, and only those files, with ONE EXCEPTION: this file. Thus, it is a Fully Operational, Pre-Built Linux Kernel, compatible with ALL Raspberry Pi models. That is, until it becomes out of date, at which point you can submit an issue or pull request. this repository work straight out of the box with no setup or building, just 2 partitions: boot and rootfs. stick this repo in boot, alter cmdline.txt and config.txt to your wishes, and do whatever you want with rootfs, though that is the partition the kernel looks in for the init binary executable.

### Configuration with `cmdline.txt` and `config.txt`
`cmdline.txt` and `config.txt` are both configuation file you can add lines to in order to adjust the settings of the kernel.

#### `cmdline.txt`:
| Option                            | Use                                                                | Default        |
|-----------------------------------|--------------------------------------------------------------------|----------------|
| dwc_otg.fiq_fix_enable            | Enable/Disable FIQ Patch                                           | Unknown        |
| dwc_otg.speed                     | Limit USB to Full Speed                                            | 0 (HS)         |
| dwc_otg.lpm_enable                | Change USB Link Power Management                                   | 0 (Disabled)   |
| dwc_otg.microframe_schedule   	  | Enable/Disable Microframe Scheduler                                | 1 (On)         |
| dwc_otg.nak_holdoff_enable        | Enable the NACK Holdoff	                                           | Unknown        |
| sdhci-bcm2708.allow_highspeed     | Allow high speed transfers modes	                                 | Enabled        |
| sdhci-bcm2708.emmc_clock_freq     | Specify the speed of emmc clock	                                   | 50MHz          |
| sdhci-bcm2708.sync_after_dma      | Block in driver until dma complete	                               | Unknown        |
| sdhci-bcm2708.missing_status      | Use the missing status quirk	                                     | Unknown        |
| sdhci-bcm2708.spurious_crc_acmd51 | Use the spurious crc quirk for reading SCR (ACMD51)                | Unknown        |
| sdhci-bcm2708.enable_llm          | Enable low-latency mode (1=Enabled)                                | Unknown        |
| sdhci-bcm2708.extra_messages      | Enable more sdcard warning messages                                | Unknown        |
| i2c-bcm2708.baudrate              | The I2C baudrate	                                                 | 1000KHz        |
| w1-gpio.pullup                    | Enable pullup to enable parasite power in bitbang mode (1=Enabled) | Unknown        |
| smsc95xx.macaddr                  | Overrides the default mac adress with the specified one            | Unknown        |
| console                           | Unknown                                                            | ttyAMA0,115200 |
| kgdboc                            | Unknown                                                            | ttyAMA0,115200 |
| root                              | Specifies the location of the root device                          | /dev/mmcblk0p2 |
| rootfstype                        | Specifies the type of the root filesystem                          | ext4           |
| elevator                          | Unknown                                                            | deadline       |
| rootwait                          | Unknown                                                            | Unknown        |

If you know any more configuration options for `cmdline.txt`, help me out by submitting a pull request!

#### `config.txt`:
At the moment, I dont know of any configuration options for `config.txt`. If you do, help me out by submitting a pull request!

# Standard Raspberry Pi Firmware
This repository contains the file and programs you would find in the boot partition of a micro SD card with Raspberry Pi OS Lite Bullseye 32-bit released 2022-04-04 installed, and only those files, with ONE EXCEPTION: this file. Thus, it is a Fully Operational, Pre-Built Linux Kernel, compatible with ALL Raspberry Pi models. That is, until it becomes out of date, at which point you can submit an issue or pull request. this repository work straight out of the box with no setup or building, just 2 partitions: boot and rootfs. stick this repo in boot, alter cmdline.txt and config.txt to your wishes, and do whatever you want with rootfs, though that is the partition the kernel looks in for the init binary executable.

### Configuration with `cmdline.txt` and `config.txt`
`cmdline.txt` and `config.txt` are both configuation file you can add lines to in order to adjust the settings of the kernel.

#### `cmdline.txt`:
At the moment, I dont know of any configuration options for `cmdline.txt`. If you do, help me out by submitting a pull request!

#### `config.txt`:
At the moment, I dont know of any configuration options for `config.txt`. If you do, help me out by submitting a pull request!

# NUC7i7BNH
Hackintosh NUC7i7BNH - OpenCore 0.7.3

### Specs
+ OS: macOS Big Sur 11.5.2 (Build 20G95) x86_64 / iMac18,1

+ CPU: Intel® Core™ i7-7567U Processor (4M Cache, up to 3.90 GHz, down to 700 MHz)

+ Graphics: Intel Iris Plus Graphics 650

+ Audio: Realtek ALC 283

+ NVMe: Samsung SSD 970 EVO Plus 250GB

+ SATA: INTEL SSD 120GB

+ RAM: 8GB x 2 DDR4 2133 MHz

+ BIOS: 0083

+ Monitor: DELL P2418D

### Comments

+ Enable Sidecar by switching iMac16,2 to iMac18,1 (logout AppleID first before switching).

+ update 'USBMap.kext'.

+ Enable build-in microphone by changing "layout-ID=15".

+ Inject CPU power management data in CPUFriendDataProvider.kext, thanks to https://github.com/corpnewt/CPUFriendFriend

+ Intel wireless card driver and bluetooth driver for Big Sur can be found in https://github.com/OpenIntelWireless/itlwm

+ Intel bluetooth driver for Big Sur can be found in https://github.com/zxystd/IntelBluetoothFirmware

### Credits

+ https://www.tonymacx86.com/threads/guide-intel-nuc7-nuc8-using-clover-uefi-nuc7i7bxx-nuc8i7bxx-etc.261711/

+ https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/kaby-lake.html

+ https://github.com/RehabMan/Intel-NUC-DSDT-Patch
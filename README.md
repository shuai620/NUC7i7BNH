# NUC7i7BNH
Hackintosh NUC7i7BNH - OpenCore 0.7.8

### Specs
+ OS: macOS Monterey 12.2.1 (Build 21D62) x86_64 / iMac18,1

+ CPU: Intel® Core™ i7-7567U Processor (4M Cache, up to 4.0 GHz, down to 700 MHz)

+ Graphics: Intel Iris Plus Graphics 650

+ Audio: Realtek ALC 283

+ NVMe: Samsung SSD 970 EVO Plus 250GB

+ SATA: INTEL SSD 120GB

+ RAM: 8GB x 2 DDR4 2133 MHz

+ BIOS: 0088

+ Monitor: DELL P2418D


### Before upgrading to Monterey

+ Remove "FakePCIID.kext", otherwise the computer will freeze after booting for about 10 mins !!!

+ After removing "FakePCIID.kext", HMDI audio needs reconnection to be identified.

+ Replace "IntelBluetoothInjector.kext" with "BlueToolFixup.kext"


### Comments

+ Enable Sidecar by switching iMac16,2 to iMac18,1 (logout AppleID first before switching).

+ update 'USBMap.kext'.

+ Enable build-in microphone by changing "layout-ID=15".

+ Inject CPU power management data in CPUFriendDataProvider.kext, thanks to https://github.com/corpnewt/CPUFriendFriend

+ Intel wireless card driver for Monterey and Big Sur can be found in https://github.com/OpenIntelWireless/itlwm

+ Intel bluetooth driver for Monterey and Big Sur can be found in https://github.com/zxystd/IntelBluetoothFirmware

### Credits

+ https://www.tonymacx86.com/threads/guide-intel-nuc7-nuc8-using-clover-uefi-nuc7i7bxx-nuc8i7bxx-etc.261711/

+ https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/kaby-lake.html

+ https://github.com/RehabMan/Intel-NUC-DSDT-Patch

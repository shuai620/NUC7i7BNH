# NUC7i7BNH
Hackintosh NUC7i7BNH - OpenCore 0.9.4

### Specs
+ OS: macOS Ventura 13.5.1 (Build 22G90) x86_64 / MacBook Pro14,2

+ CPU: Intel® Core™ i7-7567U Processor (4M Cache, up to 4.0 GHz, down to 600 MHz)

+ Graphics: Intel Iris Plus Graphics 650

+ Audio: Realtek ALC 283

+ NVMe: TOSHIBA SSD 512GB

+ RAM: 8GB x 2 DDR4 2133 MHz

+ BIOS: 0091

+ Monitor: DELL P2418D

### Don't work

+ Sleep doesn't work for Ventura.

### Before upgrading to Monterey

+ Remove "FakePCIID.kext", otherwise the computer will freeze after booting for about 10 mins !!! After removing "FakePCIID.kext", HMDI audio needs reconnection to be identified. Don't use old "FakePCIID.kext"!!!

+ New progress!! Intel HMDI audio has been fixed by recompiling "FakePCIID.kext" with Xcode 13, and "fakepciid_intel_hdmi_audio.kext" has been integrated into new "FakePCIID.kext".

+ Replace "IntelBluetoothInjector.kext" with "BlueToolFixup.kext". 

### Before upgrading to Ventura from Monterey

+ Replace "AirportItlwm.kext" with Ventura version.

### Comments

+ Fix HEVC support in VideoProc, by delete the item in "config.plist": DeviceProperties -> PciRoot(0x0)/Pci(0x2,0x0) -> "AAPL,slot-name".

+ Enable Sidecar by switching iMac16,2 to iMac18,1 (logout AppleID first before switching).

+ Switching from iMac18,1 to MacBookPro14,2, CPU power management will be more balanced.

+ update 'USBMap.kext'.

+ Enable build-in microphone by changing "layout-ID=15".

+ Inject CPU power management data in CPUFriendDataProvider.kext, thanks to https://github.com/corpnewt/CPUFriendFriend. Or use ssdtPRGen.sh to generate ssdt.aml, https://github.com/Piker-Alpha/ssdtPRGen.sh. Choose either method.

+ Intel wireless card driver for Ventura, Monterey and Big Sur can be found in https://github.com/OpenIntelWireless/itlwm

+ Intel bluetooth driver for Ventura, Monterey and Big Sur can be found in https://github.com/zxystd/IntelBluetoothFirmware

### Credits

+ https://www.tonymacx86.com/threads/guide-intel-nuc7-nuc8-using-clover-uefi-nuc7i7bxx-nuc8i7bxx-etc.261711/

+ https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/kaby-lake.html

+ https://github.com/RehabMan/Intel-NUC-DSDT-Patch

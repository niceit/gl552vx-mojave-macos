# Gl552VX-Mojave
# Hackintosh GL552VX Mojave 10.14.6

- Upload Date: 23/9/2020
- For research and study purpose

![Gl552VX Mojave 10.14.6](https://i.imgur.com/LKRZaea.png)

# Clover EFI Bootloader Config 
[Download](https://github.com/CloverHackyColor/CloverBootloader/releases) - This one is using **v5.0 r5122**

**General**
- Clover for UEFI booting only
- Install Clover in ESP

**UEFI Drivers**
- DataHubDxe
- FSInject
- SMSCHelper
- AptioInputFix
- ApfsDriverLoader
- OsxLowMemFixDrv
- FirmwareVolume 

# Installation
Make installation USB Disk (at least 8GB) from **MacOS Mojave Image**, install the **Clover bootloader config** as section above.

Mount EFI USB and copy **BOOT** and **CLOVER** folder downloaded from this repo into **EFI USB**.

Plug USB into **USB2.0** slot (right side of the laptop). Turn on power and choose boot from **USB UEFI Partition**.

Use **DiskUtil** to format the disk to be installed **Apple HFS+ or Journal**, then choose Install MacOS Mojave into that disk.

Useful command to completely format the disk.

**diskutil eraseDisk HFS+ "macosx" /dev/disk1**

**/dev/disk1** is the target part (depend on each machine it will be different).

**MacOS** will start installation progress, no worry that machine will restart 2-3 times to complete it's progress (so you need to be patient here).

# Kexts Others

After installation finished, mount the EFI of MacOS Disk, copy 2 kexts from **kexts-others** to **EFI\CLOVER\kexts\Other**

# Working Object:
- Wifi (BCM94352Z Broadcom)
- Card Reader
- sleep (Fn+F1 icon)
- Airplane mode (Fn+F2 icon)
- shutdown
- Intel HD 530 (WhateverGreen to fix external monitor and large resolutions)
- HDMI
- Bluetooth
- All USB ports
- Keyboard 16 (Support Automatically turn off lights)
- TouchPad with VoodooI2C (Turn off fn+f9 and ignore built-in trackpad when mouse or wireless trackpad is present )
- Fn Keys
- Keyboard Backlighting
- Ethernet (LAN)
- Battery Status
- UVC HD Webcam
- Speaker + Internal Microphone
- iMessage + FaceTime
- Disable Touch ID
- Audio

# Not Working 
- NVIDIA Optimus
- SD Card Reader

# Credit 
- [Lilu](https://github.com/acidanthera/lilu/releases)
- [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) (fix HDMI and resolutions)


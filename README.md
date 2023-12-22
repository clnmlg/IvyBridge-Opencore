<img src="https://www.podfeet.com/blog/wp-content/uploads/2022/02/OpenCore-Logo-bg.png"/>

# Disclaimer
Don't forget to backup original EFI Folder & use this configuration at your own risks.
I strongly recommend you to full read official Opencore documentation related to IvyBridge, 
as it's easier to doublecheck if your hardware is compatible with this EFI. Additionaly, you'll
learn a lot and avoid mistakes by building it yourself rather than simply copy/past a folder from
a random guy (me) on Github.

# IvyBridge-Opencore
Opencore Configuration of Intel IvyBridge Hackintosh (with some tweaks).

# Status

* OS: tested in BigSur 11.7.10
* Opencore: 0.9.1
    * NVRAM: native
    * AppleHotKey: works
    * FileVault: un-tested
    * Boot-Audio: works with onboard audio passthrough
* SMBIOS: iMac14,4
* Power Management
  * Sleep: works, see details below.
  * EC: faked one
  * USB Power: works even with USB3 passthrough

# Hardware configuration

* CPU:
    * Intel 3,4 GHz Quad-Core Intel Core i7 (config.plist configuration is really important for CPU, in particular with Ivy CPU, please follow carrefuly all the instructions of the OpenCore Documentation). 
* GPU:
    * NVIDIA GeForce GTX 680 4 GB (Note that for this card Big Sur Opencore is the latest functionnal OS which support it, cf:documentation)
    * HDMI/DP Audio: works well 
* USB(Passthrough): works, no problem reported
* RAM
  * 8 GB 1333 MHz DDR3
* DISK
  * 120 GB Solid State SATA Drive && 2 TB SATA Disk
* ETHERNET
  * RealtekRTL8111 kext added to OC configuration (not tested, but kext installed)
* WIFI
 * As there are no specific kext for WIFI on Bigsur, I managed to make it work thanks to chris1111 repo : https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter. Just follow readme file to install on your system. 

# Tweaks

I followed Opencore post-install recommendations in order to have a more stable,
fluid Hackintosh.

* Smoother GUI & resolution scale fixed.
* Fast booting removing verbose arguments.

# Usage
1. Download the repository and put the EFI under your EFI disk while following the official Opencore documentation.
2. To update your EFI folder with new kexts or else, you can mount partition using Diskutil native tool or any good
EFI mount software. 

Have fun building !

---
title: "Installing UEFI on Rockpi 5B"
categories:
  - Hardware
tags:
  - traefik
  - ansible
  - auth
---
# Installation
## Maskrom mode
First you have to get the rockpi into Maskrom mode
1. Power off the board.
2. Remove bootable device like MicroSD card, eMMC module, etc.
3. Press the golden (or silver on some board revisions) button and hold it.
4. Plug the USB-A to Type-C cable to ROCK 5B Type-C port, the other side to PC.
5. Release the golded button.
6. Check usb device ```lsusb``` should be something like ***Bus 001 Device 079: ID 2207:350b Fuzhou Rockchip Electronics Company***

## Get images and flash tool
Images:
- [Loader](https://dl.radxa.com/rock5/sw/images/loader/rock-5b/rk3588_spl_loader_v1.08.111.bin)
- [UEFI Releases](https://github.com/edk2-porting/edk2-rk35xx/releases) latest for rock5b

Flash Tool: [rkdevtool](https://wiki.radxa.com/Rock5/install/rockchip-flash-tools)

## Flashing image to SPI
1. List all devices 
```bash
❯ sudo rkdeveloptool ld
DevNo=1 Vid=0x2207,Pid=0x350b,LocationID=104    Maskrom

```


# Sources
[How to wrtite to SPI Flash](https://wiki.radxa.com/Rock5/install/spi#Advanced_.28external.29_method)
[UEFI Releases](https://github.com/edk2-porting/edk2-rk35xx/releases)

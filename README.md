# gentoo-rpi
Gentoo Ebuilds for Raspberry Pi Ahead of the Gentoo Repository. 

Here be ebuilds for arm64 for things in the ::gentoo repo that are out of date.
That does not always mean that they are current, just newer than the ::gentoo repo.

There are mostly but not always, open bugs for the things here.

This repo exists to make it easy for me to keep my Pis in sync.

Only arm64 is tested. That's what I use.
If arm (32 bit) works, that's luck. Well the binary things are tested by upstream and indirectly by millions of users worldwide.

Do no file bugs for ebuilds here as they are not officially supported.

They are all simple version bumps ... so far.

## dev-embedded/raspberrypi-utils

A collection of utilities that survive the deprciated/abandoned media-libs/raspberrypi-userland and media-libs/raspberrypi-userland-bin.
There are no releases. It's built from a seleted commit.


## dev-embedded/rpi-eeprom

Updated	SPI (Boot EEPROM) firmware. Especially important on the Pi5


## sys-boot/raspberrypi-firmware

Together with a recent kernel (6.12.x?) and recent dev-embedded/rpi-eeprom provides some Pi5 performance enhancements.

e.g. Fake NUMA, and increased DRAM refresh interval (less frequent refreshes), so that there is more DRAM time for useful work.


## sys-kernel/raspberrypi-image

Not tested by me at all as I have root in LVM with a module free initramfs. This kernel does not support that, so I don't use it.
It pulls a set of binary files from github so should be OK. The image looks good. 

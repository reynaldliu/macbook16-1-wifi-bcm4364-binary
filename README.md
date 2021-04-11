#MacBookPro 16,1 BCM4364 Wifi 
MacBookPro 16,1 2019 16Inch broadcom bcm4364 wifi works  Linux Kernel Binary

# ubuntu 20.04 install ISO  :

https://github.com/marcosfad/mbp-ubuntu/releases/download/v20.04-5.8.13-1/livecd-5.8.13-mbp-alt.zip
# wifi drivers build guide :

https://wiki.t2linux.org/distributions/ubuntu/building/

# How to Use
1.Download https://github.com/reynaldliu/macbook16-1-wifi-bcm4364-binary/releases

2.Replace or add  `vmlinuz-5.10.28`  to /boot/vmlinuz-5.10.28

3.Replace or add   `initrd.img-5.10.28` to /boot/initrd.img-5.10.28

4.Run command `update-grub`

5.Reboot Computer

6.OK

# FAQ:
1./lib/modules/5.10.28 too large 1.3Gb ,i can not upload it to github
2.linux build include header `/usr/src/5.10.28`  or `/lib/moules/5.10.28/build` too large 8.5Gb,i can not upload it to github

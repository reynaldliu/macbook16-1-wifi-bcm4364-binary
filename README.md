# MacBookPro 16,1 BCM4364 Wifi 
MBP,mbp,mbp16,mbp2019,mbp2019,linux,ubuntu,wifi,drivers,bcm4364,broadcom4364
MacBookPro 16,1 2019 16Inch broadcom bcm4364 wifi works  Linux Kernel Binary

# ubuntu 20.04 install ISO  :

https://github.com/marcosfad/mbp-ubuntu/releases/download/v20.04-5.8.13-1/livecd-5.8.13-mbp-alt.zip
# wifi drivers build guide :

https://wiki.t2linux.org/distributions/ubuntu/building/

# How to Use

1.Download https://github.com/reynaldliu/macbook16-1-wifi-bcm4364-binary/releases/tag/v5.10.28-wifi

2.Replace or add  `vmlinuz-5.10.28`  to /boot/vmlinuz-5.10.28

3.Replace or add   `initrd.img-5.10.28` to /boot/initrd.img-5.10.28

decompression  `lib_modules_5.10.28.tar.gz` to /lib/modules/5.10.28

4.Run command `update-grub`

5.Find Your MBP firmware On `macOS` And Add to `Ubuntu`

`ioreg -l | grep RequestedFiles`

Show,Record File Path
```
"RequestedFiles" = 
({
"Firmware"="C-4364__s-B3/bali.trx",
"TxCap"="C-4364__s-B3/bali-X2.txcb",
"Regulatory"="C-4364__s-B3/bali-X2.clmb",
"NVRAM"="C-4364__s-B3/P-bali-X2_M-HRPN_V-m__m-7.9.txt"
})}
```
`!!!every computer is different, you have to enter macOS to run the command yourself to see the echo!!!`

Put the firmware to Ubuntu system 

The `C-4364__s-B3/bali.trx` File Rename And Copy to  Ubuntu Path `/lib/firmware/brcm/brcmfmac4364-pcie.bin`

The `C-4364__s-B3/bali-X2.clmb`   File Rename And Copy to  Ubuntu Path `/lib/firmware/brcm/brcmfmac4364-pcie.clm_blob`

The `C-4364__s-B3/P-bali-X2_M-HRPN_V-m__m-7.9.txt` File Rename And Copy to  Ubuntu Path `/lib/firmware/brcm/brcmfmac4364-pcie.Apple Inc.-MacBookPro16,1.txt`

6.Reboot Computer

7.OK

# FAQ:


linux build include header `/usr/src/5.10.28`  or `/lib/moules/5.10.28/build` too large 8.5Gb,i can not upload it to github

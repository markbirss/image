# ubuntu-24.04.2-picocalc (Developer Image - HUGE

[Updated] 2025-06-18 - Bug Fix - Uknown Symbols when loading kernel modules

# To extract the image you will require upto 50GB of free disk space and a fast SD/tfCard of at least 16GB
I use these

![image](https://github.com/user-attachments/assets/6a03eee2-4ac7-4e76-a0b6-f68768c010ff)
https://us-legacy.hikvision.com/en/products/accessories/storage/micro-sd-cards/l2-series-video-surveillance-microsd-tf-card-hs-tf

cd image
7z t image.7z.001


```
git clone https://github.com/markbirss/ubuntu-24.04.2-picocalc.git

cd ubuntu-24.04.2-picocalc
rm -fr .git/
cd image

7z x image.7z.001


cd image
sha256sum *

```

```
sha256sum *
a4fbadbe374f01a6c86708eb9615fa679bf3db03fb8176f4933f6f2243ee464c  boot.img
3f43aecc1b5a43689586fe400226610ec03410308f5ce34349c9ae10c20ff82d  MiniLoaderAll.bin
05a8ebd2cc7627722af8b8c8007985989632d5ed6fafa38c2688ca70d7645e7b  parameter.txt
1f0ae484e717d80ab11fe3dc74cad10f5f374a93222b84357c59048a2819cb15  rootfs.img
143ce7fd34449b2ded2a1ac39b342652240115305c47690f8c9f590d90330b16  uboot.img
d84683d1443e6d3a046259f39e25541484a4a71f3f5582d266af0f62f7367ef2  update.img
```




```
sudo ~/Downloads/linux/upgrade_tool uf update.img

Loading firmware...
Support Type:350F       FW Ver:8.1.00   FW Time:2025-06-13 13:34:37
Loader ver:1.01 Loader Time:2025-06-13 13:32:30
Start to upgrade firmware...
Test Device Start
Test Device Success
Check Chip Start
Check Chip Success
Get FlashInfo Start
Get FlashInfo Success
Prepare IDB Start
Prepare IDB Success
Download IDB Start
Download IDB Success
Download Firmware Start
Download Image... (100%)
Download Firmware Success
Upgrade firmware ok.

```

![image](https://github.com/user-attachments/assets/a4eadc3f-982c-49f1-bc2e-6a3b713f3de9)

```
make menuconfig
```

![image](https://github.com/user-attachments/assets/6569b411-5ac0-41ef-8ef2-9357767457c4)

Locate and enable modules for the wifi adatpers (which are available in the 6.1.99 kernel)

```
make modules; make modules_install; reboot
```

or

Download source for your dongle and compile it on the PicoCalc

https://github.com/morrownr/88x2bu-20210702

https://github.com/lwfinger/rtw88

https://github.com/morrownr/rtw89

[Disclaimer] Comes without any warranty whatsoever, use at own risk

[Credits] hiro fu - hisptoot [PicoCalc Drivers - keyboard, pwm, sound and video

Support my work and considder buying me a coffee

https://buymeacoffee.com/mark.birss

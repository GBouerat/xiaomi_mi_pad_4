# Xiaomi Mi Pad 4 : install generic system image

### Reboot your device on TWRP :

```
$ adb reboot recovery
```

![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Menu.png)

### Download files :

Download a Generic system image **system-arm64-aonly-gapps-su.img.xz** from [here](https://github.com/phhusson/treble_experimentations/releases).

Extract system-arm64-aonly-gapps-su.img file from this .zx archive.

Download [Universal DM-Verity and ForceEncrypt Disabler](https://github.com/GBouerat/xiaomi_mi_pad_4/releases/download/Disable_Dm-Verity_FEC/Disable_Dm-Verity_FEC_v1.2.zip) more info [here](https://forum.xda-developers.com/android/software/universal-dm-verity-forceencrypt-t3817389)

### Copy files on your device :

```
$ adb push system-arm64-aonly-gapps-su.img /sdcard/
ROM/AOSP/system-arm64-aonly-gapps-su.img: 1 file pushed. 25.0 MB/s (1541832948 bytes in 58.930s)
```


```
$ adb push Disable_Dm-Verity_FEC_v1.2.zip /sdcard/
Disable_Dm-Verity_FEC_v1.2.zip: 1 file pushed. 25.6 MB/s (3664647 bytes in 0.137s)
```

### Installation :

#### Go in TWRP Wipe menu :
![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Wipe%20menu.png)

#### In Advanced Wipe, select this 4 partitions to wipe :

* Dalvik / ART cache
* Data
* Cache
* System

#### And wipe

![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Wipe%20partitions.png)


#### Go in TWRP Install menu :

* Click on **Install image** button (if you are in Install Zip screen)

![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Select%20image%20to%20install.png)

* In **/sdcard** directory, click on **system-arm64-aonly-gapps-su.img** file and flash it to **System Image**

![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Install%20system%20image.png)

#### Go back in TWRP install menu :

* Click on **Install Zip** button (if you are in Install Image screen)

![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Select%20zip%20to%20install.png)

* In **/sdcard** directory, click on **Disable_Dm-Verity_FEC_v1.2.zip** file and flash it

![](https://raw.githubusercontent.com/GBouerat/xiaomi_mi_pad_4/master/ROM/Screenshots/TWRP%20-%20Install%20disable%20Dm-Verity.png)

#### Now you can reboot your device to your new Android Generic System thanks to Treble.
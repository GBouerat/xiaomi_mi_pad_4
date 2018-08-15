# Xiaomi Mi Pad 4

# TWRP version 3.2.2-0711


#### Reboot your device to bootloader :

```
$ adb reboot bootloader
```

#### List devices on fastboot :

```
$ fastboot devices
XXXXXX	fastboot
```

#### Check if bootloader is unlocked :

```
$ fastboot oem device-infov
(bootloader) Verity mode: true
(bootloader) Device unlocked: true
(bootloader) Device critical unlocked: true
(bootloader) Charger screen enabled: true
OKAY [  0.001s]
Finished. Total time: 0.003s
```

#### Flash TWRP recovery :

```
$ fastboot flash recovery recovery.img
Sending 'recovery' (54400 KB)                      OKAY [  1.540s]
Writing 'recovery'                                 OKAY [  0.410s]
Finished. Total time: 1.952s
```

#### Flash misc : (don't know what it is)

```
$ fastboot flash misc misc.bin
Sending 'misc' (8 KB)                              OKAY [  0.011s]
Writing 'misc'                                     OKAY [  0.004s]
Finished. Total time: 0.017s
```

#### Reboot your device

```
$ fastboot reboot
Rebooting
Finished. Total time: 0.000s
```

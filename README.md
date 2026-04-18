# android_device_OPPO_PCNM00
For building TWRP for OPPO K5

TWRP device tree for OPPO K5

## Features

Works:

- ADB
- Decryption of /data
- Screen brightness settings
- Correct screenshot color
- MTP
- Flashing (opengapps, roms, images and so on)
- Backup/Restore
- USB OTG

TO-DO:

- Adb sideload

## Compile

First checkout manifest:

```
repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
repo sync
```
Finally execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch twrp_PCNM00-eng
mka recoveryimage
```

To test it:

```
fastboot boot out/target/product/PCNM00/recovery.img
```

## Other Sources

Using precompiled stock kernel

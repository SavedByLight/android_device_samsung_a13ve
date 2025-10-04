## Recovery Device Tree for the Samsung Galaxy A13 - SM-A137F (MTK) - tested & working

Mounting /Data is still failing, as we need encryption blobs in A13.

# Contributors
 - [Physwizz](https://github.com/physwizz) - Created the custom kernel
 - [SavedByLight](https://github.com/SavedByLight) - Tester

# How to Build.

## Init repo
```bash
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
```

## Clone a13ve repo
```bash
git clone https://github.com/SavedByLight-twrp/android_device_samsung_a13ve device/samsung/a13ve
```

## Clone a13ve kernel
```bash
git clone https://github.com/edward0181/android_kernel_samsung_a13ve kernel/samsung/a13ve
```

## Sync
```bash
repo sync
```

## Build
```bash
source build/envsetup.sh; export ALLOW_MISSING_DEPENDENCIES=true; lunch twrp_a13ve-eng; mka recoveryimage
```





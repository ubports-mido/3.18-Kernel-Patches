# kernel_3.18_apparmor_patches
Apparmor patches for linux kernel 3.18


### Usage:

```
git am --signoff < 0002-0010_xxxx.patch
```

Patches from https://kernel.ubuntu.com/git/jj/linux-apparmor-backports/refs/heads and fix build error with https://lists.ubuntu.com/archives/kernel-team/2016-January/068128.html

And you also need add apparmor.d configs: https://github.com/ubports-on-vince/device_xiaomi_vince/tree/master/ubuntu/apparmor.d

Add them to system.img: 

```
PRODUCT_COPY_FILES += \
    ...
    ...
    $(LOCAL_PATH)/ubuntu/apparmor.d/local/usr.bin.media-hub-server:system/halium/etc/apparmor.d/local/usr.bin.media-hub-server \
    $(LOCAL_PATH)/ubuntu/apparmor.d/abstractions/base:system/halium/etc/apparmor.d/abstractions/base
```

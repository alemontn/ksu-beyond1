# KernelSU for Galaxy S10/Note10 series

![](working.png)

## ⚠️ Warning

The max version for KSU for non-GKI kernels (the S10's)
is 0.9.5, which is out-of-date. Please do not bug the
creator of KSU or any other KSU contributors/devs with
bugs asking why X, Y or Z doesn't work.

## Compatibility

This is built for LineageOS 21 (from Linux4) but may be
compatible with other ROMS. If you want to test it, make
sure to make a backup of your current bootimg in case
something goes wrong.

##  Known bugs/issues

*  The kernel will be compiled with the '-dirty' suffix,
   since running the KernelSU script makes the Git repo
   'detached', meaning there are uncommited/unstashed
   changes. This can cause Play Integrity to fail since
   it will check the kernel's name. Play Integrity Fix
   should fix this, though.

*  Superuser list not working & resetting on every
   restart

*  Modules won't install & fail with 'os error 22'

##  How to install (Linux only)

1)  Get the bootimg for your device

    This can be done by either extracting it from
    recovery/fastboot or downloading it from your
    ROM's sideload ZIP file

2)  Compile & install 'magiskboot'

    Here are some rough guidelines on how:

    * Install the Android SDK & export it as
      `ANDROID_SDK_ROOT`

    * Clone 'topjohnwu/Magisk' with submodules

    * Get the NDK (`./build.py ndk`)

    * Compile standalone magiskboot (`./build.py binaries magiskboot`)

    * Install (`sudo install -m755 ./native/out/<ARCH>/magiskboot /usr/bin/magiskboot`)

3)  Extract your device's boot image & removing the current kernel:

    `magiskboot unpack boot.img`

    `rm kernel`

4)  Download the patched kernel from releases

5)  Decompress it:

    `gunzip Image.gz`

    `mv Image kernel`

6)  Repack the boot image:

    `magiskboot repack boot.img`

7)  Flash the boot image:

    `adb reboot download`

    `heimdall flash --BOOT boot.img`

8)  Install the KernelSU manager

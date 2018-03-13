## TWRP device tree for LG V20 (US Unlocked US996)

Add to `.repo/local_manifests/us996.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
        <project path="kernel/lge/msm8996" name="x86cpu/twrp_android_kernel_lge_msm8996" remote="github" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_us996-eng
make -j5 recoveryimage
```

** Using TARGET_PREBUILT_KERNEL for now
Kernel sources are available at: https://github.com/x86cpu/twrp_android_kernel_lge_msm8996/tree/android-7.1


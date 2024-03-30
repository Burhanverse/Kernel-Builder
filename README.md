# KERNEL BUILDER
### Kernel Source
The kernel source is hardcoded into the workflow script instead of .env

### Kernel defconfig
Type your kernel defconfig

e.g. lancelot_defconfig

### Kernel file

Type in the image you need, usually the same as BOARD_KERNEL_IMAGE_NAME in your aosp-device tree.

e.g. Image.gz-dtb

### Clang version

The script fetches the latest ZyC Clang, if you need to change it, do it so by editing the kernel.yml (DON'T EDIT THE CLANG IN `CONFIG.ENV`)


### Use overlayfs

It is recommended to add the overlayfs configs in defconfig of your kernel soure.

`CONFIG_OVERLAY_FS=y`
`CONFIG_OVERLAY_FS_REDIRECT_DIR=y`
`CONFIG_OVERLAY_FS_INDEX=y`

### Need DTBO

If your kernel also needs to be flashed with DTBO image, set it to true.

## Credits
- [AnyKernel3](https://github.com/osm0sis/AnyKernel3)
- [AOSP](https://android.googlesource.com)
- [xiaoxindada](https://github.com/xiaoxindada)
- [xiaoleGun](https://github.com/xiaoleGun)

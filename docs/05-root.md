# Rooting (Magisk)

1. Download [Magisk](https://github.com/topjohnwu/Magisk) and install on the device
2. Copy your original boot image to the device (from your backup) with `adb push <path_to_boot_image> /storage/emulated/0/Download`
3. Install Magisk with `adb install <path_to_magisk_apk>`
4. Open Magisk Manager and click `Install`
5. Select the boot image you copied over
6. After patching, pull the boot image with `adb pull /storage/emulated/0/Download/magisk_patched<id>.img` ~/<directory_to_save_to>
7. Reboot into fastboot with `adb reboot bootloader`
8. Flash the patched boot image with `fastboot flash boot <path_to_patched_boot_image>/magisk_patched<id>.img`
9. Reboot the device with `fastboot reboot`

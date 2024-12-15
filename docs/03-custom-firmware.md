# Custom Firmware

## At this step, please ensure you have backed up your original firmware and data, and unlocked your bootloader. Failure to do so may result in a brick that will be a pain to fix.

## Requirements:

- Duoqin F22 Pro
- Android Platform Tools (adb, fastboot)
- [mtkclient](https://github.com/bkerler/mtkclient) - This assumes you've already set it up.

## Steps

1. Choose your GSI image [PHH Wiki List](https://github.com/phhusson/treble_experimentations/wiki/Generic-System-Image-%28GSI%29-list) - I'm using [LineageOS 21-TD (TrebleDroid) built by AndyYan](https://sourceforge.net/projects/andyyan-gsi/files/lineage-21-td/)
2. Download the GSI image (our device is arm64, I'm chosing `arm64-bvN`, you can choose whatever you want as long at it starts with `arm64-b`)
3. Extract the GSI image
4. Power off your device and close the mtkclient GUI if you have it open
5. Plug in your device and run `./mtk.py da vbmeta 3` to disable vbmeta verification + verity
6. Unplug your device and boot it up
7. Enable `USB Debugging` - Settings > About Phone > Tap `Build Number` 7 times > *back* > System > Developer Options > Enable `USB Debugging`
8. Ensure you have no copies of mtkclient running
9. Run `adb reboot recovery` and allow it on the device if prompted
10. When you see the sad Android logo, press Power + Volume Up to get into recovery
11. Navigate to `Enter fastboot` and press Power
12. Plug in your device and run `fastboot flash system <path_to_gsi_image>/image.img`
13. After the image is flashed, go to `Enter bootloader` and press Power
14. Wipe the device with `fastboot -w`
15. Reboot the device with `fastboot reboot`
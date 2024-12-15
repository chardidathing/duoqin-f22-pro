# Unlock Bootloader

### I *assume* this will work for your device, mine came unlocked out of the box. Not too sure about that but we ball.

### Unlocking your bootloader will ***ERASE ALL DATA*** on your device. Please ensure you backup your data before proceeding.

## Requirements

- Duoqin F22 Pro
- Android Platform Tools (adb, fastboot)
- [mtkclient](https://github.com/bkerler/mtkclient) - This assumes you've already set it up.

## Steps

1. Enable `OEM Unlocking` - Settings > About Phone > Tap `Build Number` 7 times > *back* > System > Developer Options > Enable `OEM unlocking`
2. Power off device
3. Run `mtk_gui.py`
4. Plug in device via USB
> At this step, you should see nothing on the device, but should see
```
Phone detected:
MT6778/MT6769 (Helio P65/G85 k68v1)
DA mode
```
5. Navigate to `Flash Tools`
6. Select `Unlock bootloader`
7. Unplug your device and power it on. You will be presented with the OOBE to set up your device again.
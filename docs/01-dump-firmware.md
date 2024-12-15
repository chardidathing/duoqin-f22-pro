# Dumping Firmware

## Requirements

- Duoqin F22 Pro
- Python 3.8+
- Android Platform Tools (adb, fastboot)

### I'll be using the mtkclient GUI for these steps, if you know how to do it with the CLI, feel free. :)

# Whole Flash

1. Setup [mtkclient](https://github.com/bkerler/mtkclient)
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
6. Select `Read Flash` and save it in a safe place.
7. Do the same for `Read preloader` and `Read boot2`

Woo, you dumped the firmware!

> If you happen to have the device with the original Chinese firmware, and are happy to share a copy, feel free to email be at `charlie (at) ktty (dot) au`

# Individual Partitions

If you'd like to dump individual partitions (easy for quick recovery during testing), you can do so with the following steps:

1. Setup [mtkclient](https://github.com/bkerler/mtkclient)
2. Power off device
3. Run `mtk_gui.py`
4. Plug in device via USB
> At this step, you should see nothing on the device, but should see
```
Phone detected:
MT6778/MT6769 (Helio P65/G85 k68v1)
DA mode
```
5. Navigate to `Read partition(s)`
6. Select the partition(s) you'd like to dump
7. Select the `Read partition(s)` button (not the tab), and save them in a safe place.

Woo, you,,, did it or whatever. well done? idk what you want from me </3

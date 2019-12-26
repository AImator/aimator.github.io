## [Making the USB drive bootable](./usb_drive_bootable)

**Note: this procedure requires an .img file that you will be required to create from the .iso file you download.**

*TIP: Drag and Drop a file from Finder to Terminal to 'paste' the full path without typing and risking type errors.*

1. Download the desired file

1. Open the Terminal (in /Applications/Utilities/ or query Terminal in Spotlight)

1. Convert the .iso file to .img using the convert option of hdiutil

```
hdiutil convert /path/to/ubuntu.iso -format UDRW -o /path/to/target.img
```

1. Note: OS X tends to put the .dmg ending on the output file automatically.

1. Run

```
diskutil list
```

to get the current list of devices.

1. Insert your flash media

1. Run

```
diskutil list
```

again and determine the device node assigned to your flash media (e.g. /dev/disk2).

1. Run

```
diskutil unmountDisk /dev/diskN
```

(replace **N** with the disk number from the last command; in the previous example, N would be 2.)

If you see the error "Unmount of diskN failed: at least one volume could not be unmounted", start **Disk Utility.app** and unmount the volume (don't eject).

1. Execute

```
sudo dd if=/path/to/downloaded.img of=/dev/diskN bs=1m
```

(replace /path/to/downloaded.img with the path where the image file is located; for example, ./ubuntu.img or ./ubuntu.dmg).

1. Using /dev/rdisk instead of /dev/disk may be faster.

	- If you see the error dd: Invalid number '1m', you are using GNU dd. Use the same command but replace bs=1m with bs=1M.

	- If you see the error dd: /dev/diskN: Resource busy, make sure the disk is not in use. Start Disk Utility.app and unmount the volume (don't eject).

1. Run

```
diskutil eject /dev/diskN
```

and remove your flash media when the command completes.

1. Restart your Mac and press alt while the Mac is restarting to choose the USB-Stick.
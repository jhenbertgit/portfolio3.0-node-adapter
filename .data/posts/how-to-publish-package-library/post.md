---
date: 11/17/2024
title: How to mount additional hard drive in Linux system
description: This article will demonstrate how to mount an additional hard drive in a Linux system and configure it to auto-mount upon restart.
tags: [How-To, Linux]
---

## Adding a hard drive in Linux is easy! Follow these steps

1. **Identify new drive.**
   By running the command `lsblk -lf` you'll see each drive connected in your system. Take note on the column "NAME" value, (sdb, or sdb1), and the file system type (ext4, vfat, or ntfs).

2. **Partition the drive (Optional).**
   Use `fdisk /dev/sdb` to create partition.

   - Type `n` to create a partition.
   - Follow prompts, then type `w` to write changes.

3. **Format the drive.**
   Format the partition with filesystem, e.g., `mkfs.ext4 /dev/sdb1`

4. **Create a new directory for the mount point.**
   `sudo mkdir /mnt/localdisk`.

5. **Use `mount` to mount the drive in the newly created directory.**
   Follow this syntax `mount /dev/<drivename> <created-mount-point>`. Example, `sudo mount /dev/sdb1 /mnt/localdisk`.

6. **Auto mount the drive upon system restart, add an entry to /etc/fstab.**
   - Open `/etc/fstab` in a text editor. E.g. `sudo nano /etc/fstab`
   - Add this line to the file - `/dev/sdb1 /mnt/localdisk ext4 defaults 0 0`
   - Save and exit the file. `Ctrl + O and Ctrl + X`

## Important Note

- Name of the drive, on my part is sdb, maybe in your part is sdc.
- I am using ext4 filesystem.
- I am using nano in this tutorial, just adjust command on how to save and exit file.

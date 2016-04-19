# DisplayBoards
This is a repo for the SBC display computers attached to the numerous Television displayboards at the Space Systems Lab

# Instructions

1. Image your favorite OpenELEC image first. Copy it to your SD card as such:
   
       sudo dd if=OpenELEC-RPi2.arm-6.0.3.img of=/dev/sdc bs=4M
   
   (Note - your OpenELEC image may vary!)

2. Unplug and boot with your RPi. Once it has booted (it says it wants to reboot), unplug it!

3. Mount the data partition, and run:
   
       ./install_config_archive.sh /path/to/mounted/data/partition
   
4. Mount the mini system partition, and copy `SYSTEM` to this directory.

5. Run:
   
       ./patch_image.sh SYSTEM
   

6. Copy the new `SYSTEM` back onto the mini system partition.

7. Run:
   
       ./install_oemsplash.sh /path/to/mounted/mini/system/partition
   

8. (OPTIONAL) Copy videos you want to the data partition's `video` folder.
   (If it doesn't exist, create it.)

9. Unmount both partitions and eject the SD card.

10. Plug in and enjoy!

# Black borders on HDMI screen

You have to edit the `/boot/config.txt` file (`sudo vim /boot/config.txt`) and uncomment the following line (remove the `#` at the beginning of the line):

```txt
disable_overscan=1
```

If this only makes the border thinner and still not gone completely. So, you may want to take a look at the following lines:

```txt
# uncomment the following to adjust overscan. Use positive numbers if console
# goes off screen, and negative if there is too much border
#overscan_left=16
#overscan_right=16
#overscan_top=16
#overscan_bottom=16
```

---
layout: post
title: New screen
subtitle: "Setting up a new screen in linux"
tags: [linux, hardware]
---

Today I got a new screen so I can return to the department the one I took at the beginning of the lockdown. I got exactly the same: BenQ eye-care 27inches, as I've been happy with it for the past months.

As the setting up of the new screen takes a bit of time, I'm writing here the steps I followed, to do it faster the next time. Note that I'm using Ubuntu 19.10 (Eoan Ermine), with a KDE desktop.

I connected the screen to my laptop and switch off the laptop screen (eDP-1 in my current system) so I only have the big, external screen on:

```
xrandr --output eDP-1 --off
```

eDP-1 refers to my laptop screen, but you can find the name of yours using the command `xrandr`.

Unfortunatelly, the resolution on my big and brand new screen was wrong and there was no option to change the resolution in the 'Settings' menu so I had to change this by hand. I've followed the [instructions posted by Chirag Bhatia](https://unix.stackexchange.com/a/227894) to do the changes on the command line:

 * First find out the specifications of the resolution you think you are targeting, in n my case 1920x1080:
 
 ```
 gtf 1920 1080 60
 ```

 ```
 # 1920x1080 @ 60.00 Hz (GTF) hsync: 67.08 kHz; pclk: 172.80 MHz Modeline "1920x1080_60.00"  172.80  1920 2040 2248 2576  1080 1081 1084 1118  -HSync +Vsync

 ```
 
 * Declare a new mode with the information obtained with the above command:
 
 ```
 xrandr --newmode "1920x1080_60.00"  172.80  1920 2040 2248 2576  1080 1081 1084 1118  -HSync +Vsync
 ```

 * Add the new mode to your output, in my case HDMI-1 (you can see the available names with the `xrandr` command):

 ```
 xrandr --addmode HDMI-1 "1920x1080_60.00"
 ```

 * Set the new resolution mode:

 ```
 xrandr --output HDMI-1 --mode "1920x1080_60.00"
 ```

And now I got a crisp display!
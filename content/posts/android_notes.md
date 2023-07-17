---
title: "Android Notes"
date: 2022-04-04T13:46:37-07:00
tags: []
draft: true
---
In a nutshell: I needed to borrow a phone for the weekend and I had access to several phones that had been modified for research, how can you completely wipe and reset a phone like this?

I did this stuff in an afternoon with some help from a few friends. The following is just some notes that I made from that experience (it may be incorrect, and what is correct today will likely be outdated very soon).



There are 2 main ways to interact with the phone as an exteral device: **adb** and **fastboot**. 

I didn't have much luck with adb, here are some commands that I ran trying to figure things out (while plugging and unplugging a phone):
 
```
sudo apt search adb
sudo apt install adb
sudo adb devices 
lsusb
sudo dmesg 
sudo adb devices 
adb kill-server
adb start-server 
sudo adb devices 
adb kill-server
adb start-server 
sudo adb devices 
adb devices 
adb remount-bootloader
adb restore 
adb shell
```

Conversely, with [fastboot](https://android.googlesource.com/platform/system/core/+/master/fastboot/#fastboot), it seemed to go quite... *fast*
I got the tool and experimented with it:


```
sudo apt install fastboot
which fastboot 
echo $PATH
fastboot -h 
fastboot
fastboot flashing unlock
fastboot flashing lock
fastboot flashing unlock
```

Then I downloaded the [correct image](https://dl.google.com/dl/android/aosp/sargo-sp2a.220305.012-factory-6a43e833.zip) from the specific phone model from the [official place](https://developers.google.com/android/images).
It came with it's own flash-all.sh script.

```
cd Desktop/sargo/
fastboot flashall -w
ls
cd sargo-sp2a.220305.012/
./flash-all.sh 
which fastboot 
sudo mv -v ~/Desktop/platform-tools/fastboot /usr/bin/
./flash-all.sh 
fastboot flashing unlock
./flash-all.sh 
fastboot flashing lock
```

That appeared to do the trick!

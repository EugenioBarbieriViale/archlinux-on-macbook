# Installing Linux on a T2 MacbookAir with broken screen
Here you can read about my experience with installing Linux (dual boot) on a MacbookAir Retina 2020 13" with Intel processor and with the infamous (for the linux community at least) T2 chip.  
The biggest hurdle was dealing with the completely black screen of the laptop, which had to be connected to an external monitor.  
This is not a complete guide, for reference follow the **[t2linux installation guide](https://wiki.t2linux.org/)**

## Entering Recovery Mode

After having partitioned the disk, you have to disable Secure Boot to allow booting from external hard drives. To do it, you have to go in Recovery Mode by pressing the **command+R** key combination at boot time. Achieving this with a broken screen is quite challenging.  
Very likely nothing will show up on the external monitor (plugged via HDMI with an adapter in my case) and you will have to force MacOS to recognize the monitor at boot time.  
In my case, I had to charge the laptop and plug in the monitor before powering it up. In the meantime, with my free hand, I had to keep a magnet attached to where the camera is located, in order to trigger the sensor that detects when the lid is closed. This way, MacOS is forced to use the monitor as video output and not the internal screen.  
For me, connecting the laptop to an external USB keyboard and pressing the key combination to enter Recovery Mode there while the lid was closed didn't work. MacOS was using the monitor as the video output, but even if I pressed the keys on the external keyboard it booted in normal mode.  
I had to use the magnet so that I could press the keys on the built-in keyboard. Still this was not enough, because by using the magnet I only got to a grey screen with a movable cursor. At this point, I had to connect a mouse and a USB keyboard, and then close the lid while holding the magnet in place until the lid was closed (I don't know if this is necessary). Now, I could finally see the recovery mode screen.

## Booting from USB

Now, in order to boot from the bootable flash drive you have to enter MacOS Startup Manager. To do so, on startup you have to press the **Option** key. However, the previous method does not work and up to now, I am not able to display the Startup Manager.  
The only solution I could find is to just go in blind and press the right arrow multiple times to make sure to select the EFI Boot option to the far right in case there was more than one, and then press **Return/Enter**.  
Keep in mind that you should wait a bit before pressing the keys, especially if your MacBook is old. The Startup Manager could take some time to load.  


In the end I managed to get Arch Linux running perfectly. All the drivers (keyboard, audio, wifi, bluetooth, etc.) work fine. I hope that reading about my experience has helped you, traveler! :)  
<img width="1920" height="1080" alt="1775750328" src="https://github.com/user-attachments/assets/7a4489a7-fbcc-45a1-8c9d-bbb351d52238" />

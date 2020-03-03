## Moving OpenCore from USB to Hard Drive

Last edited: March 03, 2020

#### MountEFI

First you need to download CorpNewts MountEFI

Do the following one line at a time in Terminal:
```bash
    git clone https://github.com/corpnewt/MountEFI
    cd MountEFI
    chmod +x MountEFI.command
```  
Then run by double-clicking **MountEFI.command**

#### Mount USB EFI
![](https://i.imgur.com/nI4jKe2.png)

In the above example the USB is option:  
**2. Install macOS Catalina**

Once you have selected this option you will be prompted for your password.

![](https://i.imgur.com/wn7jUcc.png)

Your USB is now mounted and you can enter Q to quit and close Terminal.

#### Copy EFI folder to the desktop

Now open Finder and you will see the EFI partition click on this and you will see a folder called EFI, copy this to your desktop.

#### Unmount USB and mount boot drive's EFI

In finder to the right of EFI click ![](https://i.imgur.com/tF0Rp5Z.png?1) and eject the USB.
Now go back to MountEFI and run it again.  
This time tho we will be mounting the EFI partition on the hard drive.

![](https://i.imgur.com/jeZW3jP.png)

**VERY IMPORTANT**  
If you have any other operating system like Windows or Linux on a seperate hard drive you must make sure you do **NOT** select them in this step.  
In the above example macOS is the drive that contains the Catalina install.  
Select option:  
**2. macOS**

Go back to finder and click on the EFI partition.  
There should be no folders showing.  
If there is some folders there **STOP** and double check what you have mounted.  
Once satisfied you have the correct partition go to your desktop and copy the EFI folder we copied over earlier.  
Now click on the EFI partition and paste the folder.  
Again click on ![](https://i.imgur.com/tF0Rp5Z.png?1) to unmount your hard drive's EFI partition.  
Remove your USB drive from the PC and reboot.  
When rebooting you need to select the drive either by boot selection or making the drive first in BIOS boot order.  
You need to check your board manual on how to do this.

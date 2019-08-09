Wanna try OpenCore but can't boot UEFI based sources? Well don't fret, there's hope for you! OpenCore supports DuetPkg which emulates a UEFI enviroment for legacy systems. 

To start, you nned the following:
* BootInstall.command
* Install source


![BootInstall Location](https://i.imgur.com/D9YT3M4.png)

Within your OpenCore build folder, naviigate to `Utilities/BootInstall`. Here you'll find a file called  `BootInstall.command`. What this does is install DuetPkg to your desired drive. 

![](https://i.imgur.com/FoJs4zU.png)

Now you'll want to run `BootInstall.command`, do note that you may need `sudo` for this to work correctly on newer versions of macOS

```
sudo Utilities/BootInstall/BootInstall.command
```

![Disk Selection/writing new MBR](https://i.imgur.com/20BQvtv.png)

This will givve you a list of avalible disks, choose yours and you will be promted to write a new MBR. Choose yes`[y]` and you'll be finished.

![Finished Installer](https://i.imgur.com/w3AyfVd.png)
![Base EFI](https://i.imgur.com/Lhw52gb.png)

This will provide you with an EFII partiion with a `boot` file, this is where we'll add our OpenCore EFI. 
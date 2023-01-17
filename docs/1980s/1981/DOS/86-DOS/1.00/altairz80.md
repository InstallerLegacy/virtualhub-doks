---
tags: [AltairZ80]
comments: true
---

# How to install 86-DOS 1.00 on AltairZ80?

![AltairZ80 emulator with 86-DOS](/assets/img/1980s/1981/DOS/86-DOS/1.00/altairz80/86-DOS-1.00-AltairZ80-3.webp){ loading=lazy }

86-DOS 1.00 SCP OEM edition for SCP Cromemco 4FDC can run on the AltairZ80 emulator without any modification. If you have a disk image of that version, you can use it or else [download](#downloads) it from WinWorld.

## Downloads

You need the floppy image for 86-DOS. You can download it from WinWorld:

- [86-DOS 1.0 [SCP OEM] [SCP Cromemco 4FDC]](https://winworldpc.com/download/354a6299-2ade-11e8-a4ce-fa163e9022f0){:target="_blank" rel=noopener} ([Local Copy](https://link.storjshare.io/jvl4jik7qrpccq6v5r3t4yrgdagq/virtualhub%2F1980s%2F1981%2FOS%2FDOS%2F86-DOS%2F1.00%2FAltairZ80%2F86-DOS%201.0%20%5BSCP%20OEM%5D%20%5BSCP%20Cromemco%204FDC%5D%20(4-30-1981)%20(8%20inch%20SSSD).7z?download=true))

## Using 86-DOS

!!! tip
    If you have not already installed AltairZ80, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/altairz80/){:target="_blank" rel=noopener} on Linux and Windows.

Extract the archive you downloaded from WinWorld. Inside you will find several files. We do not need all of them. Create a folder somewhere to store the files for this VM.

Now move the `86dos.imd` from the `Images` folder in the extracted folder to the VM folder. Also, move the `86mon.bin` file from the `Emulator` folder to the VM folder.

Now we will create a config file for our VM. Create a text file called `86-DOS-1.00.conf` with the following content in the VM folder:

``` title="86-DOS-1.00.conf" linenums="1"
set cpu 8086
load 86mon.bin 0
load 86mon.bin ff800
set sio port=f6/0/0/0/0/F/0/T
set sio port=f7/0/2/0/1/F/0/F
set sio ansi
set cromfdc norom
set cromfdc en
set wd179x en
d cromfdc fdctype 4
att cromfdc0 86dos.imd
echo
echo VirtualHub (https://virtualhub.eu.org)
echo Press <return> a few times to get monitor prompt, then type 'B' to boot
echo
go ffff0
```

![86-DOS-1.00.conf](/assets/img/1980s/1981/DOS/86-DOS/1.00/altairz80/86-DOS-1.00-AltairZ80-1.webp){ loading=lazy }

Now open a terminal and move to the VM folder. Run the following command to start the emulator:

``` console
altairz80 86-DOS-1.00.conf
```

![altairz80 86-DOS-1.00.conf](/assets/img/1980s/1981/DOS/86-DOS/1.00/altairz80/86-DOS-1.00-AltairZ80-2.webp){ loading=lazy }

Press ++enter++ until a prompt appears and then type a capital ++b++ and press ++enter++ to start 86-DOS.

![AltairZ80 emulator with 86-DOS](/assets/img/1980s/1981/DOS/86-DOS/1.00/altairz80/86-DOS-1.00-AltairZ80-3.webp){ loading=lazy }

Enter a date from the 1980s to continue. You should not enter dates after the year 2000 due to a bug in almost all software released before that year. For example, enter 12-22-82 and press ++enter++. 86-DOS will start. You can enter the `DIR` command to see a list of available files.

![DIR command running in 86-DOS](/assets/img/1980s/1981/DOS/86-DOS/1.00/altairz80/86-DOS-1.00-AltairZ80-4.webp){ loading=lazy }

That's it! We used 86-DOS. We can create a shell script to make it easy to launch the VM. Create a file called 86-DOS-1.00.sh with the following content:

``` bash title="86-DOS-1.00.sh" linenums="1"
#!/bin/bash
altairz80 86-DOS-1.00.conf
```

Now make the file executable:

``` console
chmod +x 86-DOS-1.00.sh
```

Now you can start the VM using the shell script. For example, on KDE you can double-click on that file and click on `Execute` or on GNOME, where you can right-click the file and choose `Run as executable`. The VM will start.

See the [Manuals section](/1980s/1981/DOS/86-DOS/#manuals) on the main 86-DOS page to learn how to use 86-DOS.

### Windows

!!! tip
    You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/categories/os/){:target="_blank" rel=noopener}, a beginner-friendly distro.

!!! note
    In my limited testing, the 64-bit version of AltairZ80 does not seem to work on Windows. On Linux, both 64-bit and 32-bit work fine. If you are using Windows, you can use the 32-bit version instead. 32-bit software works on 64-bit Windows too.

On Windows, you need to place the `altairz80.exe` file you downloaded in [this tutorial](https://setup.virtualhub.eu.org/altairz80/#windows){:target="_blank" rel=noopener} in the VM folder. Then you can follow the above tutorial as usual. The shell script will not work on Windows. You need to rename it to `86-DOS-1.00.bat`. Then you can double-click the file to launch the VM, no need to make it executable.

## Credits

- The disk image used above was taken from [WinWorld](https://winworldpc.com/){:target="_blank" rel=noopener}.

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub){:target="_blank" rel=noopener} soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1980s/1981/DOS/86-DOS/1.00/altairz80/){:target="_blank" rel=noopener}.

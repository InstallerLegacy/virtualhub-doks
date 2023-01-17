---
tags: [VirtualBox]
comments: true
---

# How to install 86-DOS 1.00 on VirtualBox?

![86-DOS 1.00 on VirtualBox](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox.webp){ loading=lazy }

86-DOS 1.00 is not compatible with IBM PC or its emulators. It does not run on VirtualBox unmodified but Michal Necasek of [OS/2 Museum](https://www.os2museum.com/wp/){:target="_blank" rel=noopener} modified it to make it run on IBM PC and its emulators. So we can run it on VirtualBox. If you want to run an unmodified copy of 86-DOS, you can do so using the [AltairZ80 emulator](../altairz80).

## Downloads

You can download the modified image from OS/2 Museum Website:

- [pc86dos.img](http://www.os2museum.com/files/pc86dos.img) ([Local Copy](https://link.storjshare.io/juybp4quqgvmzmxgohgffpfey5ka/virtualhub%2F1980s%2F1981%2FOS%2FDOS%2F86-DOS%2F1.00%2Fpc86dos.img?download=true))

## Using 86-DOS

!!! tip
    If you have not already installed VirtualBox, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/virtualbox/){:target="_blank" rel=noopener} on Linux and Windows.

Open VirtualBox, and click on New Machine. The new machine dialog box will open:

![New Machine Dialog](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-1.webp){ loading=lazy }

Enter the name of the VM as you wish and make sure the Type is set to Other and Version is set to DOS. Click on `Next >`  to continue.

![Setting the RAM](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-2.webp){ loading=lazy }

4 MB of memory is much more than enough for this VM. Set it and click on `Next >`.

![Setting the Hard Disk](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-3.webp){ loading=lazy }

86-DOS does not support hard disks, so click on Do not add a virtual hard disk and click on `Create` button.

![Summary](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-4.webp){ loading=lazy }

You will be shown a summary of the things you have set. Click on `Finish`.

<figure markdown>
![Hard Disk Warning](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-5.webp){ loading=lazy }
</figure>

You will be warned that there is no hard disk. Click on Continue. Now the Virtual Machine is created. Copy the `pc86dos.img` file to the VM folder.

![Adding the floppy](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-6.webp){ loading=lazy }

Back on the VirtualBox window, click on `Empty` which is written in front of `Floppy Device 0:` (See the above image). Now click on `Choose a disk file ...`  and choose the `pc86dos.img` image (You may need to choose All Files from the corner of your file chooser to see the disk image file).

Now click on Start to start the virtual machine:

![86-DOS 1.00 date prompt](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-7.webp){ loading=lazy }

Enter a date from the 1980s to continue. You should not enter dates after the year 2000 due to a bug in almost all software released before that year. For example, enter 12-22-82 and press ++enter++. 86-DOS will start. You can enter the `DIR` command to see a list of available files.

![86-DOS 1.00 DIR command](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-8.webp){ loading=lazy }

You can now close that window. When you will try to close the window this window will open:

<figure markdown>
![86-DOS 1.00 close window](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-9.webp){ loading=lazy }
</figure>

Make sure to choose to `Power off the machine` and then click on `OK`.

Since 86-DOS is used from floppy disks, it is better to add another floppy drive as it is the required setup for many software and more convenient with others. Click on Settings and choose storage from the left sidebar. Now click on the small floppy icon next to `Controller: Floppy`  to add a floppy drive (see the below image):

![Adding a floppy drive](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-10.webp){ loading=lazy }

Click on `Leave Empty` when the following window opens:

<figure markdown>
![Leave the floppy drive empty](/assets/img/1980s/1981/DOS/86-DOS/1.00/virtualbox/86-DOS-1.00-VirtualBox-11.webp){ loading=lazy }
</figure>
Now click on `OK` to close the settings window. Now we can add another floppy if we want.

That's it. We used 86-DOS 1.00 in VirtualBox. See the [Manuals section](/1980s/1981/DOS/86-DOS/#manuals) on the main 86-DOS page to learn how to use 86-DOS.

### Windows

!!! tip
    You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/categories/os/){:target="_blank" rel=noopener}, a beginner-friendly distro.

You can follow the above tutorial on Windows also. No change is required specifically for Windows.

## Credits

- The disk image used above was taken from the [OS/2 Museum website](https://www.os2museum.com/wp/){:target="_blank" rel=noopener}. Thanks to Michal Necasek for making this image available.

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub){:target="_blank" rel=noopener} soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1980s/1981/DOS/86-DOS/1.00/virtualbox){:target="_blank" rel=noopener}.

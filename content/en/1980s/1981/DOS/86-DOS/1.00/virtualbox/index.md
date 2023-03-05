---
title: "How to install 86-DOS 1.00 on VirtualBox?"
description: "Open VirtualBox, and click on New Machine. The new machine dialog box will open. Enter the name of the VM as you wish and make sure the Type is set to Other and Version is set to DOS."
date: 2023-03-05T07:08:56+05:30
draft: false
images: [86-DOS-1.00-VirtualBox.webp]
type: docs
weight: 121102
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox.webp" alt="86-DOS 1.00 on VirtualBox" >}}

86-DOS 1.00 is not compatible with IBM PC or its emulators. It does not run on VirtualBox unmodified but Michal Necasek of [OS/2 Museum](https://www.os2museum.com/wp/) modified it to make it run on IBM PC and its emulators. So we can run it on VirtualBox. If you want to run an unmodified copy of 86-DOS, you can do so using the [AltairZ80 emulator](../altairz80).

## Downloads

You can download the modified image from OS/2 Museum Website:

- [pc86dos.img](http://www.os2museum.com/files/pc86dos.img) ([Local Copy](https://link.storjshare.io/juybp4quqgvmzmxgohgffpfey5ka/virtualhub%2F1980s%2F1981%2FOS%2FDOS%2F86-DOS%2F1.00%2Fpc86dos.img?download=true))

## Using 86-DOS

{{< alert icon="👉" context="success" >}}
If you have not already installed VirtualBox, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/virtualbox/) on Linux and Windows.
{{< /alert >}}

Open VirtualBox, and click on New Machine. The new machine dialog box will open:

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-1.webp" alt="New Machine Dialog" >}}

Enter the name of the VM as you wish and make sure the Type is set to Other and Version is set to DOS. Click on `Next >`  to continue.

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-2.webp" alt="Setting the RAM" >}}

4 MB of memory is much more than enough for this VM. Set it and click on `Next >`.

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-3.webp" alt="Setting the Hard Disk" >}}

86-DOS does not support hard disks, so click on Do not add a virtual hard disk and click on `Next` button.

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-4.webp" alt="Summary" >}}

You will be shown a summary of the things you have set. Click on `Finish`.

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-5.webp" alt="Hard Disk Warning" >}}

You will be warned that there is no hard disk. Click on `Continue`. Now the Virtual Machine is created. Copy the `pc86dos.img` file to the VM folder.

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-6.webp" alt="Adding the floppy" >}}

Back on the VirtualBox window, click on `Empty` which is written in front of `Floppy Device 0:` (See the above image). Now click on `Choose a disk file ...`  and choose the `pc86dos.img` image (You may need to choose All Files from the corner of your file chooser to see the disk image file).

Now click on Start to start the virtual machine:

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-7.webp" alt="86-DOS 1.00 date prompt" >}}

Enter a date from the 1980s to continue. You should not enter dates after the year 2000 due to a bug in almost all software released before that year. For example, enter 12-22-82 and press `enter`. 86-DOS will start. You can enter the `DIR` command to see a list of available files.

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-8.webp" alt="86-DOS 1.00 DIR command" >}}

You can now close that window. When you will try to close the window this window will open:

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-9.webp" alt="86-DOS 1.00 close window" >}}

Make sure to choose to `Power off the machine` and then click on `OK`.

Since 86-DOS is used from floppy disks, it is better to add another floppy drive as it is the required setup for many software and more convenient with others. Click on Settings and choose storage from the left sidebar. Now click on the small floppy icon next to `Controller: Floppy`  to add a floppy drive (see the below image):

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-10.webp" alt="Adding a floppy drive" >}}

Click on `Leave Empty` when the following window opens:

{{< figure src="/1980s/1981/dos/86-dos/1.00/virtualbox/86-DOS-1.00-VirtualBox-11.webp" alt="Leave the floppy drive empty" >}}

Now click on `OK` to close the settings window. Now we can add another floppy if we want.

That's it. We used 86-DOS 1.00 in VirtualBox. See the [Manuals section](/1980s/1981/DOS/86-DOS/#manuals) on the main 86-DOS page to learn how to use 86-DOS.

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

You can follow the above tutorial on Windows also. No change is required specifically for Windows.

## Credits

- The disk image used above was taken from the [OS/2 Museum website](https://www.os2museum.com/wp/). Thanks to Michal Necasek for making this image available.

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1980s/1981/DOS/86-DOS/1.00/virtualbox).

---
title: "How to install ! TSS/8 on SIMH?"
description: 'We can run ! TSS/8 on the SIMH PDP-8 emulator. First, we need to download the ! TSS/8 kit. You can download the kit needed to run ! TSS/8 on the SIMH PDP-8 emulator from the "SIMH Legacy" website:'
date: 2023-08-19T18:00:56+05:30
draft: false
images: [TSS8-B.webp]
type: docs
weight: 210001
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1960s/1968/tss8/simh/TSS8-B.webp" alt="SIMH PDP-8 emulator with ! TSS/8" >}}

We can run [! TSS/8](/1960s/1968/tss8) on the SIMH PDP-8 emulator. First, we need to download the ! TSS/8 kit.

## Downloads

You can download the kit needed to run ! TSS/8 on the SIMH PDP-8 emulator from the ["SIMH Legacy" website](http://simh.trailing-edge.com/):

- [! TSS/8 kit](http://simh.trailing-edge.com/kits/tss8.zip)

## Using ! TSS/8

{{< alert icon="👉" context="success" >}}
If you have not already installed SIMH PDP-8 emulator, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/simh-pdp8/) on Linux and Windows.
{{< /alert >}}

Extract the kit you downloaded. Inside you will find several files. Create a folder somewhere to store the files for this VM and move the files named `tss8_init.bin` and `tss8_rf.dsk` into it.

Now we will create a config file for our VM. Create a text file called `pdp8.ini` with the following content in the VM folder:

``` config
load tss8_init.bin
set rf enabled
set df disabled
attach rf tss8_rf.dsk
attach ttix 4000
run 24200
```

{{< figure src="/1960s/1968/tss8/simh/TSS8-1.webp" alt="pdp8.ini" >}}

Now open a terminal and move to the VM folder. Run the following command to start the emulator:

``` console
pdp8
```

{{< figure src="/1960s/1968/tss8/simh/TSS8-2.webp" alt="pdp8" >}}

After the emulator starts, type `START` and press enter. When asked enter the date in `MM-DD-YY` format. Year should be between 74 and 85. Then enter time in `HH:MM` 24-hour format.

Press enter until you get a `.` prompt. The type the following:

```
LOGIN 2 LXHE
```

There will be no output on screen as you type this, but it is being typed. Press enter after you are done. Here, 2 is the username and LXHE is the password. There are other users too. You can learn about them from Manuals and site listed below. Finally, you will get to this screen:

{{< figure src="/1960s/1968/tss8/simh/TSS8-3.webp" alt="Login Successful" >}}

Type `R CAT` and press enter. It will list all the files available on the disk.

{{< figure src="/1960s/1968/tss8/simh/TSS8-4.webp" alt="List of files in ! TSS/8" >}}

That's it! We used ! TSS/8. We can create a shell script to make it easy to launch the VM. Create a file called `TSS8.sh` with the following content:

``` bash
#!/bin/bash
pdp8
```

Now make the file executable:

``` console
chmod +x TSS8.sh
```

Now you can start the VM using the shell script. For example, on KDE you can right-click the file and choose `Run in Konsole` or on GNOME, where you can right-click the file and choose `Run as executable`. The VM will start.

See the [manuals section](/1960s/1968/tss8/#manuals) on the [main ! TSS/8 page](/1960s/1968/tss8/) and [this website](https://raymii.org/s/articles/Running_TSS_8_on_the_DEC_PiDP-8_i_and_SIMH.html) to learn how to use it.

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

On Windows, you need to place the `PDP8.exe` file you downloaded in [this tutorial](https://setup.virtualhub.eu.org/simh-pdp8#windows) in the VM folder. Then you can follow the above tutorial as usual. The shell script will not work on Windows. You need to rename it to `TSS8.bat`. Then you can double-click the file to launch the VM, no need to make it executable.

## Credits

- The disk image and other files used above are from a kit available on [SimH "Classic" website](http://simh.trailing-edge.com/).

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial may be available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1960s/1968/tss8/simh/).

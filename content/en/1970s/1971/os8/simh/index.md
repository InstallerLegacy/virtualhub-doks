---
title: "How to install ! OS/8 on SIMH?"
description: 'We can run ! OS/8 on the SIMH PDP-8 emulator. First, we need to download the ! OS/8 kit. You can download the kit needed to run ! OS/8 on the SIMH PDP-8 emulator from the "SIMH Legacy" website:'
date: 2023-08-19T18:00:56+05:30
draft: false
images: [OS8-SIMH-3.webp]
type: docs
weight: 210001
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1970s/1971/os8/simh/OS8-SIMH-3.webp" alt="SIMH PDP-8 emulator with ! OS/8" >}}

We can run [! OS/8](/1970s/1971/os8) on the SIMH PDP-8 emulator. First, we need to download the ! OS/8 kit.

## Downloads

You can download the kit needed to run ! OS/8 on the SIMH PDP-8 emulator from the ["SIMH Legacy" website](http://simh.trailing-edge.com/):

- [! OS/8 kit](http://simh.trailing-edge.com/kits/os8swre.tar.Z)

If you are on Windows, you may need to install additional software such as [7-Zip](https://www.7-zip.org/) to extract the kit.

## Using ! OS/8

{{< alert icon="👉" context="success" >}}
If you have not already installed SIMH PDP-8 emulator, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/simh-pdp8/) on Linux and Windows.
{{< /alert >}}

Extract the kit you downloaded. Inside you will find two folders. Open the folder named `Disks`. Inside, you will find two files. Create a folder somewhere to store the files for this VM and move the file named `os8_rx.dsk` into it.

Now we will create a config file for our VM. Create a text file called `pdp8.ini` with the following content in the VM folder:

``` config
attach rx0 os8_rx.dsk
boot rx0
```

{{< figure src="/1970s/1971/os8/simh/OS8-SIMH-1.webp" alt="pdp8.ini" >}}

Now open a terminal and move to the VM folder. Run the following command to start the emulator:

``` console
pdp8
```

{{< figure src="/1970s/1971/os8/simh/OS8-SIMH-2.webp" alt="pdp8" >}}

After the emulator starts, you can enter `DIR` to see a list of files available:

{{< figure src="/1970s/1971/os8/simh/OS8-SIMH-3.webp" alt="List of files in ! OS/8" >}}

That's it! We used ! OS/8. We can create a shell script to make it easy to launch the VM. Create a file called `OS8.sh` with the following content:

``` bash
#!/bin/bash
pdp8
```

Now make the file executable:

``` console
chmod +x OS8.sh
```

Now you can start the VM using the shell script. For example, on KDE you can right-click the file and choose `Run in Konsole` or on GNOME, where you can right-click the file and choose `Run as executable`. The VM will start.

See the [manuals section](/1970s/1971/os8/#manuals) on the [main ! OS/8 page](/1970s/1971/os8/) to learn how to use it.

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

On Windows, you need to place the `PDP8.exe` file you downloaded in [this tutorial](https://setup.virtualhub.eu.org/simh-pdp8#windows) in the VM folder. Then you can follow the above tutorial as usual. The shell script will not work on Windows. You need to rename it to `OS8.bat`. Then you can double-click the file to launch the VM, no need to make it executable.

## Credits

- The disk image and other files used above are from a kit available on [SimH "Classic" website](http://simh.trailing-edge.com/).

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial may be available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1970s/1971/os8/simh/).

---
title: "How to install ! PDP7 UNIX on SIMH?"
description: 'We can run ! PDP7 UNIX on the SIMH PDP-7 emulator. First, we need to download the ! PDP7 UNIX kit. You can download the kit needed to run it on the SIMH PDP-7 emulator from our github repo.'
date: 2023-08-22T10:08:56+05:30
draft: false
images: [pdp7unix-SIMH-4.webp]
type: docs
weight: 110001
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1970s/1970/pdp7unix/simh/pdp7unix-SIMH-4.webp" alt="SIMH PDP-7 emulator with ! PDP7 UNIX" >}}

We can run [! PDP7 UNIX](/1970s/1970/pdp7unix) on the SIMH PDP-7 emulator. First, we need to download the ! PDP7 UNIX kit.

## Downloads

You can download the kit needed to run ! PDP7 UNIX on the SIMH PDP-7 emulator from [our github repo fork](https://github.com/InstallerLegacy/pdp7-unix) of the original [project to resurrect Unix on the PDP-7 from a scan of the original assembly code](https://github.com/DoctorWkt/pdp7-unix):

- [! PDP7 UNIX kit](https://github.com/InstallerLegacy/pdp7-unix/releases/download/20230821/pdp7.zip)

We will publish a guide on how to create the images yourself soon.

## Using ! PDP7 UNIX

{{< alert icon="👉" context="success" >}}
If you have not already installed SIMH PDP-7 emulator, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/simh-pdp7/) on Linux and Windows.
{{< /alert >}}

Extract the kit you downloaded. Inside you will find two files. Create a folder somewhere to store the files for this VM and move those two files named `boot.rim` and `image.fs` into it.

Now we will create a config file for our VM. Create a text file called `pdp7.ini` with the following content in the VM folder:

``` config
set cpu 8k
set cpu eae
set cpu history=100
show cpu
set tti unix
set rb ena
att rb image.fs
set g2in ena
att -U g2in 12345
set lpt disa
set drm disa
set dt disa
show dev
load boot.rim 010000
go
```

{{< figure src="/1970s/1970/pdp7unix/simh/pdp7unix-SIMH-1.webp" alt="pdp7.ini" >}}

Now open a terminal and move to the VM folder. Run the following command to start the emulator:

``` console
pdp7
```

{{< figure src="/1970s/1970/pdp7unix/simh/pdp7unix-SIMH-2.webp" alt="pdp7" >}}

After the emulator starts, login using the id `ken` and password `ken`. You will see the following screen:

{{< figure src="/1970s/1970/pdp7unix/simh/pdp7unix-SIMH-3.webp" alt="login" >}}

{{< alert icon="👉" context="success" >}}
There are other user accounts on the image like `dmr` (password: `dmr`). Do you know who `dmr` and `ken` were? Check the first comment to find out, or search it on the web!
{{< /alert >}}

Type `ls` followed by enter. It will list all the files available on the disk.

{{< figure src="/1970s/1970/pdp7unix/simh/pdp-7-unix-SIMH-4.webp" alt="List of files in ! PDP7 UNIX" >}}

That's it! We used ! PDP7 UNIX. We can create a shell script to make it easy to launch the VM. Create a file called `pdp7unix.sh` with the following content:

``` bash
#!/bin/bash
pdp7
```

Now make the file executable:

``` console
chmod +x pdp7unix.sh
```

Now you can start the VM using the shell script. For example, on KDE you can right-click the file and choose `Run in Konsole` or on GNOME, where you can right-click the file and choose `Run as executable`. The VM will start.

See the [manuals section](/1970s/1970/pdp7unix/#manuals) on the [main ! PDP7 UNIX page](/1970s/1970/pdp7unix) to learn how to use it.

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

On Windows, you need to place the `PDP7.exe` file you downloaded in [this tutorial](https://setup.virtualhub.eu.org/simh-pdp7#windows) in the VM folder. Then you can follow the above tutorial as usual. The shell script will not work on Windows. You need to rename it to `pdp7unix.bat`. Then you can double-click the file to launch the VM, no need to make it executable.

## Credits

- The disk image and other files used above are from a kit built from the [project to resurrect Unix on the PDP-7 from a scan of the original assembly code](https://github.com/DoctorWkt/pdp7-unix).

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1970s/1970/pdp7unix/simh/).

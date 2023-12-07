---
title: "How to install Alto OS on ContrAlto emulator?"
description: "We can run Alto OS on ContrAlto emulator. First we need to download a disk image of Alto OS. You can download the Alto OS Non-programmer's disk image bitsavers:"
date: 2023-11-30T09:08:56+05:30
draft: false
images: [alto-os-contralto-7.webp]
type: docs
weight: 310001
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1970s/1973/alto-os/contralto/alto-os-contralto-7.webp" alt="Alto OS running on ContrAlto emulator" >}}

We can run [Alto OS](/1970s/1973/alto-os/) on ContrAlto emulator. First we need to download a disk image of Alto OS.

## Downloads

You can download the Alto OS Non-programmer's disk image [bitsavers](http://bitsavers.org/bits/Xerox/Alto/simulator/salto/disks/):

- [Alto OS Non-programmer's disk image](http://bitsavers.org/bits/Xerox/Alto/simulator/salto/disks/nonprog.dsk.Z)

If you are on Windows, you may need to install additional software such as [7-Zip](https://www.7-zip.org/) to extract the kit.

## Setting Up

{{< alert icon="👉" context="success" >}}
If you have not already installed ContrAlto emulator, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/contralto/) on Linux and Windows.
{{< /alert >}}

### Linux

Extract the `nonprog.dsk.Z` you downloaded. Inside you will find the `nonprog.dsk` disk image file. Copy that file to where you have stored the files for ContrAlto emulator.

Now open the file called `Contralto.cfg` in a text editor. Find the following line:

```config
# Drive0Image =
```

and replace it with the following:

```config
Drive0Image = nonprog.dsk
```

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-1.webp" alt="Contralto.cfg" >}}

Save and quit the file.

Now open a terminal and move to the ContrAlto folder. Run the following command to start the emulator:

``` console
mono Contralto.exe
```

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-2.webp" alt="mono Contralto.exe" >}}

In the console window that appears, type `start` followed by enter. The main emulation window will turn white, and Alto OS will start.

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-3.webp" alt="start (console)" >}}

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-4.webp" alt="start (emulation)" >}}

You can now continue with [installing Alto OS](#installing-alto-os).

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

Start the ContrAlto emulator from Start menu. After it opens, click on `System` > `Drive 0` > `Load`. Choose the `nonprog.dsk` file. Now click on `System` > `Start`. The emulation will start. You can now continue with [installing Alto OS](#installing-alto-os).

## Installing Alto OS

Run `install` in the emulation window to start the installation. When asked whether you want the long installation dialog, press `N`. Enter your username and the name you want to give to the disk.

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-5.webp" alt="Installation" >}}

If you want to setup a password, press `Y` else press `N`. If you choose to setup a password, enter it. You will need the password every time you start Alto OS, so make sure to remember it.

Afterwards, Alto OS will restart. If you have setup a password, it will ask for it. Note that while the password is shown as you type when setting it, there is no feedback while you are entering you password now, similar to Unix systems, but the password is being entered.

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-6.webp" alt="Password" >}}

After entering the password, Alto OS will start and display your username as well as the disk name you gave. You can type `?` to see the list of files:

{{< figure src="/1970s/1973/alto-os/contralto/alto-os-contralto-7.webp" alt="List of files" >}}

That's it! We installed Alto OS. See the [manuals section](/1970s/1973/alto-os/#manuals) on the [main Alto OS page](/1970s/1973/alto-os/) to learn how to use it.

There are several preinstalled apps on the disk image. We cover them here:

- [Preinstalled apps in Alto OS](/1970s/1973/alto-os/preinstalled-apps/)

## Credits

- The disk image and other files used above are from [bitsavers](http://bitsavers.org/bits/Xerox/Alto/simulator/salto/disks/). They have disk images of many software which run on Alto OS. You may want to try them.

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org1970s/1973/alto-os/contralto/).

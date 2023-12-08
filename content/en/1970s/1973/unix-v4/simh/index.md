---
title: "How to install ! Unix v4 on SIMH?"
description: 'Sadly, we do not have a complete copy of Unix v4, but we do have a copy of a kernel that is from between v3 and v4. We can use that kernel with v5 userland.'
date: 2023-11-30T09:08:56+05:30
draft: false
images: [unix-v4-SIMH--5.webp]
type: docs
weight: 320001
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1970s/1973/unix-v4/simh/unix-v4-SIMH-5.webp" alt="SIMH PDP-11 emulator with ! Unix v4" >}}

Sadly, we do not have a complete copy of Unix v4, but we do have a copy of a kernel that is from between v3 and v4. We can use that kernel with v5 userland. It can be used on SIMH PDP-11 emulator.

## Downloads

First, we need to prepare an image of Unix v5 with the `nsys` kernel. We have prepared such an image for you to download:

- [! Unix-v4 image (v5 root with nsys kernel)](https://github.com/InstallerLegacy/nsys-image/releases/latest/download/nsysroot.zip)

If you want to prepare the image yourself, refer to [our guide on how to do so](/blog/how-to-put-the-nsys-kernel-on-a-disk-image-of-unix-v5/).

## Using ! Unix-v5

{{< alert icon="👉" context="success" >}}
If you have not already installed SIMH PDP-11 emulator, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/simh-pdp11/) on Linux and Windows.
{{< /alert >}}

Extract the archive you downloaded. Inside you will find a file called `nsysroot`. Create a folder somewhere to store the files for this VM and move that file into it.

Now we will create a config file for our VM. Create a text file called `pdp11.ini` with the following content in the VM folder:

``` config
set cpu 11/45
att rk0 nsysroot
boot rk0
```

{{< figure src="/1970s/1973/unix-v4/simh/unix-v4-SIMH-1.webp" alt="pdp11.ini" >}}

Now open a terminal and move to the VM folder. Run the following command to start the emulator:

``` console
pdp11
```

{{< figure src="/1970s/1973/unix-v4/simh/unix-v4-SIMH-2.webp" alt="pdp11" >}}

After the emulator starts, you will get a `@` prompt. Type `nsys` and press enter to run the `nsys` kernel.

{{< figure src="/1970s/1973/unix-v4/simh/unix-v4-SIMH-3.webp" alt="boot" >}}

You will be asked to login. Type `root` and press enter to login. There is no password.

{{< figure src="/1970s/1973/unix-v4/simh/unix-v4-SIMH-4.webp" alt="! Unix-v4 login" >}}

You can now run `ls` to see the list of files. To change directory, you need to use the `chdir` command, `cd` is not available.

{{< figure src="/1970s/1973/unix-v4/simh/unix-v4-SIMH-5.webp" alt="! Unix-v4 list of files in root." >}}

That's it! We used ! Unix-v4. We can create a shell script to make it easy to launch the VM. Create a file called `unix-v4.sh` with the following content:

``` bash
#!/bin/bash
pdp11
```

Now make the file executable:

``` console
chmod +x unix-v4.sh
```

Now you can start the VM using the shell script. For example, on KDE you can right-click the file and choose `Run in Konsole` or on GNOME, where you can right-click the file and choose `Run as executable`. The VM will start.

See the [manuals section](/1970s/1973/unix-v4/#manuals) on the [main ! Unix-v4 page](/1970s/1973/unix-v3) to learn how to use it.

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

On Windows, you need to place the `PDP11.exe` file you downloaded in [this tutorial](https://setup.virtualhub.eu.org/simh-pdp11#windows) in the VM folder. Then you can follow the above tutorial as usual. The shell script will not work on Windows. You need to rename it to `unix-v4.bat`. Then you can double-click the file to launch the VM, no need to make it executable.

## Credits

- The Unix v5 image, the `nsys` kernel and other files used above are from [TUHS](https://www.tuhs.org).

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1970s/1973/unix-v4/simh/).

---
title: "How to install ! DOS-15 on SIMH?"
description: 'We can run ! DOS-15 on the SIMH PDP-15 emulator. First, we need to download the ! DOS-15 kit. You can download the kit needed to run ! DOS-15 on the SIMH PDP-15 emulator from the "SIMH Legacy" website.'
date: 2023-11-24T07:08:56+05:30
draft: false
images: [dos-15-SIMH-5.webp]
type: docs
weight: 140001
---

{{< load-photoswipe >}}
{{< fig class="no-photoswipe" src="/1970s/1970/dos-15/simh/dos-15-SIMH-5.webp" alt="SIMH PDP-15 emulator with ! DOS-15" >}}

We can run [! DOS-15](/1970s/1970/dos-15) on the SIMH PDP-15 emulator. First, we need to download the ! DOS-15 kit.

## Downloads

You can download the kit needed to run ! DOS-15 on the SIMH PDP-15 emulator from the ["SIMH Legacy"](http://simh.trailing-edge.com/) website:

- [! DOS-15 kit](http://simh.trailing-edge.com/kits/dos15.zip)

## Using ! DOS-15

{{< alert icon="👉" context="success" >}}
If you have not already installed SIMH PDP-15 emulator, see [the VirtualHub Setup tutorial on how to do so](https://setup.virtualhub.eu.org/simh-pdp15/) on Linux and Windows.
{{< /alert >}}

Extract the kit you downloaded. Inside you will find several files. Create a folder somewhere to store the files for this VM and move those two files named `dosv2a_4p.rf` and `rfsboot.rim` into it.

Now we will create a config file for our VM. Create a text file called `pdp15.ini` with the following content in the VM folder:

``` config
at -e rf dosv2a_4p.rf
load rfsboot.rim 77637
run
```

{{< figure src="/1970s/1970/dos-15/simh/dos-15-SIMH-1.webp" alt="pdp15.ini" >}}

Now open a terminal and move to the VM folder. Run the following command to start the emulator:

``` console
pdp15
```

{{< figure src="/1970s/1970/dos-15/simh/dos-15-SIMH-2.webp" alt="pdp15" >}}

When asked for a date, enter it in `MM/DD/YY` format. You *cannot* use backspace to erase characters, even if it looks like you can. Try entering a date before the year 2000, to avoid problems related to [Y2K](https://en.wikipedia.org/wiki/Year_2000_problem).

{{< figure src="/1970s/1970/dos-15/simh/dos-15-SIMH-3.webp" alt="Enter date" >}}

Now that DOS-15 is ready, let's run some commands on it. Type `D` and press enter to see the system's date:

{{< figure src="/1970s/1970/dos-15/simh/dos-15-SIMH-4.webp" alt="See date" >}}

You can run `I` to see a list of commands you can run:

{{< figure src="/1970s/1970/dos-15/simh/dos-15-SIMH-5.webp" alt="List of commands" >}}

That's it! We used ! DOS-15. We can create a shell script to make it easy to launch the VM. Create a file called `dos-15.sh` with the following content:

``` bash
#!/bin/bash
pdp15
```

Now make the file executable:

``` console
chmod +x dos-15.sh
```

Now you can start the VM using the shell script. For example, on KDE you can right-click the file and choose `Run in Konsole` or on GNOME, where you can right-click the file and choose `Run as executable`. The VM will start.

See the [manuals section](/1970s/1970/dos-15/#manuals) on the [main ! DOS-15 page](/1970s/1970/dos-15) to learn how to use it.

### Windows

{{< alert icon="👉" context="success" >}}
You should use Linux. If you don’t know how to install a Linux distro, see [our tutorials on how to install Kubuntu](https://setup.virtualhub.eu.org/tag/os/), a beginner-friendly distro.
{{< /alert >}}

On Windows, you need to place the `PDP15.exe` file you downloaded in [this tutorial](https://setup.virtualhub.eu.org/simh-pdp15#windows) in the VM folder. Then you can follow the above tutorial as usual. The shell script will not work on Windows. You need to rename it to `dos-15.bat`. Then you can double-click the file to launch the VM, no need to make it executable.

## Credits

- The disk image and other files used above are from a kit available on [SimH “Classic” website](http://simh.trailing-edge.com/).

## Video tutorial

Do you want to follow the tutorial by watching a video? We will post a video on our [youtube channel](https://www.youtube.com/@virtua1hub) soon.

Archives of this tutorial are available on [Wayback Machine](https://web.archive.org/web/*/https://virtualhub.eu.org/1970s/1970/dos-15/simh/).

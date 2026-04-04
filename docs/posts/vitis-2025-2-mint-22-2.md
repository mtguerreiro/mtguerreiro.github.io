---
icon: lucide/square-code
title: 'Running Vitis/Vivado 2025.2 on Linux Mint 22.2'
tags:
  - xilinx
  - mint
  - embedded-systems
---

Unfortunately, Linux Mint is not one of the officially supported operating systems for Vitis/Vivado, but we can get it to work with some extra steps.

## Preparing

- Install `libncurses-dev`
```sh
sudo apt-get install libncurses-dev
```

- Create symlinks to `lbtinfo.so.5` and `libncurses.so.5` (if they are missing, installation will hang)
```sh
sudo ln -s /usr/lib/x86_64-linux-gnu/libtinfo.so.6 /usr/lib/libtinfo.so.5
sudo ln -s /usr/lib/x86_64-linux-gnu/libncurses.so.6 /usr/lib/libncurses.so.5
```

## Download and install

- Download the Linux self extracting installer from the [Xilinx' download website](https://www.xilinx.com/support/download.html). Give execution permission to the downloaded `bin` file and execute it:
```sh
./FPGAs_AdaptiveSoCs_Unified_*_Lin64.bin
```

- Select what you must, make sure not to select acquire/manage license keys, select the installation path and wait until the installation finishes. For the installation path, I'd recommend choosing `~/tools/Xilinx`. This is the path assumed for the rest of this tutorial. 

    (Another option is to select "download image, install separately". This will first download and then install. This is useful if the process hangs, because you can execute things again without having to download anything. Technically Xilinx has an option to cancel the installation without deleting the downloaded files, but good luck with that.)

- To go the installation directory and checkout the `installLibs.sh` and install the missing libraries. The script can be found at:
```sh
~/tools/Xilinx/2025.2/Vitis/scripts
```

- Next, make sure to install the usb drivers (more info on the [official documentation](https://docs.amd.com/r/en-US/ug973-vivado-release-notes-install-license/Installing-Cable-Drivers) and also [thanks to Whitney](https://www.hackster.io/whitney-knitter/vivado-vitis-petalinux-2024-1-install-on-ubuntu-22-04-e76e91)). Go to the directory where you'll find the install script:
```sh
cd ~/tools/Xilinx/2025.2/Vivado/data/xicom/cable_drivers/lin64/install_script/install_drivers
```
Then, run 
```sh
sudo ./install_drivers
```

## Post install steps

- If you haven't added yourself to the dialout group before, you should also do it. You can check if you're part of the group by running
```sh
groups groups $USER
```
If not part of the group, add by running
```sh
sudo usermod -a -G dialout $USER
```
Note that you'll need to log out and in again for the changes to take effect.

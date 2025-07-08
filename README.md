ArchBSD-build
==============
Live media creator for ArchBSD distribution

## Introduction
The purpose of this tool is to quickly generate live images for ArchBSD.

## Features
* Build ArchBSD from packages
* Mate and XFCE desktop environments
* Hybrid DVD/USB image

## Graphics support
* Compatible with VirtualBox, VMware, NVIDIA graphics out of box
* SCFB support with automatic best resolution for UEFI enabled systems with Intel/AMD graphics

## System requirements
* Latest version of ArchBSD 
* 20GB of free disk space
* 4GB of free memory

Note: ArchBSD 22.01.12 and later should be used to build ISO.

## Initial setup
Install the required packages:

pkg install git transmission-utils rsync

Make sure to have linux64 kernel module loaded

kldload linux64
sysrc -f /etc/rc.conf kld_list="linux64"

Clone the repo:

git clone https://github.com/PersianBSD/ArchBSD.git

## Starting a build
#### Enter the directory for running the LiveCD build script:

cd ArchBSD


#### To build a ArchBSD with __MATE__ as default desktop

./build.sh -d mate -b unstable

or

./build.sh -d mate -b release


#### (Option) To build ArchBSD with __XFCE__ as default desktop

./build.sh -d xfce -b unstable
   



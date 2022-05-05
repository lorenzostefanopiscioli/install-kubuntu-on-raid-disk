# How to install Kubuntu 22.04 LTS on raid
This guide shows you a way to easily install [Kubuntu 22.04 LTS](https://kubuntu.org/getkubuntu/ "Kubuntu 22.04 LTS") (but it works for other Ubuntu flavors too) on a [RAID](https://en.wikipedia.org/wiki/RAID "RAID"). In this specific case I will install the operating system on SSD disks by setting a level 0 software raid.

## Introduction
The fundamental condition to consider is that a level 0 raid system (striping) tries to divide the data to be saved in equal parts over the number of disks of which it is composed (minimum 2).

If, for example, our Raid 0 consists of 2 disks, the data to be saved will be divided equally between the two disks. If they are 4 they will be divided equally between 4 disks, and so on.

The raids can be made with very fast dedicated hardware in the operations of managing the subdivision and recovery of data on the various disks, but also through software that can be installed in the system that perform the same task.

Normally the hardware systems are more performing, but the speed of the software raids for consumer-level computers is still very interesting. However, it should be noted that for each additional pair of disks added to a type 0 raid system, the overhead of management operations increases. So if you go from a single disk system to a raid 0 with 2 disks, don't expect a net doubling of performance. The same thing if you go from 2 to 4 disks, raid 0 will increase its performance but a little less than proportionally to the increase in the resources used.

### 1. Download Ubuntu Server 22.04 LTS
I realize this step can seem unexpected, but this is probably the basic idea for simplifying a raid installation. You should know that the server version of the Ubuntu installer comes with loaded software drivers that allow the creation, mounting and management of software raids: mdadm.

So let's start downloading the iso of [Ubuntu Server 22.04 LTS](https://cdimage.ubuntu.com/ubuntu-server/daily-live/current/jammy-live-server-amd64.iso "Ubuntu Server 22.04 LTS").

### 2. Creating an installation disk
Once we have the image file, in this step we will need to use this same file to create a boot disk for the system installer. I will give the example of how to create an installation disk from a Kubuntu system using the *Startup Disk Creator* application. Here you can read how to install this utility if it is not already present in your system: [how to install *Startup Disk Creator*](https://www.how2shout.com/linux/create-live-bootable-usb-using-ubuntu-20-04s-startup-disk-creator/ "how to install *Startup Disk Creator*").
If you have currently been using a Windows system, I suggest you use [*Rufus*](https://rufus.ie/en/ "*Rufus*").

For linux users, press the *CTRL + ALT + T* keys simultaneously. This will open a terminal window in the center of your screen. At the command line, type "usb-creator-gtk" and hit enter.

[![abc](abc "abc")](https://raw.githubusercontent.com/lorenzostefanopiscioli/install-kubuntu-on-raid-disk/main/guide-images/ubuntu-terminal.png "abc")



# How to Install RTL8821CE Driver On Fedora 34.
[Home Page](index.md)

[Disclamier](disclamier.md)

After Fedora 34 was installed if your pc has RTL8821ce Wifi card the OS can not use Wifi adaptor so you need to install the driver of the wifi card.

First of all *your pc should NOT be in Secure Boot mode.* You can disable it in BIOS menu.

## Step 1 Connect the internet without the Wifi Card

You can use ethernet cable or USB tethering function of your mobile phone. 

## Step 2 Make Sure that your PC using RTL8821CE Wifi Card.

Use `lspci | grep -i wireless` command to see if you are using RTL8821CE. 
You should see someting like  `1:00.0 Network controller: Realtek Semiconductor Co., Ltd. RTL8821CE 802.11ac PCIe Wireless Network Adapter`

## Step 3 Install the necessary tools.

Use `sudo dnf install build-essential linux-source bc kmod cpio flex libncurses5-dev libelf-dev libssl-dev` command to install necessary tools for kernel compiling process.

## Step 4 Download and Install Driver from Github.

First install Git with the help of `sudo dnf install git` command.
Download the Driver with `git clone https://github.com/tomaspinho/rtl8821ce` command.
Change directory with the help of `cd rtl8821ce`.
Then make executable the install file with the help of `chmod +x dkms-install.sh`.
Finally install the driver with `sudo ./dkms-install.sh` command.

##  Step 5 Activate the Driver.

Activate the driver with `sudo modprobe 8821ce` command.

## Step 6 Reboot Your PC.



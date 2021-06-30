# How to Install RTL8821CE Drivers On Fedora 34
[Home Page](index.md)
[Disclaimer](disclaimer.md)

After Fedora 34 was installed if your pc has RTL8821ce Wifi card the OS can not use Wifi adaptor so you need to install the driver of the wifi card.

## Step 1 Connect the internet without the Wifi Card

You can use ethernet cable or USB tethering function of your mobile phone. 

## Step 2 Make Sure that your PC using RTL8821CE Wifi Card

Use `lspci | grep -i wireless` command to see if you are using RTL8821CE 
You should see someting like  `1:00.0 Network controller: Realtek Semiconductor Co., Ltd. RTL8821CE 802.11ac PCIe Wireless Network Adapter`

## Step 3 Install the necessary tools

Use `sudo dnf install build-essential linux-source bc kmod cpio flex libncurses5-dev libelf-dev libssl-dev` command to install necessary tools for kernel compiling process.

## Step 4 


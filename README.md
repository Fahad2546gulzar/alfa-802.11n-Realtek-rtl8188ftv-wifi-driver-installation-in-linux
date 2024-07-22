# alfa-802.11n-Realtek-rtl8188ftv-wifi-driver-installation-in-linux
Hello In this tutorial we make installation for Realtek RTL8188FTV alfa wifi adapter drivers in linux.Follow all the steps and enjoy this method to avoid frustation.Feel free to ask anything if you have any issue.All steps are described below:
# Check for detection of wifi adapter
1. Type `ip a` in the terminal.Then check for `wlx` in the list shown.
2. (Alternatiely)If the above step does not work Then type `lsusb` in the terminal and check for `Realtek Semiconductor Corp. RTL8188FTV 802.11b/g/n 1T1R 2.4G WLAN Adapter`.
"Not" If you find nothing then you have mechanical failure.Try to replace your hardware.
# Update and Upgrade the system
After detection of device successfully.Then update and upgrade your system as follows.
- For updation
  `sudo apt update`
- For upgrade
   `udo apt upgrade`
# Install dependencies
`sudo apt install build-essential dkms git`
# Download driver files
After installing dependencies.Download driver files as: 
 `git clone https://github.com/kelebek333/rtl8188fu`
# Build and install drivers
`cd rtl8188fu
sudo dkms add .
sudo dkms build rtl8188fu/1.0
sudo dkms install rtl8188fu/1.0`
# Load module
`sudo modprobe rtl8188fu`
# Checking module
After load module check for working as `lsmod | grep rtl8188fu`.

Thats it you have installed it successfully now go to settings>Wifi option and connect to wifi.
If you are in trouble feel free to contact me on g3388610@gmail.com


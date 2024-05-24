## Realtek WiFi/Bluetooth drivers (RTL8852CE)

For this tutorial, you may need to hook up your phone and tether it to your PC, as to allow it to access the internet (See https://support.google.com/pixelphone/answer/2812516?hl=en for Android)

These drivers are very confusing and frustracting to install, as it seems like nothing works, but there's a very simple fix, use DKMS

Script:

```sh
sudo apt update
sudo apt install make gcc linux-headers-$(uname -r) build-essential git dh-sequence-dkms debhelper build-essential devscripts git-build-recipe
git clone https://github.com/lwfinger/rtw89.git
cd rtw89
git deborig HEAD
dpkg-buildpackage -us -uc
sudo apt install ../rtw89-dkms*.deb 
```

Once finished, you should be able to connect to WiFi and Bluetooth!

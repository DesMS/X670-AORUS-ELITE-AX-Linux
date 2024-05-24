## RGB Controller for Gigabyte X670 AORUS ELITE AX

This will use OpenRGB, as Gigabyte does not provide drivers for Linux, and thus does not provide their software.

Script to install OpenRGB:

```sh
wget https://openrgb.org/releases/release_0.9/openrgb_0.9_amd64_bookworm_b5f46e3.deb
sudo apt install ./openrgb*.deb
```

Once you have it installed, you can run `openrgb`, and it will open the program. It should be autoconfigured for you, so you can just control the RGB straight away!

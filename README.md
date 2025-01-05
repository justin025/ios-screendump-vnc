# Install

1. Download the latest `.deb` package from GitHub actions:
https://github.com/BenEdridge/ios-screendump-vnc/actions
2. Upload packages from the `screendump/packages/*.deb` directory to your device
3. Install with package manager like Sileo or use `dpkg` manually
4. Restart Springboard or Soft Reboot


# Build

1. Install https://theos.dev
2. `cd screendump` (screendumpLowFrame has not been fixed yet)
3. Run `make package`
4. Upload packages from the `screendump/packages/*.deb` directory to your device
5. Install with package manager like Sileo or use `dpkg` manually

# Tips

- Check logs for errors using: `idevicesyslog -m screendumpd`
- Use `nmap` to check if the VNC server is actually running: `sudo nmap <ip> -p 5900`
- Set a lower resolution and colour depth
- Try an alternative VNC client  clients ([Remmina](https://remmina.org/) or [RealVNC](https://www.realvnc.com/en/connect/download/viewer/))
- For a superior connection consider connecting over USB with reverse USB tethering: https://github.com/libimobiledevice/libimobiledevice/issues/1348

# Acknowledgements

Based on recent changes by wh1te4ever https://gitlab.com/alias20/screendump to support iOS 14+
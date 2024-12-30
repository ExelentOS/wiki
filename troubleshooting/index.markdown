---
layout: default
title: Troubleshooting
nav_order: 5
---

# ExelentOS Troubleshooting Guide

This guide provides technical troubleshooting steps for common issues you might encounter while using ExelentOS. For advanced details, refer to the [Arch Wiki](https://wiki.archlinux.org/).

tip: if you see anything encased in 
```
this
```
it means you have to use a terminal(Ctrl+alt+t) unless otherwise noted


> note: this is more technical, if there really is something you don't understand, then create an issue on [Github](https://github.com/exelentos/exelentos-iso/issues)

---

## Desktop Environment Issues

### Desktop Environment Not Loading
1. Open a terminal with `Ctrl + Alt + T` or switch to a TTY with `Ctrl + Alt + F2`.
2. Log in and restart the display manager:
   ```bash
   sudo systemctl restart sddm
   ```
3. If the issue persists, check the status of the display manager:
   ```bash
   systemctl status sddm
   ```
4. Review logs for errors:
   ```bash
   journalctl -xe | grep sddm
   ```

---

## Driver and Hardware Issues

### Graphics Drivers Not Working
1. Open a terminal with `Ctrl + Alt + T`.
2. Check installed drivers:
   ```bash
   mhwd -li
   ```
3. List available drivers:
   ```bash
   mhwd -l
   ```
4. Install the recommended driver:
   ```bash
   sudo mhwd -a pci nonfree 0300
   ```
5. Reboot your system:
   ```bash
   sudo reboot
   ```

### Wi-Fi Not Connecting
1. Check Wi-Fi device status:
   ```bash
   nmcli device
   ```
2. Restart the network service:
   ```bash
   sudo systemctl restart NetworkManager
   ```
3. Reconnect to your Wi-Fi network:
   ```bash
   nmcli device wifi list
   nmcli device wifi connect <SSID> password <password>
   ```

---

## Software and Package Management

### Applications Not Launching
1. Verify the application is installed:
   ```bash
   pacman -Q <application-name>
   ```
2. Reinstall the application:
   ```bash
   sudo pacman -S <application-name>
   ```
3. Check application logs by running it in the terminal:
   ```bash
   <application-name>
   ```

### System Update Fails
1. Clear the package cache:
   ```bash
   sudo pacman -Scc
   ```
2. Synchronize package databases:
   ```bash
   sudo pacman -Syyu
   ```
3. If a keyring error occurs, refresh the keyring:
   ```bash
   sudo pacman-key --refresh-keys
   ```

---

## Display Issues

### Resolution Not Detected
1. Identify connected monitors:
   ```bash
   xrandr
   ```
2. Set the resolution manually:
   ```bash
   xrandr --output <monitor-name> --mode <resolution>
   ```
3. Save changes by editing the configuration file:
   ```bash
   nano ~/.xprofile
   ```
   Add the `xrandr` command from step 2 and save.

---

## Miscellaneous

### Logs and Diagnostics
1. System logs:
   ```bash
   journalctl -p 3 -xb
   ```
2. Boot issues:
   ```bash
   journalctl -b
   ```
3. Hardware information:
   ```bash
   lspci -v
   ```

---

Again, for detailed technical guidance, visit the [Arch Wiki](https://wiki.archlinux.org/).

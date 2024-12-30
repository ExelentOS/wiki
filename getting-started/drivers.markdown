---
layout: default
title: Drivers
parent: Getting Started
nav_order: 2
---

# ExelentOS Drivers

ExelentOS is designed to support a wide range of hardware to ensure compatibility and ease of use for new users. This guide provides simple steps to install drivers for various devices based on your hardware.

tip: if you see anything encased in 
```
this
```
it means you have to use a terminal(Ctrl+alt+t) unless otherwise noted

---

## Graphics Drivers

If you have one of the following graphics cards, install the respective driver package:

- **NVIDIA**:
  1. Open the **Driver Manager** from System Settings.
  2. Select the recommended driver (usually labeled "NVIDIA proprietary driver").
  3. Click **Apply Changes** and reboot.
  4. Alternatively, install manually:
     ```bash
     sudo pacman -S nvidia
     ```

- **AMD**:
  1. AMD GPUs are typically supported out of the box with the open-source AMDGPU driver.
  2. If you experience issues, install the driver manually:
     ```bash
     sudo pacman -S xf86-video-amdgpu
     ```

- **Intel**:
  1. Intel integrated graphics are supported automatically.
  2. For additional utilities:
     ```bash
     sudo pacman -S intel-media-driver
     ```

---

## Audio Drivers

- **Realtek**: Most Realtek audio devices are supported out of the box. If sound issues persist:
  ```bash
  sudo pacman -S alsa-utils pulseaudio
  ```
  Open **Audio Settings** to configure your device.

- **Intel HD Audio**: Supported natively. Ensure you have PulseAudio installed:
  ```bash
  sudo pacman -S pulseaudio
  ```

---

## Network Drivers

### Wi-Fi

- **Realtek or Broadcom Wi-Fi Chipsets**:
  1. Open the **Driver Manager** to check for available proprietary drivers.
  2. Install the recommended driver and reboot.
  3. Alternatively, for Realtek:
     ```bash
     sudo pacman -S rtl8821ce-dkms
     ```

- **Intel Wi-Fi**:
  Intel Wi-Fi drivers are pre-installed. If connectivity issues occur, install:
  ```bash
  sudo pacman -S iwlwifi
  ```

### Ethernet

- Most Ethernet controllers (Realtek, Intel) work out of the box. If needed:
  ```bash
  sudo pacman -S r8168
  ```

---

## Printer Support

1. Open **Printers** in System Settings.
2. Add a new printer and select the appropriate driver.
3. Install additional drivers if prompted:
   ```bash
   sudo pacman -S cups gutenprint
   ```

---

## Troubleshooting Driver Issues

1. Open a terminal with `Ctrl + Alt + T`.
2. Check hardware information:
   ```bash
   lspci -v
   ```
3. If a driver is missing, install it using the package manager (as outlined above).

---

## Additional Resources

For advanced troubleshooting and detailed driver configurations, visit the Arch Wiki:
- [NVIDIA Drivers](https://wiki.archlinux.org/title/NVIDIA)
- [AMDGPU Drivers](https://wiki.archlinux.org/title/AMDGPU)
- [Intel Graphics](https://wiki.archlinux.org/title/Intel_graphics)
- [Realtek WiFi](https://wiki.archlinux.org/title/Network_configuration/Wireless#Realtek)


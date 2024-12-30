---
layout: default
title: Getting Started
nav_order: 1
---

# Getting Started with ExelentOS

Welcome to ExelentOS! This guide will help you set up and explore your new system. Whether you are installing ExelentOS for the first time or looking for tips to enhance your experience, this guide has you covered.

---

## Table of Contents

- [Downloading the ISO](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#downloading-the-iso)
- [Creating Bootable Media](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#creating-bootable-media)
- [Booting ExelentOS](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#booting-exelentos)
- [Exploring the Live Environment](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#exploring-the-live-environment)
- [Installing ExelentOS](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#installing-exelentos)
- [Post-Installation Setup](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#post-installation-setup)
- [Next Steps](https://github.com/exelentos/exelentos-iso/wiki/Getting-Started#next-steps)

---

## Downloading the ISO

1. Visit the [ExelentOS ISO Download page](https://exelentos.github.io).
2. Download the latest stable ISO file.
3. Verify the integrity of the downloaded ISO using the provided checksums.

---

## Creating Bootable Media

To install ExelentOS, you need a bootable USB drive:

### Windows:
- Use [Rufus](https://rufus.ie/):
  1. Open Rufus and select your USB drive.
  2. Choose the downloaded ExelentOS ISO file.
  3. Click "Start" to create the bootable drive.

### Linux:
- Use the `dd` command:
  ```bash
  sudo dd if=/path/to/exelentos.iso of=/dev/sdX bs=4M status=progress && sync
  ```
  Replace `/dev/sdX` with the correct USB drive.

---

## Booting ExelentOS

1. Insert the bootable USB drive into your computer.
2. Restart your computer and enter the boot menu (usually by pressing keys like `F12`, `Esc`, or `Del` during startup).
3. Select the USB drive from the boot options.
4. Choose the **Live Boot** option to load ExelentOS.

---

## Exploring the Live Environment

The Live Environment allows you to try ExelentOS before installing it:

- Explore the KDE Plasma 6 desktop environment.
- Open applications to ensure compatibility with your hardware.
- Test Wi-Fi, audio, and other system components.

---

## Installing ExelentOS

1. Click the **Install ExelentOS** icon on the desktop.
2. Follow the step-by-step installation wizard:
   - Choose your preferred language.
   - Set up partitions (automatic or manual).
   - Create a user account.
   - Select your time zone and keyboard layout.
3. Complete the installation and reboot the system when prompted.

> for a more in-depth installation process, visit the [installation page](https://github.com/exelentos/exelentos-iso/wiki/Installation-Guide)

---

## Post-Installation Setup

After rebooting into your newly installed ExelentOS:

1. **Update the System**:
   ```bash
   sudo pacman -Syu
   ```
2. **Install Additional Software**:
   Use the built-in package manager or the command line to install your favorite applications.
3. **Set Up Drivers**:
   - For NVIDIA GPUs: Install the proprietary driver:
     ```bash
     sudo pacman -S nvidia nvidia-utils
     ```
   - For other hardware, refer to the [driver guide](https://github.com/exelentos/exelentos-iso/wiki/Drivers).

---

## Next Steps

Now that ExelentOS is up and running, you can:

- Personalize your desktop by customizing themes and widgets.
- Explore pre-installed applications.
- Learn about advanced features in the [User Guide](https://github.com/exelentos/exelentos-iso/wiki/User-Guide).

---

If you encounter issues, check the [Troubleshooting Guide](https://github.com/exelentos/exelentos-iso/wiki/Troubleshooting) or reach out via [GitHub Issues](https://github.com/exelentos/exelentos-iso/issues).

Enjoy your experience with ExelentOS!

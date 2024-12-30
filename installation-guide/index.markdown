---
layout: default
title: Installation Guide
nav_order: 2
---

# ExelentOS Installation Guide

Welcome to the ExelentOS Installation Guide! This document provides detailed, step-by-step instructions for installing ExelentOS using the user-friendly Calamares installer. Follow along to get ExelentOS running on your system in no time.

---

## Prerequisites

Before starting the installation, ensure you have the following:

1. **System Requirements:**
   - 2 GHz dual-core processor or better.
   - 4 GB of RAM (8 GB recommended).
   - 20 GB of free disk space.
   - A USB port or DVD drive for installation media.

2. **Installation Media:**
   - A bootable USB or DVD with the ExelentOS ISO. Refer to the [Getting Started Guide](../getting-started) for instructions on creating bootable media.

3. **Data Backup:**
   - Back up all important files to avoid data loss during installation.

---

## Starting the Installer

1. Insert the ExelentOS bootable USB or DVD into your computer.
2. Boot your computer and select **Live Boot** from the boot menu.
3. Once the ExelentOS desktop loads, locate and click on the **Install ExelentOS** icon or use the welcome app to start the Calamares installer.

---

## Installation Steps

### 1. Welcome Screen

- Select your preferred language from the list.
- Click **Next** to proceed.

### 2. Location

- Choose your region and timezone from the interactive map or dropdown menus.
- Click **Next**.

### 3. Keyboard Layout

- Select your keyboard layout and test it in the provided text box.
- Click **Next**.

### 4. Partitioning

Calamares provides two primary partitioning methods:

- **Erase Disk:** Automatically configure partitions for you. This is the recommended option for most users.
- **Manual Partitioning:** For advanced users who want custom partition layouts.

> **Note:** When choosing manual partitioning, ensure you create at least the following partitions:
> - Root (`/`): Minimum 15 GB.
> - Swap (optional): Recommended if your system has limited RAM.
> - Home (`/home`, optional): For storing personal files.

- After selecting your partitioning method, click **Next**.

### 5. User Setup

- Enter your full name, desired username, and a secure password.
- Optionally, enable automatic login for convenience.
- Click **Next**.

### 6. Summary

- Review the installation summary to ensure all options are correct.
- Click **Install** to begin the installation process.

### 7. Installation Progress

- The installer will copy files and set up ExelentOS on your computer. This step may take several minutes. Feel free to explore the live environment while you wait.

### 8. Finish Installation

- Once the installation completes, click **Restart Now** to reboot your computer into the newly installed ExelentOS.

---

## Post-Installation

Congratulations! ExelentOS is now installed on your system. Here are some recommended next steps:

1. **Update Your System:**
   click on the update pacman packages

2. **Install Additional Software:**
   Use the package manager to explore and install software tailored to your needs.

3. **Configure Settings:**
   Adjust system preferences, install drivers, and customize your environment.

For further guidance, check out the [Getting Started Guide](../getting-started).

---

## Troubleshooting

If you encounter any issues during installation, refer to the [Troubleshooting Guide](../troubleshooting) or submit a query via [GitHub Issues](https://github.com/exelentos/exelentos-iso/issues).

---

Enjoy your journey with ExelentOS!

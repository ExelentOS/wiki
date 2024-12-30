---
layout: default
title: FAQ
nav_order: 4
---

# ExelentOS FAQ (Frequently Asked Questions)

Here are answers to common questions and troubleshooting tips for ExelentOS users:

---

## General Troubleshooting

### The desktop environment is not loading after boot.
1. **Restart the Display Manager:**
   - Press `Ctrl + Alt + F2` to switch to a terminal interface.
   - Log in and restart the display manager by running:
     ```bash
     sudo systemctl restart sddm
     ```
   - If the issue persists, reboot your computer.

2. **Check Graphics Drivers:**
   - Open the Driver Manager from System Settings and ensure the correct graphics drivers are installed.

---

### Apps are not appearing in the menu.
1. **Refresh the Application Menu:**
   - Log out of your session and log back in to reload the menu.
2. **Check Installed Apps:**
   - Open the Software Center and search for the app to ensure it is properly installed. Reinstall if necessary.
3. **Update Application Settings:**
   - Go to System Settings > Applications > Menu Editor and verify that the app is not hidden.

---

## Display and Graphics

### The screen resolution is incorrect or not detected.
1. **Adjust Resolution Settings:**
   - Open System Settings > Display and Monitor and manually set the resolution.
2. **Verify Drivers:**
   - Open the Driver Manager from System Settings and ensure GPU drivers are installed and updated.

---

### External monitor is not detected.
1. **Detect Displays:**
   - Open System Settings > Display and Monitor and click "Detect Displays."
2. **Reconnect Cables:**
   - Ensure all cables are securely connected, and the monitor is powered on.

---

## Software and Updates

### An app is not launching.
1. **Reinstall the App:**
   - Open the Software Center, uninstall the app, and reinstall it.
2. **Check Default Applications:**
   - Open System Settings > Applications > Default Applications to ensure proper configuration.
3. **Check File Permissions:**
   - Right-click the app’s executable file, open Properties, and ensure "Allow executing file as program" is enabled.

---

## System Updates

### The system is not updating or shows an error.
1. **Check Internet Connection:**
   - Open a browser to verify your connection.
2. **Update System:**
   - Open Discover, refresh the package list, and apply updates.
3. **Switch Update Servers:**
   - Go to System Settings > Software Sources and select a different mirror.

---

## Other Common Issues

### Sound is not working.
1. **Check Volume Levels:**
   - Open System Settings > Audio and ensure the volume is turned up and not muted.
2. **Select Output Device:**
   - In Audio settings, verify the correct output device is selected.

---

### Wi-Fi is not connecting.
1. **Reconnect to the Network:**
   - Click the network icon in the system tray, select your Wi-Fi network, and re-enter the password if prompted.
2. **Restart Network Manager:**
   - Open System Settings > Network and toggle Wi-Fi off and on again.

---

### Printer is not detected.
1. **Add a Printer:**
   - Open System Settings > Printers and click "Add Printer." Follow the prompts to install drivers if necessary.
2. **Verify Printer Connection:**
   - Ensure the printer is powered on and connected to the same network or directly via USB.

---

For more detailed support, open an issue on [GitHub](https://github.com/exelentos/exelentos-iso/issues).

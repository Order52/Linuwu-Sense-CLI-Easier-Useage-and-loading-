# Linuwu-Sense Launcher

A streamlined Bash-based frontend for managing PredatorSense-like features on Linux systems, using the **Linuwu-Sense** kernel module.

> **Fork of** [0x7375646F/Linuwu-Sense](https://github.com/0x7375646F/Linuwu-Sense)  
> Huge thanks to **sudo / 0x7375646F** for bringing PredatorSense to Linux!

This launcher script was developed (with some help from AI 😎) to provide a **clean, user-friendly, menu-driven interface** for configuring system-level features via the `linuwu_sense` kernel module.

---

## 📸 Preview

Here’s what the tool looks like in action:

![image](https://github.com/user-attachments/assets/61cd9260-3b39-4303-aade-3271d16cc56a)


---

## 🧩 Features

Easily control and monitor:

- ✅ Keyboard Backlight Timeout
- 🔋 Battery Charge Limiter
- 🎵 Boot Animation and Sound
- 🌬️ Fan Speeds (Auto, Quiet, Balanced, Performance, Turbo, Custom)
- 💡 LCD Override
- ⚡ USB Charging Thresholds
- 🔧 Battery Calibration

All through a terminal interface, backed by SysFS and requiring root access.

---

## 🚀 Usage

### 1. Prerequisites

- Linux kernel module: `linuwu_sense.ko`
- Compatible Acer Predator laptop
- Root privileges (the script will attempt to elevate with `sudo`)

> ⚠️ You **must load** the Linuwu-Sense kernel module before using this script.
### 🧱 Step 1: Install Kernel Headers

**On Arch Linux:**

```bash
sudo pacman -S linux-headers
```
### 🛠️ Step 2: Clone and Build the Module
  ```bash
git clone https://github.com/Order52/linuwu-sense-cli.git
cd linuwu-sense-cli
make install
```
⚠️ This will remove the default acer_wmi module and load the patched version from Linuwu-Sense.
Make sure to run with sudo if needed.

⚙️ Using Clang Instead?
  ```bash
sudo make CC=clang LD=ld.lld install
```
🔄 To Uninstall

  ```bash
make uninstall
```

### Then Run the Script

```bash
chmod +x Linuwu-sense-cli.sh
sudo ./Linuwu-sense-cli.sh

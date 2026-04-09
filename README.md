# Openwrt for MediaTek/Airoha EN751627 based chips ( tested on DX-3301 and EX3301 Routers) 

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](LICENSE)
[![Release](https://img.shields.io/github/v/release/yourusername/zyxel-matrix-wsr30)](https://github.com/majad00/DX-EX3310-T0_Openwrt_Hybrid/releases/tag/V-15)
[![Downloads](https://img.shields.io/github/downloads/yourusername/zyxel-matrix-wsr30/total)](https://github.com/majad00/DX-EX3310-T0_Openwrt_Hybrid/releases/download/V-15/DX-EX3301-T0_Openwrt_Zyxel-Matrix-v-15.zip)

The Zyxel-Matrix, Functional Openwrt Port for DX EX-3301 is developed using Imagebuilder,around the integrates proprietary utilities that are already available on your router. The open-source components are distributed under the GPL V2 license. 
👉 Most of the proprietary utilities will remain accessible even after transitioning to the Zyxel-Matrix.
👉 You have the flexibility to revert to original router status at any time by using Rollback firmware. Also, updating to the latest Zyxel firmware is possible through LUCI interface in Zyxel-Matrix.

## ✨ Features  Full functional Openwrt 
- **Easy Installation** - No UART or disassembly required! Install from Web interface
- **MSSID** - Router support Multiple SSIDs
- **Full Luci Interface** - Manage your router through any browser
- **Advanced Radio Control** - Control over all available Radios
- **SSH Access** - for lowe level tasks
- **Root access** - Zyxel-Matrix OS with full previliges (No Password or 1234)
- **pre compiled** - cross-compiled binary ready to install
- **Roll Back** - Openwrt Sysupgrade can flash OEM firmware to router

## 📥 Quick Download

👉 **[Download Latest Release](https://github.com/majad00/DX-EX3310-T0_Openwrt_Hybrid/releases/download/V-15/DX-EX3301-T0_Openwrt_Zyxel-Matrix-v-15.zip)**
sha256:d576cdc73309a6c9ad63ccfaef6e9adcffd1f7fb3be36d792ce0cd82536057ed
The download includes:
- `openwrt-15.5-zyxel-matrix-v-15-squashfs-sysupgrade.bin` - Zyxel-Matrix for DX3301-T0 and EX3301-T0
- `zyxel-3.3-squashfs-rollback.bin` - Roll Back to Zyxal factory firmware
- `README.txt` - Complete instructions
- `CHANGELOG.txt` - Version history
- `docs` - for detail documentations and installation
  
## 🚀 Flashing in 2 minutes 

1. **Connect** Ethernet cable from PC to router
2. **Login to router**: Login to OEM Zyxel router through web
3. **Flash**: From drop down menu Select Maintenance → click Firmware Upgrade
4. **Wait** 2-3 minutes for first boot
5. **Connect WiFi**: `Zyxel_Matrix` / `12345678` ( Enable through LUCI)
6. **Configure**: http://192.168.1.1 (root/no passwrod or 1234)

> ⚠️ **IMPORTANT**: Change password after first boot!, on successfull boot the power LED will blink RED for a second
> ⚠️ **Optional**: After flashing Zyxel-Matrix, please reset to make sure previous Zyxel settings removed

## 🚀 Flashing using UART (safe for testing release)
1. **Connect** Using TX, RX and GND, rename the firmware to RAS.bin (optional)
2. **Get to Shell**: Intrupt boot process by pressing any button, rename the firmware 
3. **Flash**: ATUR RAS.bin ( router will start a tftp server and wait for the file), send that RAS.bin file using TFTP.
4. **Wait** Bootloader will take file and write to proper offsets, router will reboot, wait for 2-3 minutes for first boot

## 📋 Detailed Documentation

- [Building from Source](docs/build_guide.md)
- [Changelog](CHANGELOG.txt)

## 🔧 Default Settings

| Mode | IP Address | WiFi SSID | WiFi Password | Login |
|------|------------|-----------|---------------|-------|
| **AP Mode** | 192.168.1.1 | Zyxel_Matrix | 12345678 | root/1234 |

## 🛠️ Development

This project include busybox based on OpenWrt. To build from source:
See Source, for installing precompiled firmware see Release,

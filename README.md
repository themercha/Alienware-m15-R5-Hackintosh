# Alienware m15 R5 Hackintosh – macOS Ventura (Ryzen 9 + iGPU)

This project shares a working OpenCore EFI folder and setup notes for running macOS Ventura on the **Alienware m15 R5** with **Ryzen 9 5900HX** and **RTX 3070** (iGPU only).

When I built this setup, there weren’t many resources available for this hardware combo, so I’m sharing my EFI here in hopes it helps someone else.

---

## 💻 Hardware Specs

| Component      | Details                              |
|----------------|--------------------------------------|
| CPU            | AMD Ryzen 9 5900HX                   |
| GPU            | NVIDIA RTX 3070 (disabled)           |
| iGPU           | Radeon Vega (enabled via nootedred)  |
| RAM            | 16 GB DDR4                           |
| Storage        | 1 TB NVMe SSD                        |
| Wi-Fi          | Internal module (fully working)      |
| Bluetooth      | Internal module (fully working)      |
| Ethernet       | Internal module (fully working)      |
| Display        | 15.6" 1080p (limited to 60Hz only)   |

---

## 🖥️ macOS Version

- Tested only on **macOS Ventura** (e.g., 13.x)

---

## ✅ What Works

- ✅ Internal display (iGPU + nootedred, max 60Hz)
- ✅ USB ports
- ✅ Trackpad
- ✅ Wi-Fi (original internal card)
- ✅ Bluetooth (original internal card)
- ✅ Ethernet
- ✅ Sleep/Wake (partial)

---

## ❌ Known Issues / Limitations

- ❌ NVIDIA GPU – not supported (disabled)
- ❌ HDMI output – not functional with iGPU
- ❌ Internal display limited to 60Hz
- ❌ Audio – not working (AppleALC did not help)
- ❌ Brightness control keys – non-functional (manual only)

---

## ⚙️ Installation Notes

- **OpenCore version:** 0.xx *(replace with your actual version)*
- ⚠️ **During installation, use `WhateverGreen.kext`, not `nootedred.kext`**  
  → `nootedred.kext` should only be added **after macOS is fully installed**  
  → Using it during install may cause black screen or kernel panics.
- AMD kernel patches applied based on [Dortania's AMD Vanilla Guide](https://dortania.github.io/AMD-CPU/).
- BIOS settings:
  - Secure Boot: Disabled
  - Fast Boot: Disabled
  - CSM: Disabled

---

## 🧩 Credits & Resources

- [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)

---

## 📌 Final Notes & Disclaimer

> ⚠️ This EFI was created and tested only on **macOS Ventura**, using an Alienware m15 R5 with Ryzen 9 5900HX and iGPU via nootedred.  
> I no longer own the machine, so **I cannot provide future updates or test support**.  
> Compatibility with newer macOS versions is **not guaranteed** — use at your own risk.

> Please make backups before using. Contributions are welcome. Good luck!

---

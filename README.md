# Realtek USB Wi-Fi Adapter (802.11 b/g/n)

Patched `RtWlanU.kext` for **Wireless-USB-Big-Sur-Adapter**

This repository provides a **patched version of `RtWlanU.kext`** for Realtek USB Wi-Fi adapters, based on **chris1111’s Wireless-USB-OC-Big-Sur-Adapter**.

The patch improves **boot performance and stability** on some systems while keeping Wi-Fi fully functional.

---

## ✅ What This Fixes

- Improved compatibility for **RTL8188FTV**
- Long boot delays when a Realtek USB Wi-Fi adapter is connected
- Repeated USB timeout messages during startup
- Slow system initialization before login

Wi-Fi functionality remains unchanged.

---

## 🧩 Supported Devices

- Realtek USB Wi-Fi adapters  
- Tested with:
  - **Vendor ID:** `0x0BDA` (Realtek)
  - **Product ID:** `0xF179`

Other Realtek USB adapters may also benefit.

---

## 🖥 Tested macOS Versions

- macOS Big Sur  
- macOS Monterey  
- macOS Ventura  
- macOS Sonoma  

(OpenCore recommended)

---

## 📦 Installation

1. Download and install the original package from:  
   https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter

2. After installation, **remove the original `RtWlanU.kext`** from:
   - `/Library/Extensions` **or**
   - `EFI/OC/Kexts`

3. Copy the **patched `RtWlanU.kext`** from this repository to the same location.

4. Rebuild kernel cache and reboot:
   ```bash
   sudo kmutil install --volume-root / --update-all
   sudo reboot

⚠️ Notes

This patch does not add new macOS Wi-Fi features
Intended only for Realtek USB Wi-Fi adapters that already work but cause slow boot
If your system boots normally with the original kext, you do not need this version

🙏 Credits
Original project and installer: chris1111

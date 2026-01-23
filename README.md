
This repository contains the OpenCore EFI folder for HP ProDesk 400 G2 MT

Running macOS [ElCapitan - Montorey].<br>
iMac14,2 = ElCapitan -> Mojave<br>
iMac14,4 & Macmini7,1 = BigSur -> Montorey<br>
* Montorey with OCLP<br>

---

## 💻 System Specs
* **CPU:** [Intel Core i5-4160]
* **iGPU:** [Intel HD Graphics 4400]
* **RAM:** [4GB DDR3]
* **OpenCore Version:** [1.0.6.] NOV 2025

---

## ✅ What's Working?
* [x] HD Graphics
* [x] Audio [alcid=15]
* [x] Ethernet
* [x] PowerOff / Reboot
* [x] USB Ports (Mapped)
* [x] iMessage & FaceTime
**- Tested with USB TP-Link TL-WN725<br>
**- ELCapitan-Mojave  (https://www.tp-link.com/my/support/download/tl-wn725n/)<br>
**- BigSur-Montorey (https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)<br>


## ❌ Not Working
* [ ]

---

## 🛠️ Instructions
1. **SMBIOS:** 
Generate your own Mac Devices (https://github.com/corpnewt/GenSMBIOS)<br>
a) SystemProductName	x3	Line.614, 621, 644.<br>
b) SystemSerialNumber	x4	Line.623, 646, 663, 718.<br>
c) SystemUUID			x4	Line.620, 625, 648, 665.<br>
d) MLB					x2	Line.638, 661.<br>
e) ROM					x2	Line.632, 659.<br>
* PASTE SMBIOS to ChatGPT and ask him to generate basic Config.plist<br>

2. Ethernet KEXT (https://github.com/Mieze/RTL8111_driver_for_OS_X)
* El-Capitan RealtekRTL8111.kext v2.2.1
* High Sierra RealtekRTL8111.kext v2.2.2
* Big Sur-Montorey RealtekRTL8111.kext v3.0.0

3. **BIOS Settings:** - **Disable:** Secure Boot, CFG-Lock, VT-d, Fast Boot.<br>
   - **Enable:** AHCI, UEFI, VT-x.<br>
   
4. Copy the EFI folder to your ESP (EFI System Partition) after finish Setup macOS.

---

## 📸 Screenshots
<p align="center">
  <img src="https://refreshedbyus.com/media/catalog/product/cache/3893dbf8474ca4567d4cc8d34804c0cf/h/p/hp_prodesk_400_g2_mt_front.jpg" width="45%" />
  <img src="https://raw.githubusercontent.com/suaji/Opencore-HP-ProDesk-400-G2-MT/refs/heads/main/Catalina.png" width="45%" />
</p>

---

## Credits
* [Acidanthera](https://github.com/acidanthera) for OpenCore.
* [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) for the guide.
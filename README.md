
This repository contains the OpenCore EFI folder for HP ProDesk 400 G2 MT

Running macOS [ElCapitan - Montorey].<br>
iMac14,2 = ElCapitan -> Mojave<br>
iMac14,4 & Macmini7,1 = BigSur -> Montorey<br>
* Montorey with OCLP<br>

---

## 💻 System Specs
* **CPU:** [Intel Core i5-4150]<br>
* **iGPU:** [Intel HD Graphics 4400]<br>
* **RAM:** [4GB DDR3]<br>
* **OpenCore Version:** [1.0.6.] NOV 2025<br>

---

## ✅ What's Working?
* [x] HD Graphics 4400<br>
* [x] Audio [alcid=15]<br>
* [x] Ethernet<br>
* [x] PowerOff / Reboot<br>
* [x] USB Ports (Mapped)<br>
* [x] iMessage & FaceTime<br>
**- Tested with USB TP-Link TL-WN725<br>
**- ELCapitan-Mojave  (https://www.tp-link.com/my/support/download/tl-wn725n/)<br>
**- BigSur-Montorey (https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)<br>


## ❌ Not Working
* [ ]<br>

---

## 🛠️ Instructions
0. **TIPS<br>
-> Start with Catalina (use offline image "createinstallmedia" for USB2. *OpenCore USB1<br>
-> Use 2nd HDD/SSD if you install Windows in 1st HDD/SDD. Opencore autodetect HDD / Partition Windows.<br>

1. **SMBIOS:<br>
Generate your own Mac Devices (https://github.com/corpnewt/GenSMBIOS)<br>
a) SystemProductName	x3	Line.614, 621, 644.<br>
b) SystemSerialNumber	x4	Line.623, 646, 663, 718.<br>
c) SystemUUID			x4	Line.620, 625, 648, 665.<br>
d) MLB					x2	Line.638, 661.<br>
e) ROM					x2	Line.632, 659.<br>
* PASTE SMBIOS to ChatGPT and ask him to generate basic Config.plist<br>

2. **Ethernet KEXT (https://github.com/Mieze/RTL8111_driver_for_OS_X)<br>
* El-Capitan RealtekRTL8111.kext v2.2.1<br>
* High Sierra RealtekRTL8111.kext v2.2.2<br>
* Big Sur-Montorey RealtekRTL8111.kext v3.0.0<br>

3. **BIOS Settings:<br>
   - *Disable:** Secure Boot, CFG-Lock, VT-d, Fast Boot.<br>
   - *Enable:** AHCI, UEFI, VT-x and Data Execution Prevention<br>
   
4. **Copy the EFI folder to your ESP (EFI System Partition) after finish Setup macOS.<br>

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
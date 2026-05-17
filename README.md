**VBMeta AVB Disable Patch Set – Infinix Note 30 VIP (X6710) | Android 14**

---

## 📄 Description

This release contains **AVB (Android Verified Boot) disable vbmeta patch images** for the **Infinix Note 30 VIP (X6710)**.

These images are generated using **avbtool.py** and are modified to **disable AVB verification enforcement** for development purposes such as:

* Custom ROM installation
* GSI testing
* Root / system modification development

⚠️ **Important Warning**

* This does NOT permanently remove AVB, it only disables verification enforcement
* Incorrect flashing may cause bootloop
* Warranty may be affected
* **Use at your own risk**

---

## 📁 Included Files

* `vbmeta_disable.img` (main AVB disable patch)
* `vbmeta_system_disable.img` (system partition AVB disable)
* `vbmeta_vendor_disable.img` (vendor partition AVB disable)

---

## 📱 Device Support

* Infinix Note 30 VIP
* Model: **X6710**
* Android 14 build: **X6710-H931DJ-U-GL-241029V827**

---

## ⚙️ How to Use (Flashing Guide)

### 🔓 Requirements

* Bootloader must be **UNLOCKED**
* ADB & Fastboot installed (platform-tools)
* USB debugging enabled

---

## 💻 Step 1: Boot to Fastboot

```bash
adb reboot bootloader
```

---

## 💾 Step 2: Flash VBMeta Disable Files

### Main vbmeta:

```bash
fastboot flash vbmeta vbmeta_disable.img
```

---

### System AVB disable:

```bash
fastboot flash vbmeta_system vbmeta_system_disable.img
```

---

### Vendor AVB disable:

```bash
fastboot flash vbmeta_vendor vbmeta_vendor_disable.img
```

---

## 🔁 Step 3: Reboot Device

```bash
fastboot reboot
```

---

## ⚠️ Notes

* Always ensure vbmeta files match your firmware version
* Do NOT mix stock vbmeta with disable vbmeta images
* If bootloop happens, restore stock firmware immediately
* Recommended for:

  * GSI testing
  * Custom ROM development
  * Kernel / root experiments

---

## 🧠 A/B Slot Devices (Optional)

```bash
fastboot flash vbmeta_a vbmeta_disable.img
fastboot flash vbmeta_b vbmeta_disable.img
```

---

## 🛑 Disclaimer

This project is intended for **educational and development use only**.
I am not responsible for any damage, boot failure, or data loss caused by improper flashing.

---

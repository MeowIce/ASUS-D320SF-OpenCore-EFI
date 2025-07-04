# ASUS D320SF KABY LAKE DESKTOP EFI
This is an EFI package with everything you need to run macOS perfectly on your ASUS Desktop.
> [!NOTE]  
> This EFI does NOT support dual-booting (ex. Windows & macOS).
## My specifications
![image](https://github.com/user-attachments/assets/bd175955-79c5-4537-ac63-6633083985be)

| **Type** | **Model**                                          |
| ------------- | ----------------------------------------------|
| CPU           | Intel(R) Core(TM) i7-7700K                    |
| RAM           | SAMSUNG M471A1K43CB1 DDR4 8GB 2400MHz (2x8GB) |
| GPU           | Integrated igfx HD630                         |
| Audio         | Realtek ALC887 HDA Codec                      |
| Wireless      | Apple Airport BCM94360CS2                     |
| Storage       | Colorful SL300 128GB; 1TB Toshiba HDD         |
| SMBIOS        | iMac19,1 (iMac Retina 5K 2019)                |
| macOS         | macOS Sequoia 15.5                            |
| Bootloader    | OpenCore 1.0.5 Release                        |

# Working:

- [x] GPU Acceleration
- [x] Power Management
- [x] Wi-FI (2.4GHz/5GHz)
- [x] Bluetooth
- [x] Audio playback
- [x] HDMI port
- [x] All USB ports already mapped
- [x] Temperature readings
- [x] Fan speed readings
- [x] External DVD drives
- [x] Boot chimes
- [x] AirDrop*
- [x] Hand-Off*
- [x] Continuity*
- [x] Universal Control*
- [x] AirPlay*
- [x] iPhone Mirroring*

# What not
- [ ] Sleep/Wake
  + Works most of the time, but will fail sometimes (I mean, not very stable).
  + It could be fixed with an official supported dGPU from AMD.
- [ ] SD Card reader
  + Unsupported reader vendor.

> [!NOTE]  
> Working/not working devices vary from your configuration. Add/rem patches if needed.

> [!IMPORTANT]
> For (*) features, they require you to have a compatible Wireless card.
> 
> If you have a compatible Broadcom Wireless card (aka. Apple Airport), enable the BCM kexts in the Kernel section.

# Installation
1. Copy this EFI to your macOS installation media.
The filesystem structure MUST look like this:
- EFI/
  + APPLE/
    + FIRMWARE/
     + ...
  + BOOT/
     + BOOTx64.efi
  + OC/
     + ACPI/
        + ...
     + Drivers/
        + ...
     + Kexts/
        + ...
     + Resources/
        + ...
     + Tools/
        + ...
     + OpenCore.efi
     + config.plist
   
3. Open config.plist using ProperTree
4. Get GenSMBIOS and generate your own unique serials.
5. Enable/Disable kexts in the Kernel section, if needed.
6. Enjoy !!!

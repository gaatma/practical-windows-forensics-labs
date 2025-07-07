# practical-windows-forensics-labs

# Practical Windows Forensics Labs

This repository documents my hands-on learning journey through the **Practical Windows Forensics** course by TCM Security. It includes step-by-step notes, screenshots, tool usage, and forensic analysis as I work through each phase of a host-based investigation lab.

## 🧰 Tools Used

- FTK Imager
- Autopsy
- Arsenal Image Mounter
- RegRipper
- Volatility3
- Plaso / Log2Timeline

## 🔍 Current Progress
✔️ Environment setup  
✔️ Target system preparation  
✔️ Memory acquisition  
✅ Disk acquisition *(currently here)*  
⬜ Registry analysis  
⬜ Prefetch / Event log analysis  
⬜ Super timeline  
⬜ Final reporting  

## 📁 Folder Guide
- `01_Environment_Setup`: VM, workstation setup, tools installed
- `02_Target_System_Preparation`: Target VM setup + attack simulation
- `03_Evidence_Collection`: Memory and disk acquisition, hash verification
- `resources/`: Tool links and references

## 📌 Course: [Practical Windows Forensics](https://academy.tcm-sec.com/p/practical-windows-forensics)


# 📦 Disk Acquisition - Practical Windows Forensics

## 🔧 Tools Used
- FTK Imager

## 🧪 Objective
To safely acquire a forensic disk image of the target Windows 10 VM using FTK Imager while preserving integrity and ensuring chain of custody.

## ✅ Steps Performed

1. **Opened FTK Imager** on the forensic workstation.
2. Selected the physical disk of the Windows 10 VM as the source.
3. Chose **“Create Disk Image” > “Physical Drive” > Raw (dd)**.
4. Saved the image to an external shared drive.
5. Generated **MD5 and SHA1 hashes** to verify image integrity.

## 📁 Output
- Disk Image: `windows10_target.E01`
- Hashes:
  - MD5: `e1a42a6d111...`
  - SHA1: `5f8846c6c02b...`

## 📸 Screenshot
![FTK Disk Acquisition](ftk_imager_screenshot.png)

## 📝 Notes
- FTK Imager also supports E01 format; I chose `.E01` for compression and metadata.
- Hash values were saved in `disk_image_hashes.txt`.

## 🔗 Related Resources
- [FTK Imager Download](https://accessdata.com/product-download/ftk-imager-version-4-2-0)


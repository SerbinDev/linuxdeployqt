# linuxdeployqt (Fork) – glibc 2.40 Compatible Build

This repository is a **fork** of the official  
➡️ **linuxdeployqt** project: https://github.com/probonopd/linuxdeployqt

The purpose of this fork is **only to ensure compatibility with modern Linux systems**, specifically **glibc up to version 2.40**.  
No functional changes or feature modifications have been introduced.

All credit and ownership belong to **probonopd** and the KDE/AppImage community.

---

## 📌 Purpose of This Fork

Recent Linux distributions ship with glibc versions **2.36 – 2.40**, which may cause build issues with older releases of linuxdeployqt.

This fork:

- Updates the build environment  
- Ensures compatibility with **glibc 2.40**  
- Preserves upstream behavior exactly as-is  

> ⚠️ **Note:**  

> This is *not* an independently developed version.  
> It is simply an updated fork to maintain compatibility with newer systems.

---

## 🧰 What linuxdeployqt Does

linuxdeployqt helps bundle Qt applications into a portable **AppImage**.  
It automatically detects required libraries and packages them together, allowing your Qt program to run on any Linux distribution.

---

## 🔧 Building This Fork (glibc 2.40 Compatible)

Clone this repository and create a build directory:

```bash
mkdir build && cd build
```

Build and install:
```bash
cmake ..
make
sudo make install
```
## Usage

Inside your Qt application's build directory, create a .desktop file:
```bash
[Desktop Entry]
Type=Application
Name=YourAppName
Exec=your_binary
Icon=your_icon
Categories=Utility;
```

## Then run:

```bash
linuxdeployqt YourApp.desktop -appimage
```
linuxdeployqt will scan dependencies and begin creating the AppImage.
Note: The AppImage build process may take a few minutes.

## 📜 License

This fork retains the original licensing of linuxdeployqt
(GPL/LGPL as provided in upstream).
No licensing terms have been modified.

## 🔄 Upstream Sync

This fork may periodically sync with the main repository to maintain compatibility with future glibc releases.
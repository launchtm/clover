# 🍀 Clover Client

<p align="center">
  <img src="images/clover.png" alt="Clover Logo" width="150"/>
</p>

<p align="center">
  <b>A modern, lightweight Minecraft client focused on customization and performance.</b>
</p>

<p align="center">
  <a href="https://github.com/launchtm/clover/releases/download/v7.53-MC26.1/CloverSetup.exe">
    <img src="https://img.shields.io/badge/Download-CloverSetup.exe-green?style=for-the-badge"/>
  </a>

  <a href="https://github.com/launchtm/clover#installation">
    <img src="https://img.shields.io/badge/Docs-Installation-blue?style=for-the-badge"/>
  </a>

  <a href="https://github.com/launchtm/clover/issues">
    <img src="https://img.shields.io/badge/Support-Issues-red?style=for-the-badge"/>
  </a>

  <a href="https://github.com/launchtm/clover">
    <img src="https://img.shields.io/badge/Source-GitHub-black?style=for-the-badge"/>
  </a>
</p>

<p align="center">
  <a href="https://www.minecraft.net/en-us/about-minecraft">
    <img src="https://img.shields.io/badge/Minecraft-26.1-green?style=for-the-badge"/>
  </a>

  <a href="https://fabricmc.net/">
    <img src="https://img.shields.io/badge/Loader-Fabric-orange?style=for-the-badge"/>
  </a>

  <a href="https://www.gnu.org/licenses/gpl-3.0.en.html">
    <img src="https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge"/>
  </a>
</p>

---

## 📑 Table of Contents
- [✨ Features](#-features)
- [📦 Requirements](#-requirements)
- [🛠️ Installation](#️-installation)
- [🎮 Getting Started](#-getting-started)
- [📁 Project Structure](#-project-structure)
- [🔄 Updating](#-updating)
- [❗ Troubleshooting](#-troubleshooting)
- [📜 License](#-license)
- [⚠️ Disclaimer](#️-disclaimer)

---

## ✨ Features

| Category | Description |
|---------|-------------|
| 🧩 Modular Design | Toggle features based on your playstyle |
| 🏃 Movement | Enhanced navigation and mobility |
| ⚔️ Combat | Smoother and more responsive interactions |
| 🌍 Utility | Better awareness and convenience tools |
| 🚀 Performance | Optimized for stable gameplay |
| 🎨 GUI | Clean and customizable interface |

---

## 📦 Requirements

- Minecraft: Java Edition 26.1
- Java 17+
- Windows (the installer is Windows-only)

> Fabric Loader and Fabric API are installed automatically by the installer. You do not need to download them separately.

---

## 🛠️ Installation

### ⚡ Recommended — CloverSetup.exe

**[Download CloverSetup.exe](https://github.com/launchtm/clover/releases/download/v7.53-MC26.1/CloverSetup.exe)**

CloverSetup is a small installer wizard that automates the entire setup. It handles Fabric, Fabric API, and Clover Client in one go.

#### What the installer does, step by step:

**1. Choose folder**
The installer defaults to:
```
C:\Users\<you>\AppData\Roaming\.minecraft\mods
```
You can point it at either your `mods` folder or the parent `.minecraft` folder — it figures out the rest.

**2. Review**
Before installing, it shows you exactly what it's about to do:
- Install Fabric Loader
- Copy Fabric API into your mods folder
- Copy Clover Client into your mods folder
- Rename the Minecraft Launcher profile to **Clover Launcher**

**3. Download & verify**
The installer downloads and SHA-256 verifies three files before doing anything:
| File | Version |
|------|---------|
| `fabric-installer-1.1.1.exe` | Fabric Installer |
| `fabric-api-0.144.3+26.1.jar` | Fabric API |
| `clovermenu-7.53-MC26.1.jar` | Clover Client |

**4. Fabric setup**
Runs the Fabric installer silently:
```
client -dir <minecraft-folder> -mcversion 26.1 -loader 0.18.5
```
It also ensures `launcher_profiles.json` exists and strips any UTF-8 BOM that would cause Fabric's parser to fail.

**5. Rename launcher profile**
Edits `launcher_profiles.json` to rename the Fabric profile to **Clover Launcher** in your Minecraft Launcher. The internal Fabric version ID is left untouched.

**6. Install mods**
Copies `fabric-api-0.144.3+26.1.jar` and `clovermenu-7.53-MC26.1.jar` into your mods folder.  
Any older Clover or Fabric API jars are backed up to:
```
.minecraft\mods\_clover-installer-backup\<timestamp>
```

**7. Finish**
Click **Finish** and Minecraft Launcher opens automatically. Select **Clover Launcher** and hit Play.

---

### 🔧 Manual Installation (advanced)

If you prefer to install without the setup wizard:

**Requirements:**
- Fabric Loader → https://fabricmc.net/use/installer/
- Fabric API → https://modrinth.com/mod/fabric-api

1. Install Fabric Loader for Minecraft 26.1
2. Put `fabric-api-0.144.3+26.1.jar` into your mods folder
3. Put `clovermenu-7.53-MC26.1.jar` into your mods folder
4. Launch Minecraft with the Fabric profile

**Mods folder locations:**

| OS | Path |
|----|------|
| Windows | `%appdata%\.minecraft\mods` |
| Mac | `~/Library/Application Support/minecraft/mods` |
| Linux | `~/.minecraft/mods` |

---

## 🎮 Getting Started

### Open GUI
- Press **Right Shift**

### Configure
- Enable modules
- Adjust settings
- Everything saves automatically

Config location:
```
.minecraft/config/clover/
```

---

## 📁 Project Structure

```
Clover/
├── src/
├── gradle/
├── build.gradle
├── settings.gradle
├── LICENSE
└── README.md
```

---

## 🔄 Updating

**With the installer:** Re-run `CloverSetup.exe`. It backs up your existing jars and installs the latest version.

**Manually:**
1. Download the latest release
2. Replace the old `clovermenu-*.jar` in your mods folder
3. Restart the game

---

## ❗ Troubleshooting

<details>
<summary><b>Installer not working?</b></summary>

- Make sure you're on Windows
- Run as Administrator if you get a permissions error
- Check that Minecraft has been launched at least once so `launcher_profiles.json` exists

</details>

<details>
<summary><b>Game crashing?</b></summary>

- Check Java version (17+)
- Make sure Fabric Loader version matches Minecraft 26.1
- Remove conflicting mods
- Check logs in `.minecraft/crash-reports/`

</details>

<details>
<summary><b>Clover not showing up in-game?</b></summary>

- Confirm you launched the **Clover Launcher** profile, not vanilla
- Check that both `fabric-api-*.jar` and `clovermenu-*.jar` are in your mods folder
- Fabric API is required — Clover won't load without it

</details>

<details>
<summary><b>Low FPS?</b></summary>

- Allocate more RAM in your launcher settings
- Update GPU drivers
- Clover is compatible with Sodium for additional performance gains

</details>

---

## 📜 License

This project is licensed under **GPLv3**.

---

## ⚠️ Disclaimer

<p align="center">
  <b>Clover is currently not open source. Check back later for updates.</b>
</p>

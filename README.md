<p align="center">
  <img src="https://raw.githubusercontent.com/ProjectInfinity-X/.github/main/profile/Infinity.png" alt="Project Infinity X Logo" />
</p>

## Overview

**Project Infinity X** is a powerful, customizable Android OS built on open-source principles, inspired by multiple community-driven projects. With a clear focus on performance, flexibility, and user experience, Infinity X provides a streamlined build process and comprehensive support for maintainers and device contributors.

## ✅ Prerequisites

Before you proceed, ensure your development environment includes:

- [Repo](https://source.android.com/source/using-repo.html)
- [Git](https://source.android.com/source/version-control.html)
- [Git LFS](https://git-lfs.github.com/)


## Getting Started

### 1. Repository Initialization

Initialize your local copy of the Project Infinity X source code:

Standard initialization:

```bash
repo init --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b 16 -g default,-mips,-darwin,-notdefault
```

For minimal history (saves space):

```bash
repo init --depth=1 --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b 16 -g default,-mips,-darwin,-notdefault
```


### 2. Sync Source

Fetch all repositories and set up your local workspace:

```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```


## ⚙️ Build Customization

### Key Build Flags

Configure your build type and maintainer information in your environment or build files:

```bash
INFINITY_BUILD_TYPE := OFFICIAL / UNOFFICIAL   # Default: UNOFFICIAL
INFINITY_MAINTAINER := "YourName"             # Default: Unknown
WITH_GAPPS := true/false                      # Default: true
```

### Device/Phone Properties

Add these as `PRODUCT_SYSTEM_PROPERTIES` or within your `system.prop`. Use tools like `libinit` for unified devices.

```bash
ro.product.marketname=OnePlus 12R 5G
ro.infinity.soc=Snapdragon 8 Gen 2
ro.infinity.battery=5500 mAh
ro.infinity.display=1264 x 2780, 120 Hz
ro.infinity.camera=50MP + 8MP + 2MP
```


## 🖥️ Build Environment Setup

1. Change to the source root directory:

```bash
cd path/to/source
```

2. Set up build environment scripts:

```bash
. build/envsetup.sh
```

3. Select your device configuration:

```bash
lunch infinity_$device-$buildtype
```

    - Replace `$device` with your device codename.
    - Replace `$buildtype` with your preferred build type (`user`, `userdebug`, or `eng`).

## Compiling Project Infinity X

Begin the build process:

```bash
m bacon
```


## 🙌 Credits

Project Infinity X is made possible by invaluable contributions and inspiration from:

- [LineageOS](https://github.com/LineageOS)
- [LunarisOS](https://github.com/Lunaris-CLO)
- [PixelExperience](https://github.com/PixelExperience)
- [crDroid](https://github.com/crdroidandroid)
- RisingOS
- [SuperiorOS](https://github.com/SuperiorOS)
- [BootleggersROM](https://github.com/bootleggersrom)
- [TenX-OS](https://github.com/TenX-OS)
- [ProjectPixelage](https://github.com/ProjectPixelage)
- [xdroidOSS](https://github.com/xdroid-oss)
- [OctaviOS](https://github.com/Octavi-OS)
- ...and other community projects ❤️


## 📢 Contact \& Support

- 💬 **Join Discussions:** [Telegram Group](https://t.me/InfinityXGroup)
- 📢 **News \& Updates:** [Telegram Channel](https://t.me/ProjectInfinityX)

## 🤝 Contributing

*Contributions are always welcome! If you notice any missing credits or want to suggest improvements, feel free to open an issue or reach out on Telegram.*



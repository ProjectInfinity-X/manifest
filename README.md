![Project Infinity X](https://raw.githubusercontent.com/ProjectInfinity-X/.github/main/profile/Infinity.png)

## Requirements:
Before you begin, ensure your system meets the following requirements:
- [Repo](https://source.android.com/source/using-repo.html)
- [Git](https://source.android.com/source/version-control.html)
- Git Large File Storage (Git LFS)

## Initialization and Syncing:
1. Initialize your local repository:
    ```bash
    repo init --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b 16 -g default,-mips,-darwin,-notdefault
    ```
   Or If you wish to save some system space and don't care about repo history depths:
    ```bash
    repo init --depth=1 --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b 16 -g default,-mips,-darwin,-notdefault
    ```
2. Sync up with the remote repository:
    ```bash
    repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
    ```

# Compilation of Project Infinity X:

Build Flags
---------------
```bash
# Maintainer Name
INFINITY_MAINTAINER := "YourInput" (Default: Unknown)

# Whether the device supports Fingerprint On Display
TARGET_HAS_UDFPS := true/false (Default: false)

# Whether Including Google Apps
WITH_GAPPS := true/false (Default: true)
```
About Phone Definitions
---------------
```bash
# Add these as system properties (in system.prop file), You may use utilities as libinit if configuring for unified devices
ro.product.marketname
ro.infinity.soc
ro.infinity.camera

# Example Defintions
ro.product.marketname=OnePlus 12R
ro.infinity.soc=Snapdragon 8 Gen 2
ro.infinity.camera=50MP + 8MP + 2MP
```
## Setup Environment:
1. Navigate to the root directory of Project Infinity X:
    ```bash
    cd path/to/source
    ```
2. Run the environment setup script:
    ```bash
    . build/envsetup.sh
    ```
# Build Configuration:
1. Choose your device configuration:
    ```bash
    lunch infinity_$device-$buildtype
    ```
    Replace `$device` with your device codename and `$buildtype` with your prefered build type (user, userdebug or eng).

## Compilation:
1. Start the compilation process:
    ```bash
    m bacon -j$(nproc --all)
    ```

# Credits:
- [LineageOS](https://github.com/LineageOS)
- [crDroid](https://github.com/crdroidandroid)
- [PixelExperience](https://github.com/PixelExperience)
- RisingOS
- [AxionAOSP](https://github.com/axionaosp)
- [LunarisAOSP](https://github.com/Lunaris-AOSP)
- [SuperiorOS](https://github.com/SuperiorOS)
- [BootleggersROM](https://github.com/bootleggersrom)
- [TenX-OS](https://github.com/TenX-OS)
- [xdroidOSS](https://github.com/xdroid-oss)
- [OctaviOS](https://github.com/Octavi-OS)
- And More If May Missed to Mention!

# Reach US:
- **Telegram Discussion**: [https://t.me/InfinityXGroup](https://t.me/InfinityXGroup)
- **Telegram News/Updates**: [https://t.me/ProjectInfinityX](https://t.me/ProjectInfinityX)

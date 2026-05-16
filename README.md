![Project Infinity X](https://raw.githubusercontent.com/ProjectInfinity-X/.github/cf5db878157cff92251378562517ac4b1a358cbf/profile/Infinity.png)

## Requirements:
Before you begin, ensure your system meets the following requirements:
- [Repo](https://source.android.com/source/using-repo.html)
- [Git](https://source.android.com/source/version-control.html)
- Git Large File Storage (Git LFS)

## Initialization and Syncing:
1. Initialize your local repository:
    ```bash
    repo init --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b 15 -g default,-mips,-darwin,-notdefault
    ```
   Or If you wish to save some system space and don't care about repo history depths:
    ```bash
    repo init --depth=1 --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b 15 -g default,-mips,-darwin,-notdefault
    ```
2. Sync up with the remote repository:
    ```bash
    repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
    ```

# Compilation of Project Infinity X:

Build Flags
---------------
```bash
# Whether you are compiling being an OFFICIAL Maintainer:
INFINITY_BUILD_TYPE := OFFICIAL/UNOFFICIAL (Default: UNOFFICIAL)

# Maintainer Name
INFINITY_MAINTAINER := "YourInput" (Default: Unknown)

# Whether the package includes System BLURS
TARGET_SUPPORTS_BLUR := true/false (Default: false)

# Whether the compiled package ships Google Apps:
WITH_GAPPS := true/false (Default: false)

# Whether the compiled package ships more (mostly unimportant) Google Apps:
TARGET_SHIPS_FULL_GAPPS := true/false (Default: false) (These apps could easily be installed via PlayStore as per user need, so could be skipped shipping by default)

# Whether the compiled shipped gapps package uses Google Dialer:
TARGET_SHIPS_GOOGLE_DIALER := true/false (Default: false) (By default our enhanced variant of AOSP dialer is shipped which supports call recording without announcement and a beautiful UI/caller screen)

# Whether the compiled package ships Motorola Calculator:
USE_MOTO_CALCULATOR := true/false (Default: true)
```
About Phone Definitions
---------------
```bash
# Add these as PRODUCT_SYSTEM_PROPERTIES (or in system.prop file), You may use utilities as libinit if configuring for unified devices
ro.product.marketname
ro.infinity.soc
ro.infinity.battery
ro.infinity.display
ro.infinity.camera

# Example Defintions
ro.product.marketname=OnePlus 12R 5G
ro.infinity.soc=Snapdragon 8 Gen 2
ro.infinity.battery=5500 mAh
ro.infinity.display=1264 x 2780, 120 Hz
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
    mka bacon
    ```

# Credits:
- [LineageOS](https://github.com/LineageOS)
- [ProtonAOSP](https://github.com/ProtonAOSP)
- [PixelExperience](https://github.com/PixelExperience)
- [crDroid](https://github.com/crdroidandroid)
- RisingOS
- [SuperiorOS](https://github.com/SuperiorOS)
- [ProjectPixelage](https://github.com/ProjectPixelage)
- [xdroidOSS](https://github.com/xdroid-oss)
- [OctaviOS](https://github.com/Octavi-OS)
- And More If May Missed to Mention!

# Reach US:
- **Telegram Discussion**: [https://t.me/InfinityXGroup](https://t.me/InfinityXGroup)
- **Telegram News/Updates**: [https://t.me/ProjectInfinityX](https://t.me/ProjectInfinityX)

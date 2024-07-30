![Project Infinity X](https://raw.githubusercontent.com/ProjectInfinity-X/.github/main/profile/Infinity.png)

## Requirements:
Before you begin, ensure your system meets the following requirements:
- [Repo](https://source.android.com/source/using-repo.html)
- [Git](https://source.android.com/source/version-control.html)
- Git Large File Storage (Git LFS)

## Initialization and Syncing:
1. Initialize your local repository:
    ```bash
    repo init --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b QPR3 -g default,-mips,-darwin,-notdefault
    ```
   Or If you wish to save some system space and don't care about repo history depths:
    ```bash
    repo init --depth=1 --no-repo-verify --git-lfs -u https://github.com/ProjectInfinity-X/manifest -b QPR3 -g default,-mips,-darwin,-notdefault
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
INFINITY_BUILD_TYPE := OFFICIAL (Default: UNOFFICIAL)

# Maintainer Name
INFINITY_MAINTAINER := "YourInput" (Default: Unknown)

# Whether the package supports BLURS
TARGET_SUPPORTS_BLUR := true/false (Default: false)

# Whether the device supports UDFPS (FOD)
TARGET_HAS_UDFPS := true/false (Default: false)

# Whether the compiled package ships Google Apps:
WITH_GAPPS := true/false (Default: false)

# Whether the compiled shipped gapps package uses Google Dialer, Messaging, Contacts:
TARGET_BUILD_GOOGLE_TELEPHONY := true/false (Default: false)

# Whether your device supports screen off touchgestures:
TARGET_SUPPORTS_TOUCHGESTURES := true/false (Default: false)

# Whether the compiled package ships ViMusic
TARGET_BUILD_VIMUSIC := true/false (Default: false)

# Whether the compiled package ships Moto Calculator irrespective VANILLA or GAPPS:
USE_MOTO_CALCULATOR := true/false (Default: false)
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
- [CrDroid](https://github.com/crdroidandroid)
- [RisingOS](https://github.com/RisingTechOSS)
- [Yaap](https://github.com/yaap)
- [SuperiorOS](https://github.com/SuperiorOS)
- [Project Blaze](https://github.com/ProjectBlaze)
- [Xdroid](https://github.com/xdroid-oss)
- [OctaviOS](https://github.com/Octavi-OS)
- [Evolution-X](https://github.com/Evolution-X)
- And Many More If Missed to Mention!

# Reach US:
- **Telegram Discussion**: [https://t.me/InfinityXGroup](https://t.me/InfinityXGroup)
- **Telegram News/Updates**: [https://t.me/ProjectInfinityX](https://t.me/ProjectInfinityX)


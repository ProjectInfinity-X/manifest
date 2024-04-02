# Ｉｎｆｉｎｉｔｙ Ｘ

## Requirements:
Before you begin, ensure your system meets the following requirements:
- [Repo](https://source.android.com/source/using-repo.html)
- [Git](https://source.android.com/source/version-control.html)
- Git Large File Storage (Git LFS)

## Initialization and Syncing:
1. Initialize your local repository:
    ```bash
    repo init --depth=1 -u https://github.com/ProjectInfinity-X/manifest -b QPR2 --git-lfs
    ```
2. Sync up with the remote repository:
    ```bash
    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune
    ```

# Compilation of Project Infinity X:

## Setup Environment:
1. Navigate to the root directory of Project Infinity X:
    ```bash
    cd path/to/project/infinity-x
    ```
2. Run the environment setup script:
    ```bash
    . build/envsetup.sh
    ```

## Build Configuration:
1. Choose your device configuration:
    ```bash
    lunch infinity_$device-userdebug
    ```
    Replace `$device` with your device codename.

## Compilation:
1. Start the compilation process:
    ```bash
    make bacon
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

# Additional Notes:
- **Troubleshooting**: If you encounter any issues during setup or compilation, refer to the troubleshooting section in the project's documentation or seek help from the community forums.
- **Contributions**: We welcome contributions to Project Infinity X. Refer to our contribution guidelines for more information on how to get involved.


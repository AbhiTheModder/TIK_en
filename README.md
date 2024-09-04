## TIK

#### **Introduction**

> [!CAUTION]
> This project is not published on gitcode. If you find this project on gitcode, please contact us and keep the screenshot as evidence.

> [!CAUTION]
> Free software, unauthorized commercial use prohibited

[Russian](../../tree/ru)

1. **TIK Toolkit** - An open-source ROM toolkit that supports the processing of Android ROM images of all versions. Currently updated to Ver.5;

2. Supports the disassembly/packaging of most common images, with good support for erofs/V-AB partitions, etc.

3. Added settings function - adjust interaction habits, packaging behavior

4. Testing support for Android 15...

5. New MKC_Boot_Kitchen to disassemble/unpack [boot|exaid|recovery/etc].img

6. Supports the disassembly of super.img (V-AB) of all versions and the packaging of various types (automatically identified to a certain extent, efficient and stable)

#### **Support**

**[Recognition, Disassembly, and Packaging Support]**

1. [*.zip, *.br, *.dat, ext4/2 *.img, bootimg, etc.] Traditional image recognition - disassembly - packaging
2. [Super.img <A-only/AB/V-AB>, bootimg<header3>, erofs *.img, F2FS (this tool's LINUX 64BIT version supports) etc.] Newer image recognition - disassembly - packaging
3. [dtbo, dtb, TWRP, ops, ofp, ozip, payload.bin, *.win000-004, *.dat.1~20, etc.] Special file unpacking/packaging
4. Adapts well to the latest **Android 14**, **Erofs**, **Dynamic Partition**, **V-AB Partition**

**[Software Architecture - Supports]**

1. Termux Arm64[aarch64] native support or [<Linux Deploy>/Termux] Chroot Ubuntu 20.04 and above version Arm64[aarch64] [Chroot is recommended for higher efficiency]

2. Virtual machine or physical machine Ubuntu 20.04 and above version x86_64[x64]

3. Windows 7 and Newer[x64/x86]

Note: WSL may have permission error issues, please judge and test by yourself!

#### **Referenced Projects**

1. [ApkParse](https://github.com/zxvzxv/ApkParse/)
2. [sdat2img](https://github.com/xpirt/sdat2img)
3. [img2sdat](https://github.com/xpirt/img2sdat)
4. [make_ext4fs](https://github.com/jamflux/make_ext4fs)
5. [oppo_decrypt](https://github.com/bkerler/oppo_decrypt)
6. [lpunpack](https://github.com/unix3dgforce/lpunpack)
7. [brotli](https://github.com/google/brotli)
8. [rich](https://github.com/Textualize/rich/)
9. [context_patch](https://github.com/ColdWindScholar/context_patch)
10. [erofs-utils](https://github.com/sekaiacg/erofs-utils/)
11. [Magisk_Patch_Python](https://github.com/ColdWindScholar/Magisk_Patch_Python)
12. And More...

#### **Partners**

1. Sakura
2. Affggh
3. Yeliqin666
4. [qlenlen - For F2FS REPACK](https://github.com/qlenlen)

#### **Supported Systems**

1. Android-(Termux) | ARM64
2. Windows(7 AND NEWER) | AMD64 X86 ARM64
3. Linux | ARM64 X86_64
4. Macos | ARM64(by sewzj) X86_64

#### ** Installation tutorial **

    git clone https://github.com/ColdWindScholar/TIK
    cd TIK
    chmod a+x ./*
    python build.py
    sudo ./run

#### **Instructions for Use**

1. **Warning: Do not use system root features in Termux**. Root privileges are required on the PC side (sudo, though it may not be necessary), and it is best not to run this tool in a root user login state to avoid permission issues when flashing the package into the phone!

2. **Regarding File Selection under Proot**

   - Place zip files or mpk plugins in the **Internal Storage Tool Resource Directory**, the tool will automatically search for them (can be modified in the settings).

3. Tool directory under Termux proot Ubuntu on the phone: **/data/data/com.termux/files/home/ubuntu/root/TIK**

4. **Do not delete the [Project Directory/config folder]**, the necessary file information for packaging is stored here, and the tool will automatically adjust the size to fit dynamic partitions! (Can be adjusted manually)

5. Due to factors such as phone performance, proot efficiency, and operation mode (e.g., automatic comparison of fs_config before packaging an img, not immediately packaging), there may be lags during operation. Please be patient and wait a moment.

6. When deleting files, execute **rm -rf file, folder** in **Termux or proot Ubuntu** **Do not use system root features**.

7. **To ensure the tool runs normally, ensure strong conditions: the working path must not contain Chinese characters or spaces, the project folder must not have spaces or other special symbols, and file names should not be too long!**

8. **Dynamic partitions do not allow single flashing of any partition (unless under fastbootd), please refer to the Android documentation for details.**

9. If you use **system ROOT** to perform operations (such as **adding files, modifying files**) in the project directory on the phone, remember to grant the operated files or folders **777** full permissions!

10. **Regarding the One-Click Generation of "Card-Line Integrated Package"**: Some manufacturers have restrictions on certain partitions, and it is currently recommended to flash under fastbootd to maintain the integrity of the super information.

#### **Contribution Methods**

Please initiate a PR, and we will review and handle it as soon as possible. Thank you to all developers/enthusiasts who have supported this project!

#### **Communication and Feedback**

QQ Group: [932388310](#communication-and-feedback)
Developer QQ Group: 777617022

#### **Disclaimer**

1. This tool runs in the Termux proot environment and does not require root permissions **Please use system root features with caution in Termux**!!!

2. This tool does not contain any code that is **destructive to the system, data acquisition**, or other illegal activities!!!

3. **If data loss or damage occurs due to user operations on the project directory with root privileges, no responsibility will be assumed!!!**

#### [TIK5.0](https://github.com/ColdWindScholar/TIK)

#### ColdWindScholar(3590361911@qq.com).All rights reserved.

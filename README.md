___________________________________________________________________________________________________________

                                    CROSS COMPILER TOOLCHAINS - README
___________________________________________________________________________________________________________


This branch contains some of the latest cross compiler toolchains I've built for Android kernel development,
it contains the following:
- "Linaro GCC 4.8.3-2014.04 Toolchains" include Linaro GCC 4.8-2014.04 (4.8.3) and Linaro GDB 7.6.1-2013.10
- "Linaro GCC 4.7.4-2014.04 Toolchains" include Linaro GCC 4.7-2014.04 (4.7.4) and Linaro GDB 7.6.1-2013.10

Note: GCC 4.8 toolchains could cause incompatibility problems with some kernels


You can find other zipped toolchain builds on my Mediafire folder, please take a look at the original thread on
XDA Developers forum at this link:
       http://forum.xda-developers.com/showthread.php?t=2098133


- The toolchains with "arm-cortex_a15-linux-gnueabi" prefix are optimized for Cortex-A15 cpu with Neon-VFPv4 technology support
- The toolchains with "arm-cortex_a9-linux-gnueabi" prefix are optimized for Cortex-A9 cpu with Neon-VFPv3 technology support
- The toolchains with "arm-cortex_a8-linux-gnueabi" prefix are optimized for Cortex-A8 cpu with Neon-VFPv3 technology support
  (like Qualcomm Snapdragon Scorpion cpu mounted on Samsung S Plus I9001)
- The toolchains with "arm-linux-gnueabi" prefix are built for generic Cortex-A cpu and configured with similar settings
to those of the latest Linaro toolchains

I hope you find them useful...
Let me know.
Thanks!

Christopher


These are the details on each toolchain currently available on this repo


___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a15-linux-gnueabihf-linaro_4.8.3-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Cortex-A15 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH=""
    CT_ARCH_CPU="cortex-a15"
    CT_ARCH_TUNE="cortex-a15"
    CT_ARCH_FPU="neon-vfpv4"
    CT_ARCH_FLOAT_HW=y
    CT_ARCH_FLOAT="hard"
    CT_ARCH_SUPPORT_SOFTFP=y
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.4.87
- Linaro GCC 4.8-2014.04 (4.8.3)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04 prebuilt
- Linaro GDB 7.6.1-2013.10
- GMP 5.1.1
- MPFR 3.1.2
- ISL 0.11.1
- CLOOG 0.18.0
- MPC 1.0.2
- Hard float with soft float support
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a9-linux-gnueabihf-linaro_4.8.3-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Cortex-A9 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a9"
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_HW=y
    CT_ARCH_FLOAT="hard"
    CT_ARCH_SUPPORT_SOFTFP=y
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.4.87
- Linaro GCC 4.8-2014.04 (4.8.3)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04 prebuilt
- Linaro GDB 7.6.1-2013.10
- GMP 5.1.1
- MPFR 3.1.2
- ISL 0.11.1
- CLOOG 0.18.0
- MPC 1.0.2
- Hard float with soft float support
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a8-linux-gnueabi-linaro_4.8.3-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Cortex-A8 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a8"
    CT_ARCH_TUNE="cortex-a8"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.0.101
- Linaro GCC 4.8-2014.04 (4.8.3)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04
- Linaro GDB 7.6.1-2013.10
- GMP 5.1.1
- MPFR 3.1.2
- ISL 0.11.1
- CLOOG 0.18.0
- MPC 1.0.2
- Softfp
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                      TOOLCHAIN arm-linux-gnueabi-linaro_4.8.3-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Generic ARM settings (inspired by latest Linaro builds) for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU=""
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="vfpv3-d16"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="thumb"
    CT_ARCH_ARM_MODE_THUMB=y

- Linux Kernel 3.0.101
- Linaro GCC 4.8-2014.04 (4.8.3)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04
- Linaro GDB 7.6.1-2013.10
- GMP 5.1.1
- MPFR 3.1.2
- ISL 0.11.1
- CLOOG 0.18.0
- MPC 1.0.2
- Softfp
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a15-linux-gnueabihf-linaro_4.7.4-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Cortex-A15 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH=""
    CT_ARCH_CPU="cortex-a15"
    CT_ARCH_TUNE="cortex-a15"
    CT_ARCH_FPU="neon-vfpv4"
    CT_ARCH_FLOAT_HW=y
    CT_ARCH_FLOAT="hard"
    CT_ARCH_SUPPORT_SOFTFP=y
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.4.87
- Linaro GCC 4.7-2014.04 (4.7.4)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04 prebuilt
- Linaro GDB 7.6.1-2013.10
- GMP 5.0.2
- MPFR 3.1.2
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 1.0.2
- Hard float with soft float support
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a9-linux-gnueabihf-linaro_4.7.4-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Cortex-A9 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a9"
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_HW=y
    CT_ARCH_FLOAT="hard"
    CT_ARCH_SUPPORT_SOFTFP=y
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.4.87
- Linaro GCC 4.7-2014.04 (4.7.4)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04 prebuilt
- Linaro GDB 7.6.1-2013.10
- GMP 5.0.2
- MPFR 3.1.2
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 1.0.2
- Hard float with soft float support
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a8-linux-gnueabi-linaro_4.7.4-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Cortex-A8 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a8"
    CT_ARCH_TUNE="cortex-a8"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.0.101
- Linaro GCC 4.7-2014.04 (4.7.4)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04 prebuilt
- Linaro GDB 7.6.1-2013.10
- GMP 5.0.2
- MPFR 3.1.2
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 1.0.2
- Softfp
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                      TOOLCHAIN arm-linux-gnueabi-linaro_4.7.4-2014.04

- Built using latest Linaro Crosstool-NG toolchain builder (linaro-1.13.1)
- Generic ARM settings (inspired by latest Linaro builds) for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU=""
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="vfpv3-d16"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="thumb"
    CT_ARCH_ARM_MODE_THUMB=y

- Linux Kernel 3.0.101
- Linaro GCC 4.7-2014.04 (4.7.4)
- Linaro Binutils 2.24-2014.03
- Linaro EGLibc 2.19-2014.04 prebuilt
- Linaro GDB 7.6.1-2013.10
- GMP 5.0.2
- MPFR 3.1.2
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 1.0.2
- Softfp
- Multilib support
- Alias "arm-gnueabi-"

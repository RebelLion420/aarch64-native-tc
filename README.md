# Aarch64-native toolchains


Various toolchains for use with compiling Android kernels. Compiled on a
OnePlus 7 Pro using USBHost's build-tools-gcc repo. Specs at bottom.


To download toolchains, you need git-lfs installed (apt, pacman, rpm, etc.)
and then clone this repo, e.g.:


`$ git clone https://github.com/RebelLion420/aarch64-native-tc`


If for some reason the files fail to download, running `git pull`, or if that
fails `git lfs pull`, should work. If you wish to only download a single
toolchain you can clone the repo without LFS and fetch the toolchain with the
"include" flag for `git lfs fetch`, e.g.:


`$ GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/RebelLion420/aarch64-native-tc`

`$ cd aarch64-native-tc/`

`$ git lfs fetch -I aarch64-gnu/aarch64-gnu-4.9.4-arm-linux-gnueabi.tar.xz`


Then simply unpack the toolchain where desired:


`$ tar xpf aarch64-gnu/aarch64-gnu-4.9.4-arm-linux-gnueabi.tar.xz -C ~/toolchain`


Or if you like progress bars and have `pv` installed:


`$ pv aarch64-gnu/aarch64-gnu-4.9.4-arm-linux-gnueabi.tar.xz | tar xp -C ~/toolchain`



## Host Machine

Type | Value
--- | ---
**Device:** | Oneplus 7 Pro (GM1917)
**System:** | OOS 10.3.1
**Host:** | Arch Linux ARM rolling (Termux v0.92)
**Host Arch:** | Aarch64 / ARMv8-A
**Kernel Version:** | 4.14.168-Kirisakura-Guacamole_Q_1.7.0
**CPU Model:** | Qualcomm SM8150
**GCC Version:** | GCC 9.2.0

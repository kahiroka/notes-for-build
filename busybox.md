# Prerequisite

    Ubuntu 20.04.4 LTS amd64

# Common

    $ sudo apt install flex bison libncurses-dev
    $ git clone https://git.busybox.net/busybox
    $ cd busybox/

# x86-64

    $ sudo apt install libssl-dev
    $ make defconfig
    $ make menuconfig
    $ make
    $ make install

# i386

    $ sudo apt install gcc-multilib g++-multilib
    $ sudo apt install libc6-dev:i386 libssl-dev:i386 
    $ make defconfig
    $ make menuconfig
    $ CPPFLAGS=-m32 LDFLAGS=-m32 make
    $ CPPFLAGS=-m32 LDFLAGS=-m32 make install

# arm

    $ sudo apt install gcc-arm-linux-gnueabi
    $ make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- defconfig
    $ make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- menuconfig
    $ make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- 
    $ make ARCH=arm CROSS_COMPILE=arm-linux-gnueabi- install

# aarch64

    $ sudo apt install gcc-aarch64-linux-gnu
    $ make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- defconfig
    $ make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- menuconfig
    $ make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- 
    $ make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- install
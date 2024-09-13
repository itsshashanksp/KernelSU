
# KernelSU
* A fork of https://github.com/tiann/KernelSU.git by @tiann

## Build Kernel with KernelSU

## Installing as a part of the GKI based kernels

1. Let's take [linux] as the path to your kernel source dir.
```
        cd [linux]
        git clone https://github.com/itsshashanksp/KernelSU.git
	cp -ar KernelSU [linux]/drivers/kernelsu
```

2. edit [linux]/drivers/Kconfig
```
	+source "drivers/kernelsu/Kconfig"
```

3. edit [linux]/drivers/Makefile
```
	+obj-$(CONFIG_KSU)	+= kernelsu/
```

4. set KSU defconfig
```
#
# KernelSU
#
CONFIG_KSU=y
# CONFIG_KSU_DEBUG is not set
```

build your kernel

* For more information or any doubt visit official website of KernelSU https://kernelsu.org/

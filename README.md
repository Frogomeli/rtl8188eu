# rtl8188eu

Linux driver for TpLink-WN725N/Mercury-MW150US(Rev 2.0) nano wireless adapter.

The source code is from https://github.com/Red54/linux-shumeipai2/tree/sunxi-3.0/drivers/net/wireless/rtl8188eu and updated from the patch https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1030858/+attachment/3465019/+files/use_kthread_run.patch for kernel 2.7.

From : https://github.com/gleb-chipiga/rtl8188eu

Patched for CubieBoard kernel 3.4.24

## compile and install

change in file Makefile:

line 529 the prefix of compil tools

CROSS_COMPILE := arm-linux-gnueabihf-

line 531 the directory of kernel

KSRC:= /root/dev/linux-allwinner-aufs34/

1. make
2. copy 8188eu.ko to ``/lib/modules/`uname -r`/kernel/drivers/net/wireless``
3. depmod -a
4. modprobe 8188eu
5. ifconfig and you can see the wlan interface :-)

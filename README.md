## RTL8812AU/RTL8821AU Driver for Armbian

Source: https://github.com/gnab/rtl8812au

Realtek 802.11ac v4.2.2 (RTL8812AU/RTL8821AU) driver for Armbian builds (tested with **linux kernel 3.4.113** on NanoPi NEO & Orange Pi Zero)

# Installation

Install linux headers and toolchain utilities, if you haven't already. (Note: **linux-headers-sun8i** is specific to the tested kernel -- yours could be different)

```shell

apt-get install linux-headers-sun8i binutils-arm-none-eabi gcc-arm-none-eabi

```

Clone the repository, then:

```shell

cd arm-rtl8812au/

```


Run the following (with root permissions):

```shell

make
make install

```

Load the driver (Note: use 8812au or 8821au, depending on your adapter's chipset):

```shell

modprobe 8812au

```

To make sure the module loads on boot, append the inserted module name (i.e. 8812au) to **/etc/modules**

nitial src
can boot though u-boot and/or grub
console via serial line
has support for pci, usb, ethernet, ...
do not support display (radeonfb)
working on this

making uboot :
1500a mkimage -A arm64 -O linux -T kernel -a 0x80080000 -e 0x80080000 -d Image uImage

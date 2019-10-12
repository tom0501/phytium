Initial src
can boot though u-boot and/or grub:
***
linux	/uImage console=tty0 console=ttyAMA0 console=ttyS0,115200 root=/dev/ram rdinit=/sbin/init video=vesafb earlyprintk=uart8250-32bit,0x28000000 KEYBOARDTYPE=pc KEYTABLE=us
initrd	/initramfs_data.cpio.gz
devicetree	/dtb/ft1500a4-pc-gw.dtb
***
console via serial line com1
has support for pci, usb, ethernet, soundcard, etc.
DOES NOT support display (radeonfb)
working on this

making uboot :
1500a mkimage -A arm64 -O linux -T kernel -a 0x80080000 -e 0x80080000 -d Image uImage

# uboot for MT7621 NAND
It boot from SPI flash and then write bootloader to NAND. Then device can boot from NAND
## Steps
```bash
tftpboot 0x80100000 uboot.img
md 0x80100000
nand init
nand read 0 200
nand erase 0 40000
nand write.fan
```

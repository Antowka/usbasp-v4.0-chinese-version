**This is the README file for USBasp (Chinese version: MX-USB-ISP-V4.00 and other v4.00).**

Compiled versions for mega8, mega48, mega88 there are folder **bin/firmware**.

USE PRECOMPILED VERSION

You have to change the fuse bits for external crystal (see "make fuses").

TARGET=atmega8    HFUSE=0xc9  LFUSE=0xef

TARGET=atmega48   HFUSE=0xdd  LFUSE=0xff

TARGET=atmega88   HFUSE=0xdd  LFUSE=0xff

*I used Arduino ISP and avrdude for upload firmware and set fuses, my command for atmega88:*

```
avrdude -p m88 -c avrisp -P /dev/ttyUSB0 -b 200 -U flash:w:usbasp.atmega88-modify.hex
avrdude -p m88 -c avrisp -P /dev/ttyUSB0 -b 200 -U lfuse:w:0xff:m -U hfuse:w:0xdd:m
```

SOURCE CODE I GOT FROM ORIGINAL (BEFORE MODIFY): 
2011-05-28 Thomas Fischl <tfischl@gmx.de>
http://www.fischl.de

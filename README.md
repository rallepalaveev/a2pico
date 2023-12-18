# A2retroNET RP2040

_Directly connecting the [Raspberry Pi RP2040](https://www.raspberrypi.com/products/rp2040/) to the Apple II slot bus_

[Demo Program](demo/README.md)

This is a HW implementation of Oliver Schmidt's recommended designs.

Version 1.4 is the innitial design with 3x 74LVC245 and 1x 74HC08 to prove the concept. However it is obsolete as it does not switch off the Expansion ROM ($C800-$CFFF), which is always available and could cause data bus conlisions if used with other cards that use this memory space.

Version 1.5 switches off the Expansion ROM ($C800-$CFFF) when $CFFF is accessed or when reset is issued, and switches it back on again when the slot memory is accessed (IOSelect).

Version 1.6 combines 3 of the logic chips into a PLD. 74LS08, 74LS133 and 74LS02 are replaced by ATF22V10.

The RPI usage is as follows:

| GPIO    | Usage     |
|:--------|:----------|
| 0       |  UART TX  |
| 1       |  UART RX  |
| 2 - 13  | A0 - A11  |
| 14      | R/W       |
| 15 - 22 | D0 - D7   |
| 26      | ENBL      |
| 27      | IRQ       |
| 28      | RES       |

Version "n" has support for a MicroSD card with **no** ExtROM capability.

The RPI usage of the "n" versions is as follows:

| GPIO    | Usage     |
|:--------|:----------|
| 0       |  SPI RX   |
| 1       |  SPI CSn  |
| 2       |  SPI SCK  |
| 3       |  SPI TX   |
| 4       |  NMI      |
| 5 - 12  | A0 - A7   |
| 13      | DEVSEL    |
| 14      | R/W       |
| 15 - 22 | D0 - D7   |
| 26      | ENBL      |
| 27      |  IRQ      |
| 28      |  RES      |

Version 1.7 is a successor of v1.4 by replacing the 7408 by a 7411. The data direction is controlled now by the Pico, which allows for all memory locations to be emulated. ENBL is driven by a voltage divider for minimum latency. A USB "back power" option is included.

The RPI usage is as follows:

| GPIO    | Usage     |
|:--------|:----------|
| 0       |  UART TX  |
| 1       |  DATA dir |
| 2 - 13  | A0 - A11  |
| 14      | R/W       |
| 15 - 22 | D0 - D7   |
| 26      | ENBL      |
| 27      | IRQ       |
| 28      | RES       |

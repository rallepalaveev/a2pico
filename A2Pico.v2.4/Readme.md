A2Pico Version 2.4 is a new hardware TH variant of v1.7. The major change is that A0-7 and D0-7 are multiplexed and an SD card interface is added.
The RPI usage is as follows:

| GPIO    | Usage     |
|:--------|:----------|
| 0       |  UART Tx  |
| 1       |  UART Rx  |
| 2       |  ENBL     |
| 3 - 10  | AD0 - AD7 |
| 11 - 14 | A8 - A11  |
| 15      | R/W       |
| 16      | PHI1      |
| 17      | RES       |
| 18      | IRQ       |
| 19      | CMD       |
| 20      | DAT0      |
| 21      | DAT3      |
| 22      | CLK       |
| 26      | AL-OE     |
| 27      | D-OE      |
| 28      | DDIR      |

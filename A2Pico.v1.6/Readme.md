Version 1.6 combines 3 of the logic chips into a PLD.
74LS08, 74LS133 and 74LS02 are replaced by ATF22V10.

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


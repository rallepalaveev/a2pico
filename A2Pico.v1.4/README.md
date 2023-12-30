Version 1.4 is the innitial design with 3x 74LVC245 and 1x 74HC08 to prove the concept. However it is obsolete as it does not switch off the Expansion ROM ($C800-$CFFF), which is always available and could cause data bus colisions if used with other cards that use this memory space.

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

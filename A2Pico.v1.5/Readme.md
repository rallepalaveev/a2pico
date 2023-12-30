Version 1.5 switches off the Expansion ROM ($C800-$CFFF) when $CFFF is accessed or when reset is issued, and switches it back on again when the slot memory is accessed (IOSelect).

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

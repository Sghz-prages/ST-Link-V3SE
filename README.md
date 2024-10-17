# ST-Link-V3SE
An improved version based on the ST-Link V3MINIE

This design features the following improvements over the original ST-LINK V3MINIE:
1, add exchange function for SWD and USART interface, when touching the touch panel on both sides of PCB, LED will light up, SWDIO and SWCLK will exchange pins, and touching again can stop the exchange.
2, VREF added automatic switching function, when the voltage of VREF input is lower than 1.2V, the internal will use 3.3V as VREF, when the VREF input is higher than 1.2V, the internal VREF follows the external VREF input.
3, add 5V and 3.3V power output pins and use DC-DC instead of the original LDO power supply.

Regarding the fabrication, the recommended solution is to purchase an official ST-LINK V3MINIE, and subsequently port the MCU, crystal, and level shifter ICs to the PCB of this design, and solder the remaining components. Buying the MCU on your own and burning it is a non-recommended operation because the V3 firmware is encrypted, and burning the V3 firmware that is read from other chips doesn't work properly.

It is recommended to get the MCU with V3 firmware from STM32 NUCLEO development board or ST-LINK V3.

The authors have verified that this ST-LINK V3 design is usable and can be connected to a PC and use the full functionality of the ST-LINK V3. The 24MHz SWD interface and the 21MHz JTAG interface work properly, the pin-swapping and VREF switching are valid, and the V3 firmware can be upgraded via the official ST firmware updater.

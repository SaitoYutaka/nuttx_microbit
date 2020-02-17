# nuttx_microbit
Memos that how to porting nuttx on microbit

# About Microbit
https://tech.microbit.org/hardware/

# Nuttx
https://github.com/apache/incubator-nuttx
https://github.com/apache/incubator-nuttx-apps

# Document
https://github.com/apache/incubator-nuttx/blob/nuttx-8.2/Documentation/NuttxPortingGuide.html

# UART Driver?
https://tech.microbit.org/hardware/#interface
```
item	details
Model	Freescale MKL26Z128VFM4
Core variant:	ARM Cortex-M0+
Flash ROM	128KB
RAM	16KB
Speed	16MHz
Debug capabilities	SWD
```
https://www.nxp.com/part/MKL26Z128VFM4#/

[Document](https://www.nxp.com/products/processors-and-microcontrollers/arm-microcontrollers/general-purpose-mcus/kl-series-cortex-m0-plus/kinetis-kl2x-72-96-mhz-usb-ultra-low-power-microcontrollers-mcus-based-on-arm-cortex-m0-plus-core:KL2x?fpsp=1&tab=Documentation_Tab)

boards\arm\kl\freedom-kl25z\README.txt
```
Serial Console
==============

  As with most NuttX configurations, the Freedom KL25Z configurations
  depend on having a serial console to interact with the software.  The
  Freedom KL25Z, however, has no on-board RS-232 drivers so will be
  necessary to connect the Freedom KL25Z UART pins to an external
  RS-232 driver board or TTL-to-Serial USB adaptor.

  By default UART0 is used as the serial console on this boards.  The UART0
  is configured to work with the OpenSDA USB CDC/ACM port:

    ------ ------------------------------- -----------------------------
    PIN    PIN FUNCTIONS                   BOARD SIGNALS
    ------ ------------------------------- -----------------------------
    Pin 27 PTA1/TSI0_CH2/UART0_RX/FTM2_CH0 UART1_RX_TGTMCU and D0 (PTA1)
    Pin 28 PTA2/TSI0_CH3/UART0_TX/FTM2_CH1 UART1_TX_TGTMCU and D1 (PTA2)

  But the UART0 Tx/Rx signals are also available on J1:

    ---------------- ---------
    UART0 SIGNAL     J1 pin
    ---------------- ---------
    UART0_RX (PTA1)  J1, pin 2
    UART0_TX (PTA2)  J1, pin 4

  Ground is available on J2 pin 14.  3.3V is available on J3 and J4.
```

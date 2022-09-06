# Pinout Glossary

In the world of JTAG/SWD debuggers there is a plethora of different connectors. Some are more common than others. This page is trying to collect some of the more common ones in one place. The goal is to make it bit easier to find out what signals should be connected where.

## Black Magic Debug Unified Connector (BMDU)

![](../_pinouts/unified-legend.svg)

This connector is backwards compatible with the ubiquitous [ARM Cortex 10pin Debug connector](#arm-cortex-10pin-debug-connector). We have introduced this connector on the Black Magic Probe V2.3 hardware. To add the UART connections you will have to adjust the jumpers on the back of the board. You have to disconnect the default connection on the RX pin with an exacto blade and then solder together the alternate connection on RX and TX jumpers. (TODO: Add Black Magic Probe V2.3 documentation)

## ARM Cortex Debug Connectors

There are two main connectors that are standard are very common on boards that use ARM Cortex Microcontrollers.

### ARM Cortex 10pin Debug Connector

![](../_pinouts/arm-cortex-10-legend.svg)

This is the connector provided on the Black Magic Probe debugger and is the most common JTAG/SVD connector. Keep in mind that since Black Magic Probe V2.3 we provide jumpers on the back side of the PCB allowing the user to change the connector to the [Black Magic Debug Unified Connector (BMDU)](#black-magic-debug-unified-connector-bmdu).

### ARM Cortex 20pin Debug & Trace Connector

![](../_pinouts/arm-cortex-20-legend.svg)

This connector is an expansion of the ARM Cortex 10pin debug connector and adds the parallel trace interface (Embedded Trace Macrocell). This connector can be directly used with the [ORBTrace Mini](https://orbcode.org/orbtrace-mini/).

If your target has the 20pin connector and you would like to connect the Black Magic Probe to that target. You can use a 10 to 20 pin ribbon cable that allows the connection of one half of the pins to the Black Magic Probe. ([1BitSquared](https://1bitsquared.com/products/jtag-swd-10pin-to-20pin-idc-cable) is offering this cable in their store).

## ARM JTAG Connector

![](../_pinouts/arm-jtag-20-legend.svg)

This connector is the old and trusty ARM JTAG connector. It is a bigger pitch (0.1 inch / 2.57 mm). You can find this connector on some older devices and development boards.

## STMicroelectronics STDC14

![](../_pinouts/stdc14-legend.svg)

This is a custom connector that STMicroelectronics invented. It is backwards compatible with the [ARM Cortex 10Pin Debug Connector](#arm-cortex-10pin-debug-connector). One can plug in the 14pin ribbon cable into the 10pin debug connector if the connector is not fully shrouded. The connector will then overhand two pins on each side of the connector. If your target has this connector you can connect the Black Magic Probe by connecting a 14pin ribbon cable to the Black Magic Probe ([1BitSquared](https://1bitsquared.com/products/stdc14-idc-cable) is offering these cables in their store).
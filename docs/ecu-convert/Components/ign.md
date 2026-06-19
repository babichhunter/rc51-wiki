---
sidebar_position: 7
---


# Ignition Key Switch

This guide provides detailed information about the ignition switch (IGN) used in the Honda RC51 ECU build, including its functionality, wiring, and connector details.

## Ignition Switch Description

The Honda RC51 features a standard ignition switch that provides switched power to the bike in the ON position. In the OEM setup, the ignition switch supplies main power for the electrical system and fan.

For my build, I modified the logic slightly. Instead of routing all (or most) of the bike’s power through this switch, I use it to enable several relays that then distribute power. This switch is connected via the [Main Harness](/).

Since I only use the switch to enable the relays, I stepped down the wire gauge at the end of the OEM leads. This allowed me to use a **DTM04‑3P** connector. On the main harness side, I only use one of the wires to send switched 12V back to the power supply section.

> **IMPORTANT NOTE:**  
> Refer to the [Main Harness](/) documentation for detailed wiring instructions for the ignition switch.

## Sourcing the Ignition Switch Connector

For my build, I replaced the OEM connector with a **DTM04‑3P**. I will update the OEM connector specification later.

## Ignition Switch Images

Explore this collection of images showcasing the ignition switch and its modifications.

![OEM Ignition Switch](/media/Components/IGN/IMG_8128.JPEG)
*OEM Ignition Switch*

![Modified Ignition Switch – View 1](/media/Components/IGN/IMG_8131.JPEG)
*Modified Ignition Switch – View 1*

![Modified Ignition Switch – View 2](/media/Components/IGN/IMG_8132.JPEG)
*Modified Ignition Switch – View 2*

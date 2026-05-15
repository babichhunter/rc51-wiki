---
title: Haltech HT-010300 Coolant Temperature Sensor Summary
description: Detailed overview of the Haltech HT-010300 Coolant Temperature Sensor, including specs, wiring, and ECU setup for Honda RC51 custom ECU.
---

This page provides detailed information about the Haltech HT-010300 Coolant Temperature Sensor used in the Honda RC51 custom ECU build, including specifications, connector details, wiring, and visual references.

## Haltech HT-010300 Coolant Temperature Sensor Overview

For the Engine Coolant Temperature (ECT) sensor, I chose to replace the OEM sensor with a Haltech HT-010300. This sensor matches the threads on the OEM housing, which are **M12x1.5**, and comprehensive voltage parameter documentation is readily available. While using the OEM sensor is possible, you would need to determine its resistance curve and input those values into FT Manager for the ECT input.

### Haltech Coolant Temperature Sensor Specifications

![Haltech HT-010300](https://www.haltech.com/cdn-cgi/image/width=800,format=auto/wp-content/uploads/webstore/images/HT-010300_00.JPG)
*Haltech Coolant Temperature Sensor HT-010300*

### Connector Data

The Haltech HT-010300 sensor uses a Delphi 2-Pin GM-style Coolant Temperature Connector (Part #HT-030411). The exact connector is the [Delphi 12162193](https://www.corsa-technic.com/item.php?item_id=306&category_id=81).

![HT-010300 ECT Sensor Connector](https://www.haltech.com/cdn-cgi/image/width=800,format=auto/wp-content/uploads/webstore/images/HT-030411_00.JPG)
*Delphi 2-Pin GM-style Coolant Temperature Connector*

:::note IMPORTANT NOTE
Pay careful attention to the connector you are provided with. The connector I received was not a pull-to-seat connector, contrary to what is stated on Haltech's website. However, I did receive the correct documentation with my purchased sensor. I received the rear-insert connector [Delphi: 15449028](https://www.corsa-technic.com/item.php?item_id=459&category_id=96). Always double-check the style of connector you are provided with.
:::

### Mounting the ECT Sensor

The threads on the OEM sensor are **M12x1.5**, which match those of the Haltech HT-010300. Mount the sensor in the OEM thermostat housing. No special modifications are required.

### ECU Setup

ECU configuration for the Haltech HT-010300 sensor is straightforward, as FuelTech provides default configurations for this sensor. FuelTech includes a predefined **GM Temperature Sensor (USA)** configuration, which can be used. Alternatively, you could update the Custom Interpolation table with the values provided by Haltech, but the voltage tables are nearly identical, and the FuelTech table offers greater resolution.

1. Open **FT Manager**.
2. Navigate to **Sensors and Calibration**.
3. Click on the **Inputs** tab.
4. Locate your **Engine Temp** input field.
5. Select the predefined sensor parameter, **GM Temperature Sensor (USA)**.

![Configuring the FT Manager tune with ECT Sensor parameters](/media/Components/ECT/FTManager_ect-setup.png)
*Configuring the FT Manager tune with ECT Sensor parameters*

**Note:** The original HTML included an interactive chart comparing FuelTech and Haltech calibration tables. You can replace the placeholder below with an image export of that chart.

![Coolant Temperature Sensor Calibration Chart]
*Comparison of FuelTech default and Haltech provided calibration tables*

### Wiring Diagram

The Haltech HT-010300 sensor uses a Delphi 2-Pin GM-style Coolant Temperature Connector with the following pinout: Pin A - Signal Ground, Pin B - Signal. Wiring is straightforward; refer to the [Haltech manual] for additional details if needed. You can use any available white input.

**Important:** Connect the housing ground wire as normal to ground the thermostat housing (part of the [Main Harness]; this should not be omitted.

![Wiring Diagram ECT Sensor]
*Wiring Diagram for ECT Sensor*

The ECT sensor is part of the [Sensors sub-harness]. Refer to that documentation for electrical integration and wiring of the ECT.

### Coolant Temperature Sensor Images

Explore this collection of high-resolution images showcasing the Haltech HT-010300 Coolant Temperature Sensor and its installation.

![Haltech GM Style ECT Sensor]
*Haltech GM Style ECT Sensor*

![Haltech GM Style ECT Sensor Documentation]
*Haltech GM Style ECT Sensor (Documentation)*

### Quick Links

- [Haltech ECT Sensor](https://www.haltech.com/product/ht-010300-coolant-temp-sensor-small-thread/)
- [Delphi 2-Pin GM-style Coolant Temperature Connector](https://www.haltech.com/product/ht-030411-plug-and-pins-only-delphi-2-pin-gm-style/)
- [Haltech Manual]
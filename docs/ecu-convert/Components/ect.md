---
title: ECT Sensor
sidebar_position: 8
---

This page provides detailed information about the Haltech HT-010300 Coolant Temperature Sensor used in the Honda RC51 custom ECU build, including specifications, connector details, wiring, and visual references.

---

## Haltech HT-010300 Coolant Temperature Sensor Overview

For the Engine Coolant Temperature (ECT) sensor, I chose to replace the OEM sensor with a Haltech HT-010300. This sensor matches the threads on the OEM housing, which are **M12x1.5**, and comprehensive voltage parameter documentation is readily available.

While using the OEM sensor is possible, you would need to determine its resistance curve and input those values into FT Manager for the ECT input.

---

## Haltech Coolant Temperature Sensor Specifications

<div align="center">

![Haltech HT-010300](https://www.haltech.com/cdn-cgi/image/width=800,format=auto/wp-content/uploads/webstore/images/HT-010300_00.JPG)

*Haltech Coolant Temperature Sensor HT-010300*

</div>

---

## Connector Data

The Haltech HT-010300 sensor uses a Delphi 2-Pin GM-style Coolant Temperature Connector (Part #HT-030411).

The exact connector is the [Delphi 12162193](https://www.corsa-technic.com/item.php?item_id=306&category_id=81).

<div align="center">

![HT-010300 ECT Sensor Connector](https://www.haltech.com/cdn-cgi/image/width=800,format=auto/wp-content/uploads/webstore/images/HT-030411_00.JPG)

*Delphi 2-Pin GM-style Coolant Temperature Connector*

</div>

:::note IMPORTANT NOTE
Pay careful attention to the connector you are provided with. The connector I received was not a pull-to-seat connector, contrary to what is stated on Haltech's website.

However, I did receive the correct documentation with my purchased sensor. I received the rear-insert connector [Delphi: 15449028](https://www.corsa-technic.com/item.php?item_id=459&category_id=96).

Always double-check the style of connector you are provided with.
:::

---

## Mounting the ECT Sensor

The threads on the OEM sensor are **M12x1.5**, which match those of the Haltech HT-010300.

Mount the sensor in the OEM thermostat housing. No special modifications are required.

---

## ECU Setup

ECU configuration for the Haltech HT-010300 sensor is straightforward, as FuelTech provides default configurations for this sensor.

FuelTech includes a predefined **GM Temperature Sensor (USA)** configuration, which can be used. Alternatively, you could update the Custom Interpolation table with the values provided by Haltech, but the voltage tables are nearly identical, and the FuelTech table offers greater resolution.

### FT Manager Setup Steps

1. Open **FT Manager**
2. Navigate to **Sensors and Calibration**
3. Click on the **Inputs** tab
4. Locate your **Engine Temp** input field
5. Select **GM Temperature Sensor (USA)**

<div align="center">

![Configuring the FT Manager tune with ECT Sensor parameters](/media/Components/ECT/FTManager_ect-setup.png)

*FT Manager ECT Sensor Configuration*

</div>

---

## Calibration Comparison

The plot below compares the default FuelTech GM-style calibration table with the calibration data provided by Haltech for the HT-010300 sensor.

<div align="center">

![Coolant Temperature Sensor Calibration Chart](/media/Components/ECT/coolant_sensor_comparison_plot.png)

*Comparison of FuelTech default and Haltech provided calibration tables*

</div>

### Calibration Table Comparison

| Volts | FuelTech Default: GM Style (°F) | Haltech Calibration Table (°F) |
|--------|----------------------------------|--------------------------------|
| 0.000  | 356                              | —                              |
| 0.356  | 266                              | —                              |
| 0.450  | —                                | 248                            |
| 0.747  | 212                              | —                              |
| 0.750  | —                                | 212                            |
| 0.960  | 194                              | —                              |
| 0.970  | —                                | 194                            |
| 1.238  | 176                              | —                              |
| 1.580  | —                                | 158                            |
| 1.581  | 158                              | —                              |
| 1.988  | 140                              | —                              |
| 2.450  | —                                | 122                            |
| 2.955  | 104                              | —                              |
| 3.430  | —                                | 86                             |
| 3.879  | 68                               | —                              |
| 4.210  | —                                | 50                             |
| 4.512  | 32                               | —                              |
| 4.660  | —                                | 14                             |
| 4.806  | -4                               | —                              |

---

## Wiring Diagram

The Haltech HT-010300 sensor uses a Delphi 2-Pin GM-style Coolant Temperature Connector with the following pinout:

- **Pin A** — Signal Ground
- **Pin B** — Signal

Wiring is straightforward; refer to the [Haltech manual](/media/Components/ECT/HT-010300.pdf) for additional details if needed.

You can use any available white input.

> **Important:** Connect the housing ground wire normally to ground the thermostat housing (part of the Main Harness). This should not be omitted.

<div align="center">

![Wiring Diagram ECT Sensor](/media/Components/ECT/ECT-WS.png)

*ECT Sensor Wiring Diagram*

</div>

The ECT sensor is part of the Sensors sub-harness. Refer to that documentation for electrical integration and wiring of the ECT.

---

## Coolant Temperature Sensor Images

Explore this collection of high-resolution images showcasing the Haltech HT-010300 Coolant Temperature Sensor and its installation.

| | |
|---|---|
| ![](/media/Components/ECT/IMG_8084.JPEG) | ![](/media/Components/ECT/IMG_8160.JPEG) |
| *Haltech GM Style ECT Sensor* | *Installed Sensor View* |

<div align="center">

![Haltech GM Style ECT Sensor Documentation](/media/Components/ECT/IMG_8140.JPEG)

*Haltech GM Style ECT Sensor Documentation*

</div>

---

## Quick Links

- [Haltech ECT Sensor](https://www.haltech.com/product/ht-010300-coolant-temp-sensor-small-thread/)
- [Delphi 2-Pin GM-style Coolant Temperature Connector](https://www.haltech.com/product/ht-030411-plug-and-pins-only-delphi-2-pin-gm-style/)
- [Haltech Manual](/media/Components/ECT/HT-010300.pdf)

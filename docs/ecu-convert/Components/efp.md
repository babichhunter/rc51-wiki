# FuelTech 0–150 PSI Pressure Sensor Summary

This page provides detailed information about the FuelTech 0–150 PSI Pressure Sensor used in the Honda RC51 custom ECU build, including its specifications, connector details, wiring, and visual references.

## FuelTech 0–150 PSI Pressure Sensor Overview

While a fuel pressure sensor is not mandatory for ECU operation, it is highly recommended to properly calculate injector pulse times. The Honda RC51’s stock fuel system is a regulated return‑style system, operating at approximately 50-52 PSI. Adding a fuel pressure sensor, such as the FuelTech 0–150 PSI sensor, is straightforward and provides valuable real‑time data for monitoring fuel pressure.

In this build, a FuelTech 0–150 PSI sensor (Part #5005100020‑BLK) was used, but any fuel‑compatible pressure sensor can be used, provided the input is correctly configured in FT Manager.

## FuelTech 0–150 PSI Pressure Sensor Specifications

The FuelTech PS‑150 Pressure Sensor (Part #5005100020‑BLK) is designed for accurate and reliable pressure readings in the range of 0–150 PSI.

![FuelTech PS-150](https://www.fueltech.net/cdn/shop/files/FuelTech-150-psi-Pressure-Sensor_1024x1024.jpg?v=1736975723)
*FuelTech PS‑150 0–150 PSI Pressure Sensor*

## Connector Data

The FuelTech PS‑150 Pressure Sensor uses a 3‑pin connector (Delphi: 12065287) for secure and reliable data transmission to the ECU. The connector kit ensures proper integration with the RC51’s wiring harness.

### Connector Specifications

| Component | Part Number |
|----------|-------------|
| Pan Vacuum/Pressure Sensor 3‑Pin Connector Kit | Delphi: 12065287 |

![FuelTech 3-Pin Connector](https://www.fueltech.net/cdn/shop/products/FuelTech-Pan-Vacuum-Pressure-Sensor-Electrical-Connector_1024x1024.png?v=1728421022)
*FuelTech 3‑Pin Connector Kit*

More information on the exact connector specifications can be found  
[here](https://www.corsa-technic.com/item.php?item_id=314&category_id=142).

## ECU Setup

ECU configuration for the FuelTech 0–150 PSI sensor is very straightforward. Follow the steps below and select the predefined sensor configuration.

1. Open **FT Manager**.
2. Navigate to **Sensors and Calibration**.
3. Click on the **Inputs** tab.
4. Locate your **Fuel Pressure** input field.
5. Select the correct default sensor parameter.

![FT Manager Setup](/media/Components/FPS/FT_Manager-EFP-setup.png)
*Configuring FT Manager with Fuel Pressure Sensor parameters*

## Physical Placement

Since there is no OEM sensor for fuel pressure, the sensor was added to the main fuel feed line. Refer to the  
[Fuel Lines](/home) documentation for details.

## Wiring Diagram

The FuelTech PS‑150 Pressure Sensor uses a 3‑pin connector with the following pinout:

- **Pin A** — Ground  
- **Pin B** — 5V  
- **Pin C** — Signal  

Wiring is straightforward and can be connected to any available white input on the ECU. Refer to the FuelTech manuals for additional details if needed.

## FuelTech Manual

For detailed installation and configuration instructions, refer to the official FuelTech manual:  
[FuelTech Support Page](https://www.fueltech.net/pages/support)

## Quick Links

- [FuelTech PS‑150 Pressure Sensor](https://www.fueltech.net/collections/pressure-sensors/products/pressure-sensor)
- [FuelTech Pressure Sensor 3‑Pin Connector Kit](https://www.fueltech.net/collections/connectors-sensor-plug-kits/products/pressure-sensor-pan-vacuum-sensor-plug-kit)
- [FuelTech Pressure Sensor Manual](https://files.fueltech.net/manuals/Sensor_PS.pdf)

# Oil Pressure Sensor

This page provides detailed information about the FuelTech 0–150 PSI Oil Pressure Sensor used in the Honda RC51 custom ECU build, including its specifications, connector details, wiring, and visual references.

## FuelTech 0–150 PSI Oil Pressure Sensor Overview

While an oil pressure sensor is not required for ECU operation, it is highly recommended for monitoring engine health and ensuring safe operation. The Honda RC51’s OEM setup uses a pressure switch, not a sensor, so it does not actually read pressure.

Adding an oil pressure sensor, such as the FuelTech 0–150 PSI sensor, is straightforward and provides critical real‑time data for monitoring oil pressure. In this example, a FuelTech 0–150 PSI sensor (Part #5005100020‑BLK) was used, but any oil‑compatible pressure sensor is acceptable, provided the input is correctly configured in FT Manager.

This is the same sensor used for fuel pressure.

## FuelTech 0–150 PSI Oil Pressure Sensor Specifications

The FuelTech PS‑150 Pressure Sensor (Part #5005100020‑BLK) is designed for accurate and reliable pressure readings in the range of 0–150 PSI. It is suitable for monitoring oil, fuel, or wastegate pressure, making it a versatile component for performance‑driven setups.

## Connector Data

The FuelTech PS‑150 Oil Pressure Sensor uses a 3‑pin Delphi connector (Part #12065287) for secure and reliable data transmission to the engine management system. Below are the details for the connector kit found on FuelTech’s website.

### Connector Specifications

| Component | Part Number |
|----------|-------------|
| Oil Pressure Sensor 3‑Pin Connector Kit | Delphi: 12065287 |

![FuelTech 3-Pin Connector](https://www.fueltech.net/cdn/shop/products/FuelTech-Pan-Vacuum-Pressure-Sensor-Electrical-Connector_1024x1024.png?v=1728421022)
*FuelTech 3‑Pin Connector Kit*

More information on the exact connector specifications can be found  
[here](https://www.corsa-technic.com/item.php?item_id=314&category_id=142).

## Mounting the Pressure Sensor

To mount the PS‑150 oil pressure sensor in place of the stock oil pressure switch, note that the PS‑150 uses **1/8"-27 NPT** threads, while the stock switch uses **1/8" BSPT** threads (28 TPI) with a slightly smaller major diameter (0.383" vs. 0.405").

Because BSPT and NPT differ in:

- Thread angle (55° vs. 60°)  
- Pitch  
- Major diameter  

…they are **not compatible**.

A **1/8" BSPT → 1/8" NPT female adapter** (commonly found on Amazon or eBay) allows the PS‑150 sensor to be securely installed in the OEM switch location.

## ECU Setup

ECU configuration for the FuelTech 0–150 PSI sensor is very straightforward and identical to the Fuel Pressure Sensor setup. Follow the steps below and select the predefined sensor configuration.

1. Open **FT Manager**.
2. Navigate to **Sensors and Calibration**.
3. Click on the **Inputs** tab.
4. Locate your **Oil Pressure** input field.
5. Select the correct default sensor parameter.

![FT Manager Oil Pressure Setup](/media/Components/OPS/FTManager_eop-setup.png)
*Configuring FT Manager with Oil Pressure Sensor parameters*

## Wiring Diagram

The FuelTech PS‑150 Oil Pressure Sensor uses a 3‑pin connector with the following pinout:

- **Pin A** — Ground  
- **Pin B** — 5V  
- **Pin C** — Signal  

Wiring is straightforward and can be connected to any available white input on the ECU. Refer to the FuelTech manuals for additional details if needed.

## Oil Pressure Sensor Images

Below are images showing the adapter and installed sensor.

![Thread Adapter](/media/Components/OPS/IMG_8085.JPEG)
*Thread Adapter for Oil Pressure Sensor*

![Installed Sensor](/media/Components/OPS/IMG_8087.JPEG)
*Installed Oil Pressure Sensor*

## FuelTech Manual

For detailed installation and configuration instructions, refer to the official FuelTech manual:  
[FuelTech Support Page](https://www.fueltech.net/pages/support)

## Quick Links

- [FuelTech PS‑150 Oil Pressure Sensor](https://www.fueltech.net/collections/pressure-sensors/products/ps-150-pressure-sensor)
- [FuelTech Oil Pressure Sensor 3‑Pin Connector Kit](https://www.fueltech.net/collections/connectors-sensor-plug-kits/products/pressure-sensor-pan-vacuum-sensor-plug-kit)
- [FuelTech Oil Pressure Sensor Manual](https://www.fueltech.net/pages/manuals)

---
sidebar_position: 5
---


# Throttle Position Sensor (TPS)

This page provides detailed information about the Throttle Position Sensor (TPS) used in the Honda RC51, including its specifications, connector details, visual references, and technical documentation.

## TPS Description and Ohm Readings

The Honda RC51 employs a single Throttle Position Sensor (TPS) mounted on the throttle body to monitor the throttle valve position. The TPS is a potentiometer that sends a variable voltage signal to the ECU, indicating the throttle opening angle, which is critical for precise fuel delivery and ignition timing. The TPS is connected via the fuel injector sub‑harness.

Measuring the resistance (ohm readings) of the TPS is essential for verifying its functionality. Using a multimeter across the sensor terminals, the expected readings are as follows:

### TPS Resistance Specifications

| Measurement | Resistance (Ohms) | Notes |
|------------|-------------------|-------|
| Between VCC and GND (total resistance) | Approx. 5.05 kΩ | Measure at room temperature (approx. 20°C / 68°F). |
| Between Signal and GND (variable) | Approx. 0.870 kΩ (closed) – 5.07 kΩ (open) | Varies with throttle position; fully closed to fully open. |

These ohm readings serve as a reference. The TPS should be calibrated in FT Manager during the setup of the base tune to ensure accurate performance.

## Connector Data

The TPS on the Honda RC51 uses a **Sumitomo 6189‑0154 HW Sealed Series 3‑pin connector**, integrated into the fuel injector sub‑harness. This is the same connector type used for the MAP sensor.

### TPS Connector Specifications

| Property | Details |
|----------|---------|
| Connector Type | Sumitomo 6189‑0154, HW Sealed Series (3‑pin) |
| Pin Configuration | Pin A: +5V (VCC), Pin B: Signal Output, Pin C: Sensor Ground |
| Wire Gauge | Pin A: 20 AWG, Pin B: 22 AWG, Pin C: 20 AWG |

Proper pin assignment is critical for the TPS, as incorrect connections can lead to erratic ECU readings. Always verify pin assignments using the Honda RC51 service manual. Refer to the [FI Sub‑Harness](/) page for a detailed wiring diagram.

## Sourcing the TPS Connector

The TPS connector can be sourced from the following reputable suppliers:

- [Cycle Terminal – 3‑pin HW .090 Female Connector](https://www.cycleterminal.com/hw-series-090.html)
- [KSV Looms – SKU: OE10835](https://www.ksvlooms.com/products/3-way-connector-kit-for-honda-s2000-f20-f22-tps-throttle-position-sensor-22-16-awg-1)
- [Corsa Technic – Connector Specifications](https://www.corsa-technic.com/item.php?item_id=392&category_id=113)

## Throttle Position Sensor Images

Explore this collection of high‑resolution images showcasing the Honda RC51 Throttle Position Sensor, including the connector (pin and seal sides) and the TPS with its connector attached.

![TPS Connector – Pin Side](/media/Components/TPS/TPS_Cntr_pinside.jpg)
*TPS Connector – Pin Side*

![TPS Connector – Seal Side](/media/Components/TPS/TPS_Cntr_sealside.jpg)
*TPS Connector – Seal Side*

![TPS Sensor](/media/Components/TPS/tps_1.JPEG)
*TPS Sensor*

![TPS Sensor Pins](/media/Components/TPS/tps_unit_pins1.JPEG)
*TPS Sensor Pins*

![TPS with Connector](/media/Components/TPS/tps_wc_1.JPEG)
*TPS with Connector*

![TPS with Connector](/media/Components/TPS/tps_wc_2.JPEG)
*TPS with Connector*

## Wiring Diagram

Refer to the [OEM FISH](/) or the [Custom FISH](/) for detailed wiring information.

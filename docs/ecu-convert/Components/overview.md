# Overview

This section outlines the critical sensors and components required for the FuelTech FT550 ECU to operate properly—and for the motorcycle itself. It includes both aftermarket upgrades and OEM component adaptations, along with setup notes for FT Manager and any wiring modifications. Throughout this wiki, most connections were converted to Deutsch DT or DTM whenever possible. OEM connectors were also sourced so you can reuse them if desired.

## 🔧 Required Sensors for FT550 Operation

The FT550 requires several key inputs to function correctly:

- Throttle Position Sensor (TPS)
- Manifold Absolute Pressure (MAP) Sensor (FT550 integrated or OEM)
- Coolant Temperature Sensor (ECT)
- Intake Air Temperature Sensor (IAT)
- Crankshaft Position Sensor (TRIG)
- Camshaft Position Sensor (CSYNC)
- Wideband O2 Sensor (via NanoPro or equivalent)
- Fuel Pressure Sensor (optional but recommended)
- Oil Pressure Sensor (optional but recommended)

## ⚙️ Aftermarket Components

As outlined in the [Project Planning](/docs/ecu-convert/Introduction/project-planning) page, several aftermarket components were used to ensure compatibility and reliability:

- [FuelTech NanoPro](https://www.fueltech.net/collections/o2-conditioners/products/nanopro) – Wideband O2 interface  
- [FuelTech Pressure Sensors](https://www.fueltech.net/collections/pressure-sensors/products/pressure-sensor) – Fuel and oil pressure monitoring  
- [Haltech ECT Sensor](https://www.haltech.com/product/ht-010300-coolant-temp-sensor-small-thread/) – Coolant temperature input  
- [CBR 600RR COP Conversion](https://www.rc51forums.com/threads/how-to-600rr-coil-on-plug-conversion.6482/) – Required for SparkPRO ignition setup  
- FT550 Integrated MAP Sensor – Internal MAP sensor used; OEM MAP requires calibration table  
- [SPAL Fan Upgrade](https://www.rc51forums.com/threads/rc51-sp2-only-spal-fan-mounts-proof-of-concept-and-sign-up-thread.71393/?post_id=760105&nested_view=1&sortby=oldest#post-760105) – Pusher SPAL fans for each radiator  

## 🧩 OEM Component Integration (ECU Related)

Aftermarket ECUs are highly configurable. As long as you understand how a sensor behaves, you can often reuse OEM components. Many RC51 sensors work with the FT550, though some require specific configuration.

- **OEM TPS:** Fully compatible; calibrate in FT Manager  
- **OEM IAT:** Requires voltage calibration under Inputs  
- **OEM Crank Sensor:** VR sensor; must be configured with correct polarity  
- **OEM Cam Sensor:** VR sensor; determines engine phase; also polarity‑sensitive  
- **OEM Bank Angle Sensor:** Integrated into custom main harness; mimics OEM logic  
- **OEM Transmission RPM Sensor:** Output shaft speed sensor  
- **OEM Fuel Pump:** Reused in‑tank pump and regulator  
- **OEM Fuel Injectors:** Reused OEM Denso injectors  

## 🧩 OEM Component Integration (Non‑ECU Related)

These components are part of the custom “Main Harness,” separate from the ECU harness. This allows a race‑only version to be built later by removing the main harness.

- Starter Relay  
- Starter Motor  
- Alternator  
- Rectifier  
- Side Stand Switch  
- Neutral Switch  
- LED Front Turn Signals  
- Hot Bodies LED Taillights/Turn Signals  
- LED Plate Light  
- Headlights  
- Ignition Switch  
- Brake Switches  
- Low Fuel Reading Thermistor  
- (“OEM”) Ducati Clutch and Front Brake Switches  

Additional components like handlebar switches and the custom light bar are documented elsewhere.

## 🛠 Setup in FT Manager

Each sensor must be configured in FT Manager with the correct input type, calibration curve, and filtering settings.

Key setup tasks include:

- Assigning input channels  
- Loading calibration data (resistance tables, voltage curves)  
- Setting filtering and update rates  
- Verifying live data during initial power‑up  

These tasks are documented in each component’s section.

## 🔌 Wiring Modifications

Wiring changes were made to improve reliability and aesthetics:

- Splicing or replacing connectors with compatible terminals  
- Shielding signal wires (especially crank and cam sensors)  
- Routing sensor grounds properly to avoid noise  
- Adding harness protection using Raychem DR‑25 and SCL  
- Labeling and documenting each harness branch  

> **Tip:**  
> Each component’s section includes logic and troubleshooting notes to simplify diagnostics.

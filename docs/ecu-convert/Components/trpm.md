# Driveshaft RPM Sensor

This guide details the Driveshaft RPM sensor, also known as the vehicle speed sensor, used in my Honda RC51 custom ECU build, including its specifications, connector details, wiring, ECU setup in FT Manager, and visual references.

## Driveshaft RPM Sensor Overview

The Driveshaft RPM sensor allows the FT550 ECU to determine vehicle speed by monitoring the rotation of the driveshaft. In my RC51 build, this sensor enables features like speed‑based tuning and traction control. It is a Hall Effect sensor that outputs a 5V digital square wave signal proportional to shaft speed.

## Driveshaft RPM Sensor Specifications

The OEM Honda RC51 Driveshaft RPM sensor is mounted near the counter‑shaft and reads from a gear with **27 teeth**, generating **27 pulses per revolution**, as noted in the Speedzilla post [here](https://www.speedzilla.com/threads/my-home-built-rc51-gear-position-indicator-includes-plans.43866/).

## Connector Data

For my build, I replaced the OEM connector with a **DTM04‑3P** to match my custom harness. I will update the OEM connector specifications later.

## ECU Setup in FT Manager

Configure the sensor in FT Manager under **Sensors and Calibration → Inputs**.

- Select a **white input** for *Driveshaft RPM*  
- Set the sensor type to **Hall Effect**  
- Input the pulse count: **27 pulses per revolution**  
- Configure the **differential ratio** and **tire specifications** for accurate speed calculations  

> **IMPORTANT NOTE:**  
> FT Manager must be configured to match the rear tire size and sprocket setup for accurate speed calculation.  
> Use the tire circumference (**190/50 R17**) and final drive ratio (**16F/40R = 2.5**) as stock reference values.

## Driveshaft RPM Sensor Images

![Installed Driveshaft RPM Sensor – View 1](/media/Components/TRPM/IMG_8119.JPEG)
*Installed Driveshaft RPM Sensor – View 1*

![Installed Driveshaft RPM Sensor – View 2](/media/Components/TRPM/IMG_8120.JPEG)
*Installed Driveshaft RPM Sensor – View 2*

![Installed Driveshaft RPM Sensor – View 3](/media/Components/TRPM/IMG_8121.JPEG)
*Installed Driveshaft RPM Sensor – View 3*

![Driveshaft RPM Sensor Connector](/media/Components/TRPM/IMG_8123.JPEG)
*Driveshaft RPM Sensor Connector*

![FT Manager Driveshaft RPM Input Configuration](/media/Components/TRPM/FTManager-trpm-setup-Inputs.png)
*FT Manager Driveshaft RPM Input Configuration*

![FT Manager Vehicle Speed Configuration](/media/Components/TRPM/FTManager-trpm-setup-dsrpm.png)
*FT Manager Vehicle Speed Configuration*

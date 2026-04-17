---
id: project-planning
title: Project Planning
sidebar_position: 2
---

> ⚠️ **Work in Progress**  
> This wiki is actively being developed and refined. Information may change as new data, testing, and revisions are added.  
> While every effort is made to ensure accuracy, always verify technical details independently before applying them to your own build.

The first part of this kind of project is to define what we want to accomplish. I wanted an aftermarket ECU to run on my '03 RC51.  
Next is to plan how to implement this.

## ECU Selection

I selected a [FuelTech FT550](https://www.fueltech.net/products/ft550-efi-system) for this project. You can choose any ECU, but the nice thing about the FT550 is that it has a screen built into the ECU and serves as an all‑in‑one. Also, I already had it sitting around unused, so that helped narrow down the choices.

Every ECU has its advantages and disadvantages. It helps to know the limitations of different systems and what would work best for your application.

![FuelTech FT550 ECU](/media/FT550_EN/T - FT550 - Dual - Dash 03 - USA.png)

## Supporting the ECU

Now that an ECU is selected, we need to know what components are required to support it so it can function properly.  
Below is a list of supporting components required for the RC51 application. (These are explained in more detail in their respective documentation.)

- [FuelTech NanoPro](https://www.fueltech.net/collections/o2-conditioners/products/nanopro)
- [Bosch LSU4.9 O2 Sensor](https://www.bosch-motorsport.com/content/downloads/Raceparts/en-GB/51865867208058251.html)
- Exhaust O2 Bungs
- [CBR 600RR COP Conversion](https://www.rc51forums.com/threads/how-to-600rr-coil-on-plug-conversion.6482/?post_id=45671&nested_view=1&sortby=oldest#post-45671)
- [FuelTech SparkPRO‑2](https://www.fueltech.net/collections/sparkpro/products/sparkpro-2)
- [FuelTech Fuel/Oil Pressure Sensors](https://www.fueltech.net/collections/pressure-sensors/products/pressure-sensor)
- [Haltech Coolant Pressure Sensor](https://www.haltech.com/product/ht-010300-coolant-temp-sensor-small-thread/)
- [Logical Power Supply System](https://hondarc51.com/ecu-wiki/power-supply) or a PDU

You can reuse the rest of the OEM sensors and switches for everything else.

Now that we have an idea of the components needed to support the FT550, next let’s discuss some of the software used for this project.

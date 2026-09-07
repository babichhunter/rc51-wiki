---
title: Injectors
sidebar_position: 1
---

#This page provides detailed information about the fuel injectors used in the Honda RC51, including their specifications, connector details, visual references, and technical documentation as well as their integration into the FT Manager.


## Fuel Injector Description and Ohm Readings


        The Honda RC51 (RVT1000R) uses four fuel injectors, two per cylinder (primary and secondary). These are Denso high-impedance, top-feed injectors. Each injector is a solenoid-operated valve controlled by the ECU, with the primary injector handling base fuel delivery and the secondary injector supplementing at higher RPMs or under heavier loads. The injectors are labeled as Injector 1-1 (rear primary), Injector 1-2 (rear secondary), Injector 2-1 (front primary), and Injector 2-2 (front secondary), following the sub-harness labeling convention where the rear cylinder is designated as Cylinder #1.


        Important: As mentioned in another section of this wiki, I reversed this logic and refer to the front cylinder as Cyl #1 and the rear as Cyl #2.


        The resistance (ohm readings) of the injectors is critical for verifying their functionality. Using a multimeter across the injector terminals, the expected readings are:


        Fuel Injector Resistance Specifications


| Injector | Resistance (Ohms) | Notes |
| --- | --- | --- |
| All Injectors | 12.0–12.5 Ω | Measure at room temperature (approx. 20°C / 68°F). |


        If readings fall outside this range, the injector may be faulty and should be inspected for clogs or electrical issues. Always disconnect the injector connector before testing to avoid ECU damage.


        Being high-impedance injectors, an external injector driver is not required, and the FT ECU can handle the injectors directly.


## Connector Data


        The fuel injectors on the Honda RC51 use 2-pin connectors integrated into the fuel injector sub-harness (FISH). See the table below for specific injector and connector type information:


        Fuel Injector Connector Specifications


            [Sumitomo 6195-0043](https://www.corsa-technic.com/item.php?item_id=699)


| Property | Details |
| --- | --- |
| Connector Type | or 6195-0041 |
| Pin Configuration | Pin A: ECU Output - Signal GroundPin B: +12V (switched) |
| Wire Gauge | 22 AWG (for individual injector) |


        Note: Polarity is not critical for the injectors, as they are simple solenoids, but always verify pin assignments with the RC51 service manual to ensure proper connection to the sub-harness. See the [FI Sub-Harness](/ecu-wiki/custom/fi-sub-harness) page for a wiring diagram. The 22 AWG gauge for the injectors is sufficient for splices from the main +12V line.


## Sourcing the Injector Connector


        You can source the connector for the four injectors from the following locations (ensure they are High Key):


- [Motorcycle Terminal - 6195-0041](https://www.cycleterminal.com/fuel-injector-connectors.html)

- [KSV Looms - SKU: OE10269](https://www.ksvlooms.com/products/nippon-denso-2-pin-fuel-injector-connector-plug-clip-kit-id2000-high-tag)

- [Corsa Technic](https://www.corsa-technic.com/item.php?item_id=699)

- [ProWireUSA](https://www.prowireusa.com/p-4044-2-way-denso-injector-connector-kit.html)


        Additional specifications can be found [here](https://www.corsa-technic.com/item_docs/DL090-CAT.pdf).


## Flow Testing the Injectors


        I sent my injectors in for cleaning and flow testing. While they were not excessively dirty, the process provided valuable data about the OEM injectors. I used [Fuel Injector Clinic](https://www.fuelinjectorclinic.com). They replaced all seals, filter baskets, and cushioning rings as part of the service—an excellent value considering the cost of purchasing those components separately.


        Below are the results of the flow test before and after cleaning, along with the Data Match report:


- [Flow Testing Results](/files/Inj Flow Data Sheet.pdf)

- [Data Match Results](/files/Inj Slope_Offset_Data.pdf)


        OEM Denso injectors are rated at 310cc/min (but test around 305cc/min) and have an average dead time of 1ms.


## Fuel Injector Setup Guide


### Step-by-Step Instructions


1. Open **FT Manager**.

1. Navigate to **Engine Settings**.

1. Click on the **Fuel Injection** tab.

1. Locate the **(Primary & Secondary) Total Flow** input field.

1. Convert your injector flow rate from *cc/min* to *lb/hr* using the formula below, then enter the result for both Primary and Secondary.

1. Set the **Injector Dead Time** according to your injector specifications.


### Conversion Formula: cc/min → lb/hr


            Fuel injectors are often rated in cubic centimeters per minute (cc/min), but many ECU systems require the value in pounds per hour (lb/hr).


            **Formula:**

            `lb/hr = cc/min ÷ 10.5`


- `cc/min` = injector flow rate in cubic centimeters per minute

- 10.5 = conversion factor (cc/min to lb/hr)


#### Example Calculation


```
lb/hr = 305 ÷ 10.5
            lb/hr ≈ 29.05 lb/hr per injector
```


### Setting Injector Dead Time


            Injector dead time (also called latency) is the time it takes for the injector to open and close, typically given in milliseconds (ms).


            Enter the value provided by your injector manufacturer, often specified for different battery voltages. Example:


```
Voltage (V) | Dead Time (ms)
            ----------------------------
            13.5        | 1.00
```


I only received a single entry for this parameter, 996 ms @ 13.5V. We will see if I run into any issues down the road, especially at startup or high RPM.


            ![Injector Configuration](/files/FTManager_InjConfig.png)[](/files/FTManager_InjConfig.png)

*Configuring the FT Manager tune with injector data*


## Fuel Injector Reference Images


        Below is a collection of images showing the OEM fuel injectors used in the Honda RC51. The set includes detailed views of the injector body, electrical connector (pin and seal sides), and assembled injector units with connectors.


            ![OEM Injector Connector - Pin Side](/files/Inj_cntr_pinside.jpg)[](/files/Inj_cntr_pinside.jpg)

*OEM Injector Connector – Pin Side*


            ![OEM Injector Connector - Seal Side](/files/Inj_cntr_sealside.jpg)[](/files/Inj_cntr_sealside.jpg)

*OEM Injector Connector – Seal Side*


            ![OEM Fuel Injector](/files/Inj_unit_cntr-1.JPEG)[](/files/Inj_unit_cntr-1.JPEG)

*OEM Fuel Injector*


            ![OEM Fuel Injector](/files/Inj_unit_cntr-2.JPEG)[](/files/Inj_unit_cntr-2.JPEG)

*OEM Fuel Injector*


            ![OEM Fuel Injector with Connector](/files/inj_wc_1.JPEG)[](/files/inj_wc_1.JPEG)

*OEM Fuel Injector with Connector*


            ![OEM Fuel Injector with Connector](/files/inj_wc_2.JPEG)[](/files/inj_wc_2.JPEG)

*OEM Fuel Injector with Connector*


            ![OEM Fuel Injector with Connector](/files/inj_wc_3.JPEG)[](/files/inj_wc_3.JPEG)

*OEM Fuel Injector with Connector*


## Wiring Diagram


        Refer to the [FISH](/ecu-wiki/custom/fi-sub-harness) documentation for wiring of the fuel injectors.
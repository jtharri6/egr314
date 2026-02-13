---
title: Module's Selected Major Components
---

This page outlines the main components selected for the I2C ToF sensor module, starting with the supporting power, sensing, and indicator components used in the design and ending with the selected microcontroller PIC18F47K42. 

### Power Management

**3.3 V Regulator**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](1.png)<br>**LMR16006YQ3DDCRQ1** <br><br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LMR16006YQ3DDCRQ1/5395814) | \* fixed 3.3V output <br>\* wide input range <br>\* stable current for components| \* needs inductor + caps <br>\* layout must be clean |
| ![](2.png)<br>**TPS560430X3FDBVT** <br><br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TPS560430X3FDBVT/9861429) | \* fixed 3.3V output<br>\* simple style <br>\* small footprint | \* needs inductor + caps<br>\* layout needs to reduce noise |
| ![](3.png)<br>**AP63203WU-7**<br><br>[link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP63203WU-7/9858426) | \* fixed 3.3V output<br>\* alot of current <br>\* common part | \* needs inductor + caps<br>\* requires good PCB layout |

**Barrel Jack**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](b1.png)<br>**PJ-006A-SMT-TR (2.1mm)**<br><br> $0.95/each<br>[link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-006A-SMT-TR/408456) | \* standard 2.1mm adapter size<br>\* surface mount<br>\* availability<br>\* rated above 9V | \* tough footprint <br>\* needs strong ground pad support |
| ![](b2.png)<br>**PJ-006B-SMT-TR (2.1mm)**<br><br> $0.95/each<br>[link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-006B-SMT-TR/408457) | \* standard 2.1mm plug<br>\* surface mount<br>\* clean pcb layout | \* small footprint |
| ![](b3.png)<br>**KLDVX-SMT-02-BTR (2.1mm)**<br><br>$1.40/each<br>[link to product](https://www.digikey.com/en/products/detail/kycon-inc/KLDVX-SMT-02-BTR/10247017) | \* Vertical orientation option<br>\* surface mount | \* Larger footprint<br>\* Slightly higher cost |




### I2C (ToF) Sensor

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](sen1.png)<br>**VL53L0CXV0DH/1**<br><br>[link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/VL53L0CXV0DH-1/6023691)| \* widely used ToF sensor<br>\* works directly at 3.3V<br>\* good for 2-6 ft detection | \* Small <br>\* Requires good PCB footprint |
| ![](sen2.png)<br>**VL53L1CXV0FY/1**<br><br>[link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/VL53L1CXV0FY-1/8258055?s=N4IgTCBcDaIGoBkCsBmBBGAwgDTgBgDEBNAenRAF0BfIA)| \* long range capability<br>\* adjustable timing<br>\* 3.3V compatible | \* small <br>\* configuration is complex |
| ![](sen3.png)<br>**TMF8821** <br><br>[link to product](https://www.digikey.com/en/products/detail/ams-osram-usa-inc/TMF8821-1AM/16285681) | \* multi zone detection<br>\* 3.3V compatible<br>\* fits requirements| \* small <br>\* Requires good PCB layout |

### LED Debug Light ###

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](l1.png)<br>**LTST-C150GKT** (Green LED) <br>[link to product](https://www.digikey.com/en/products/detail/liteon/LTST-C150GKT/269216?s=N4IgTCBcDaIDIBUDKCC0BhAjAVgAwHEBpBEAXQF8g)| \* easy to solder <br>\* good for power/status indicator<br>\*low current draw | \* requires series resistor |
| ![](l2.png)<br>**LTST-C150KRKT** (Red LED)<br>[link to product](https://www.digikey.com/en/products/detail/liteon/LTST-C150KRKT/386761?s=N4IgTCBcDaIDIBUDKCC0BhAjAVgAwGkAlfBEAXQF8g)| \* visible error/stop indicator<br>\* low voltage<br>\* easy solder size | \* requires series resistor |
| ![](l3.png)<br>**LTST-C150TBKT** (Blue LED)<br>[link to product](https://www.digikey.com/en/products/detail/liteon/LTST-C150TBKT/388526?s=N4IgTCBcDaIDIBUDKCC0BhAjAVgAwICEBpBEAXQF8g)| \* clean look<br>\* good for activity/comms indicator <br>\* easy to solder | \* slightly higher voltage |

### Microcontroller

Below is my selected microcontroller, for a more detailed explanation please visit the [Microcontroller Selection Page](https://jtharri6.github.io/egr314/03-Microcontroller%20Selection/Microcontoller%20Selection/).

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](pic.png)<br>**PIC18F47K42** <br><br>[link to product](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18(L)F26-27-45-46-47-55-56-57K42-Data-Sheet-40001919G.pdf) | \* PIC used in class <br>\* easy to use <br>\* peripherals for I2C ToF and UART | \* needs good decoupling and 3.3V rail<br>\* PCB layout|


## Final Components Selection

| Main Components Chosen | Purpose | Reason Chosen |
|------------------------|----------|---------------|
| PJ-006A-SMT-TR | 9V power input | standard 2.1mm adapter size, surface mount, and reliable for 9V input |
| TPS560430X3FDBVT | 3.3V voltage regulation | fixed 3.3V output and small footprint for stable power conversion |
| VL53L0CXV0DH/1 | Distance sensing (I2C ToF) | widely used ToF sensor that works directly at 3.3V and fits the 2ft to 6ft detection range |
| LTST-C150KRKT | Debug/status indicator light | visible and low voltage LED that is easy to solder and works well on 3.3V systems |



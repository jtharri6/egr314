---
title: Module's Selected Major Components
---

## Module's Selected Major Components

### Microcontroller

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](pic.png)<br>**PIC18F47K42** <br><br>[link to product](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18(L)F26-27-45-46-47-55-56-57K42-Data-Sheet-40001919G.pdf) | \* PIC used in class <br>\* easy to use <br>\* peripherals for I2C ToF and UART | \* needs good decoupling and 3.3V rail<br>\* PCB layout|

### Power Management

**3.3 V Regulator**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](1.png)<br>**LMR16006YQ3DDCRQ1** <br><br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LMR16006YQ3DDCRQ1/5395814) | \* Fixed 3.3V output <br>\* Wide input range <br>\* stable current for components| \* needs inductor + caps <br>\* layout must be clean |
| ![](2.png)<br>**TPS560430X3FDBVT** <br><br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TPS560430X3FDBVT/9861429) | \* Fixed 3.3V output<br>\* Simple style <br>\* Small footprint | \* needs inductor + caps<br>\* layout needs to reduce noise |
| ![](3.png)<br>**AP63203WU-7**<br><br>[link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP63203WU-7/9858426) | \* Fixed 3.3V output<br>\* Big current headroom <br>\* Common part with good docs | \* needs inductor + caps<br>\* requires good PCB layout |

**Barrel Jack**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](b1.png)<br>**PJ-006A-SMT-TR (2.1mm)**<br><br> $0.95/each<br>[link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-006A-SMT-TR/408456) | \* standard 2.1mm adapter size<br>\* surface mount<br>\* availability<br>\* rated above 9V | \* touch footprint <br>\* needs strong ground pad support |
| ![](b2.png)<br>**PJ-006B-SMT-TR (2.1mm)**<br><br> $0.95/each<br>[link to product](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PJ-006B-SMT-TR/408457) | \* standard 2.1mm plug<br>\* surface mount<br>\* clean pcb layout | \* small footprint |
| ![](b3.png)<br>**KLDVX-SMT-02-BTR (2.1mm)**<br>br> $1.40/each<br>[link to product](https://www.digikey.com/en/products/detail/kycon-inc/KLDVX-SMT-02-BTR/10247017) | \* Vertical orientation option<br>\* Surface mount<br>\* Strong brand (Kycon) | \* Larger footprint<br>\* Slightly higher cost |




### I2C (ToF) Sensor

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](sen1.png)<br>**VL53L0CXV0DH/1**<br><br>[link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/VL53L0CXV0DH-1/6023691)| \* widely used ToF sensor<br>\* works directly at 3.3V<br>\* good for 2-6 ft detection | \* Small <br>\* Requires good PCB footprint |
| ![](sen2.png)<br>**VL53L1CXV0FY/1**<br><br>[link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/VL53L1CXV0FY-1/8258055?s=N4IgTCBcDaIGoBkCsBmBBGAwgDTgBgDEBNAenRAF0BfIA)| \* long range capability<br>\* adjustable timing<br>\* 3.3V compatible | \* small <br>\* configuration is complex |
| ![](sen3.png)<br>**TMF8821** <br><br>[link to product](https://www.digikey.com/en/products/detail/ams-osram-usa-inc/TMF8821-1AM/16285681) | \* multi zone detection<br>\* 3.3V compatible<br>\* fits requirements| \* Small package<br>\* Requires good PCB layout |




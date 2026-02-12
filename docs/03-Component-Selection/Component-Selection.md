---
title: Module's Selected Major Components
---

## Module's Selected Major Components

### Microcontroller

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](pic.png)<br>**PIC18F47K42** <br>$/each<br>[link to product](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18(L)F26-27-45-46-47-55-56-57K42-Data-Sheet-40001919G.pdf) | \* PIC used in class <br>\* easy to use <br>\* peripherals for I2C ToF and UART | \* needs good decoupling and 3.3V rail<br>\* PCB layout|

### Power Management

**3.3 V Regulator**

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](1.png)<br>**LMR16006YQ3DDCRQ1** <br> 4V–40V input <br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LMR16006YQ3DDCRQ1/5395814) | \* Fixed 3.3V output <br>\* Wide input range <br>\* stable current for components| \* needs inductor + caps <br>\* layout must be clean |
| ![](2.png)<br>**TPS560430X3FDBVT** <br>Fixed 3.3V<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TPS560430X3FDBVT/9861429) | \* Fixed 3.3V output<br>\* Simple style <br>\* Small footprint | \* needs inductor + caps<br>\* layout needs to reduce noise |
| ![](3.png)<br>**AP63203WU-7**<br>Fixed 3.3V<br>[link to product](https://www.digikey.com/en/products/detail/diodes-incorporated/AP63203WU-7/9858426) | \* Fixed 3.3V output<br>\* Big current headroom <br>\* Common part with good docs | \* needs inductor + caps<br>\* requires good PCB layout |



### I2C (ToF) Sensor

| **Component** | **Pros** | **Cons** |
|---|---|---|
| ![](sen1.png)<br>**VL53L0CXV0DH/1**<br>Up to 2m range <br>[link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/VL53L0CXV0DH-1/6023691)| \* widely used ToF sensor<br>\* works directly at 3.3V<br>\* good for 2-6 ft detection<br>\* good documentation | \* Small <br>\* Requires good PCB footprint |
| ![](sen2.png)<br>**VL53L1CXV0FY/1**<br>Up to 4m range <br>[link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/VL53L1CXV0FY-1/8258055?s=N4IgTCBcDaIGoBkCsBmBBGAwgDTgBgDEBNAenRAF0BfIA)| \* long range capability<br>\* adjustable timing<br>\* 3.3V compatible | \* small <br>\* configuration is complex |
| ![](sen3.png)<br>**TMF8821** <br> 2m range <br>[link to product](https://www.digikey.com/en/products/detail/ams-osram-usa-inc/TMF8821-1AM/16285681) | \* multi zone detection<br>\* 3.3V compatible<br>\* fits requirements| \* Small package<br>\* Requires good PCB layout |




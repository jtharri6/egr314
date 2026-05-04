---
title: Module Power Budget
---

## Overview

This table summarizes the power requirements for the distance sensing module used in the Team 307s system. It lists the main components in the module and their current consumption on the 3.3 V rail, which is supplied by a switching regulator. Power can be provided through either a 9 V barrel jack or the team’s shared 12 V power system, and a 25% safety margin is included to ensure reliable operation.

![power budget ](power%20budget.png)

## Conclusion

The power budget was used to estimate the total current required by all components on the 3.3 V rail, including the ESP32, distance sensor, and status LEDs. Each component’s maximum current was summed to determine a baseline and a 25% safety margin was added to ensure safety. The results showed that the total current demand remains within the limits of the selected LM2575 switching regulator, leaving available current for safe operation. This confirms that the power design is sufficient and capable of supporting the subsystem without risk of overloading and possible of adding compoments if needed.
---
title: Module's Requirements
---

## Distance Sensor Module Requirements
This module provides distance and range sensing for obstacle detection and reaction time for the amphibious rover system. Using a serial distance sensor and a PIC18F47K42 microcontroller, the module reports distance measurements and obstacle status to the motion control subsystem for safe navigation.

| Requirement Description                     | Measure of Threshold (Minimum)                                   | Target Measure                                      | Stretch Requirement (Y/N) |
|--------------------------------------------|------------------------------------------------------------------|----------------------------------------------------|----------------------------|
| 3.3V power regulator on module              | Provides 3.3V to MCU and sensor                                  | Stable 3.3 V output                                 | N                          |
| Microcontroller type                        | PIC18F47K42 is powered and programmable                          | PIC18F47K42 runs sensor and UART logic reliably     | N                          |
| Microcontroller role                        | PIC processes distance data from sensor                          | PIC handles distance logic and messaging            | N                          |
| Serial distance sensor                      | Sensor communicates using serial interface                       | Sensor provides consistent distance readings        | N                          |
| Distance sensing for obstacle avoidance     | Detects obstacles within 2 ft                                | Reliable stopping or avoidance at 3 ft          | N                          |
| Distance sensing for early warning          | Detects obstacles within 8 ft                               | Early navigation awareness at 12 ft            | Y                          |
| Reaction time support                       | Sensor updates during rover motion                               | Fast response and update rate                       | N                          |
| UART communication to system                | Sends distance and obstacle status                               | Reliable messages to main controller                | N                          |
| Motor                                      | No motor used in this subsystem                                     | N/A                                                | N                          |
| Physical integration                        | Module mounts securely inside rover housing                      | Protected or adjustable sensor mount                | Y                          |
| Testing                                    | Functions in life like conditions                                | Functions near water and splash environments        | Y                          |
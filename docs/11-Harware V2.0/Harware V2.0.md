---
title: Hardware V2.0
---

## Overview

A Version 2.0 of the distance sensing subsystem would focus on improving reliability, ease of debugging, and overall system integration. While the current design meets functional requirements, several small improvements could make the hardware more robust and easier to use.

## Sensor Interface Improvements

The current I2C distance sensor requires a specific orientation to provide accurate readings, which made testing more difficult. In a Version 2.0 design, a different sensor or improved mounting method could be used to reduce sensitivity to alignment. This would improve measurement consistency.

## Debug Indicator Improvements

The current design uses LEDs to indicate system states such as STOP, SLOW, and FAST. In a Version 2.0 design, additional debugging LEDs could be included to show system activity, such as power status and UART communication. For example, one LED could indicate when the board is powered, and another could blink when data is transmitted. 

## Power Input Selection Improvement

The current design allows power from either a 9 V barrel jack or the team’s shared power, but switching between them is not easily controlled. In a Version 2.0 design, jumpers could be added to select the active power source. This would make it easier to safely switch between power inputs and improve usability.

## Removal of Direct Motor Connection

The current design includes a direct connection to the motor subsystem, but it was not used. In a Version 2.0, this connection could be removed to simplify the system and reduce unnecessary wiring and rely on team UART communication.

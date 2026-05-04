---
title: API
---

## Overview

This page describes communication for the distance sensing subsystem within Team 307’s system. The subsystem uses a UART daisy chain protocol through an 8 pin ribbon connector. Messages follow a defined packet structure and are used to transmit obstacle detection data and distance measurements to other subsystems.

## Team UART Packet Format

| Packet Section | Bytes | Description |
|---|---:|---|
| Start Frame | 2 | AZ |
| Sender ID | 1 | ID of transmitting board |
| Receiver ID | 1 | ID of intended board |
| Message Data | 1–58 | Message type and payload |
| End Frame | 2 | YB |

## Team Member IDs

| ID | Subsystem |
|---|---|
| A | OLED HMI |
| D | Hall Effect |
| E | Pressure Sensor |
| G | Motor Control |
| J | Distance Sensor |
| Z | Temperature Sensor |

## Messages Sent

### 1. Obstacle State (Motor Control)

This message is sent to the motor subsystem to control movement behavior.

| Variable Name | Data Type | Possible Values |
|---|---|---|
| obstacle_state | string | FAST, SLOW, STOP |

Example:

```
AZJGSLOWYB
```
Meaning: send SLOW command from J to G.

### 2. Distance Value (HMI Display)

This message is sent to the OLED subsystem to display the measured distance.

| Variable Name | Data Type | Min Value | Max Value | Example |
|---|---|---:|---:|---|
| distance_mm | uint16_t | 0 | 4000 | 750 |

Example:

```
AZJA750YB
```
Meaning: send distance value 750 mm from J to A.

## Messages Received

Messages addressed to J are processed. Messages addressed to other valid team IDs are forwarded through the daisy chain network.

| Sender | Receiver | Action |
|---|---|---|
| Any valid ID | J | Process |
| Any valid ID | Other | Forward |

## Message Handling Rules

1. Process messages addressed to J  
2. Forward messages addressed to other team members  
3. Ignore messages originating from J  
4. Ignore messages exceeding 64 bytes  
5. Ignore messages without valid AZ start or YB end frames  
6. Ignore messages from invalid sender IDs  

## API Functionality

Distance measurements are obtained from the I2C sensor and converted into FAST, SLOW, or STOP states for motor control. At the same time, the measured distance in millimeters is transmitted to the OLED subsystem for display. This enables obstacle avoidance, real feedback, and coordinated communication through UART.
---
title: Reflection
---

## Review of Module’s Success

The distance sensing subsystem successfully measured distance using the I2C sensor and communicated with the team through the UART. It was able to send STOP, SLOW, and FAST states to the motor subsystem and distance values to the HMI, meeting the main system requirements.

Some parts were not completed. MQTT communication was not implemented due to time constraints, and the sensor required a specific orientation to work consistently, which made testing more difficult.

## Microcontroller/Module Startup Tips

- Check the 3.3 V power before turning the board on  
- Test each component separately before combining everything  
- Start with simple code before adding full functionality   
- Make sure UART connections and message format are correct 
- Multimeters are your friend 

## Lessons Learned

One of the biggest things learned from this project was how important it is to solder correctly. A lot of issues came from bad joints or small mistakes that caused shorts, which ended up damaging components or forcing parts to be resoldered. Using a multimeter to check connections and make sure nothing is shorted before powering the board made a big difference.

Another important lesson was to not solder everything at once. It is much better to build and test the system piece by piece, since it makes it easier to find problems early. Checking the schematic and making sure the correct components are used also helps avoid mistakes during assembly.

This project also showed how helpful it is to check in with professors and TAs. Getting feedback early helped catch issues faster and made debugging a lot easier.

## Recommendations for Future Students

- Start early and do not wait to test your hardware, since problems take time to fix and can slow everything down.
- Always double check power connections and use a multimeter to make sure nothing is shorted before turning the board on.
- Build and test your system piece by piece instead of soldering everything at once, so it is easier to find and fix issues.
- Datasheets are your friend, so take time to learn how to read them because they help with wiring, pinouts, and understanding how components actually work.
- Check in with professors and TAs when you get stuck, since they can help catch mistakes early and save a lot of time.
- Order early and get as many duplicate parts as you can incase something goes wrong.
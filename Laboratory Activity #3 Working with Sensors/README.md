# Laboratory Activity #3

## Working with Sensors

### Course
**COSC 111 – Internet of Things**

## Overview
This laboratory activity focuses on using **sensors** to collect environmental data and make decisions based on sensor readings. The activity demonstrates how an Arduino microcontroller reads analog sensor values, processes them, and triggers an output based on defined conditions.


## Objectives
The objectives of this activity are to:
- Understand how analog sensors work
- Read temperature and light intensity using sensors
- Convert raw analog data into meaningful values
- Implement conditional logic based on sensor thresholds
- Control an output device based on sensor input


## Description
In this activity, a **thermistor** and a **photoresistor** are used to measure temperature and light intensity, respectively. The Arduino continuously reads sensor values and compares them against predefined threshold levels.

When both the temperature and brightness exceed their threshold values, an alert output connected to a digital pin is activated. Sensor data is also displayed through the Serial Monitor for real-time monitoring and debugging.

This setup reflects real-world IoT applications where sensors are used to monitor environments and automatically trigger alerts or actions.


## Code Explanation
The program is organized into several functional components:

- **Pin Definitions**  
  Analog pins are assigned to the thermistor and photoresistor, while a digital pin controls the alert output.

- **Sensor Reading Functions**  
  - `readTemperature()` reads the thermistor value and converts it into degrees Celsius using a mathematical formula.
  - `readBrightness()` reads the photoresistor value to determine light intensity.

- **Main Logic (`loop()`)**  
  Sensor values are read, displayed via Serial Monitor, and compared to threshold values. If both conditions are met, the alert output blinks.

Key concepts demonstrated:
- Analog-to-digital conversion
- Sensor calibration and data processing
- Conditional decision-making
- Real-time monitoring using Serial communication


## Hardware Components Used
- Arduino Uno
- Thermistor
- Photoresistor (LDR)
- Resistors
- LED or buzzer (alert output)
- Breadboard
- Jumper wires


## Pin Configuration
| Pin | Component |
|-----|----------|
| A0 | Thermistor |
| A2 | Photoresistor |
| 12 | Alert output |


## Files Included
- Arduino source code (`.ino` file)
- Circuit diagram image (`.jpg`)


## Conclusion
This laboratory activity demonstrates how sensors can be integrated into an Arduino system to monitor environmental conditions and trigger outputs automatically. It provides essential knowledge for building responsive and intelligent IoT applications.

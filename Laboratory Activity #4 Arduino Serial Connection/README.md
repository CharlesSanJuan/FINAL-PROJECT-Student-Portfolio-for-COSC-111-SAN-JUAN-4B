# Laboratory Activity #4

## Arduino Serial Connection

### Course
**COSC 111 – Internet of Things**


## Overview
This laboratory activity demonstrates the use of **serial communication** between an Arduino microcontroller and a computer. It shows how sensor data can be transmitted through the Serial Monitor and how user input from the serial interface can be used to control hardware behavior in real time.


## Objectives
The objectives of this activity are to:
- Understand Arduino serial communication
- Read and interpret analog sensor values
- Convert raw sensor data into meaningful units
- Control output behavior using serial commands
- Apply real-time interaction between hardware and software


## Description
In this activity, a **photoresistor** is used to measure ambient light intensity. The Arduino reads the sensor value, converts it into a percentage, and sends the data to the Serial Monitor.

When the brightness exceeds a defined threshold, an alert output begins blinking automatically. The system can be controlled through the Serial Monitor by sending text commands. Entering the command **“stop”** disables the blinking behavior and turns off the alert output.

This activity highlights how serial communication enables monitoring, debugging, and interactive control in IoT systems.


## Code Explanation
The program performs the following operations:

- **Sensor Reading**  
  Reads the photoresistor value using `analogRead()` and converts it into a percentage using the `map()` function.

- **Serial Output**  
  Displays raw and processed brightness values in the Serial Monitor.

- **Serial Input Handling**  
  Reads user input from the Serial Monitor and processes text commands to control program behavior.

- **Output Control**  
  Activates or stops blinking of the alert output based on sensor conditions and serial commands.

Key concepts demonstrated:
- Serial communication (`Serial.begin`, `Serial.print`)
- Analog signal processing
- Conditional logic
- Interactive hardware control


## Hardware Components Used
- Arduino Uno
- Photoresistor (LDR)
- LED or buzzer (alert output)
- Resistors
- Breadboard
- Jumper wires

## Pin Configuration
| Pin | Component |
|-----|----------|
| A2 | Photoresistor |
| 8  | Alert output |


## Files Included
- Arduino source code (`.ino` file)
- Circuit diagram image (`.jpg`)


## Conclusion
This laboratory activity demonstrates how serial communication can be used to monitor sensor data and control hardware behavior interactively. It reinforces the importance of serial interfaces in debugging, data visualization, and real-time control for IoT applications.

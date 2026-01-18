## LAB MIDTERM EXAM – Light Intensity Monitoring and LED Control
## Arduino Light Sensor With Manual and Automatic Modes
### Course
**COSC 111 – Internet of Things**

## Overview
This midterm laboratory exam focuses on using an Arduino to monitor environmental light intensity through a photoresistor and control multiple LEDs based on predefined thresholds. The system supports both MANUAL and AUTOMATIC modes, allowing dynamic adjustment of LED behavior through serial commands.

The activity demonstrates how sensor data can be interpreted and translated into meaningful system responses, a core concept in IoT applications.

## Objectives
The objectives of this midterm lab exam are to:
- Read and interpret analog sensor data using Arduino
- Convert sensor values into percentage-based measurements
- Control multiple LEDs based on configurable thresholds
- Implement MANUAL and AUTOMATIC operating modes
- Use serial commands to configure system behavior

## Description
In this activity, a photoresistor connected to an analog pin measures light intensity from the environment. The measured value is converted into a percentage and used to determine which LED (Green, Yellow, or Red) should be activated.

The system operates in two modes:
- **MANUAL Mode**: Allows the user to adjust LED thresholds using serial commands.
- **AUTOMATIC Mode**: Uses default threshold values and displays environmental conditions based on light intensity.

The Arduino continuously reports system status through the Serial Monitor, providing real-time feedback.

## Code Explanation
### Arduino Code (`lab_midterm_exam.ino`)
- Reads analog input from a photoresistor.
- Maps sensor readings to a 0–100% brightness scale.
- Activates LEDs based on configurable threshold values.
- Supports mode switching through serial commands.
- Implements serial command parsing and validation.
- Displays real-time system status and environment interpretation.

Key concepts demonstrated:
- Analog sensor reading
- Data mapping and threshold logic
- Digital output control
- Serial communication and command handling
- State-based system behavior

## Serial Commands
- `MODE MANUAL` – Switches the system to manual mode.
- `MODE AUTO` – Switches the system to automatic mode and resets thresholds.
- `SET LOW <value>` – Updates the GREEN LED threshold (0–100).
- `SET HIGH <value>` – Updates the RED LED threshold (0–100).

Invalid commands are rejected to ensure system stability.

## Hardware Components Used
- Arduino Uno (or compatible board)
- Photoresistor (LDR)
- Red LED
- Yellow LED
- Green LED
- Resistors
- Breadboard
- Jumper wires
- USB cable

## Conclusion
This midterm laboratory exam demonstrates effective use of sensors, serial communication, and conditional logic to create a responsive Arduino-based system. The activity reinforces essential IoT concepts such as environmental sensing, system modes, and real-time monitoring, forming a strong foundation for more advanced embedded and IoT applications.

# Laboratory Activity #6

## Bidirectional Control Using Arduino and Python

### Course
**COSC 111 – Internet of Things**


## Overview
This laboratory activity demonstrates **bidirectional serial communication** between an Arduino microcontroller and a Python application. Both the Arduino and the Python program are capable of sending and receiving data, allowing real-time interaction between hardware inputs and software control.

This activity reflects real-world IoT systems where devices both **transmit sensor or input data** and **receive control commands** from external applications.


## Objectives
The objectives of this activity are to:
- Understand bidirectional serial communication
- Send data from Arduino to Python
- Send control commands from Python to Arduino
- Control LEDs using both hardware buttons and software input
- Implement real-time hardware–software interaction


## Description
In this activity, three **push buttons** are connected to the Arduino. When a button is pressed, the Arduino sends a corresponding character (`R`, `G`, or `B`) to the Python program through the serial connection.

The Python program listens for these messages and responds by sending commands (`1`, `2`, or `3`) back to the Arduino. Upon receiving these commands, the Arduino toggles the state of the corresponding **RGB LED**.

Additionally, the Python program allows the user to manually send commands through keyboard input, enabling LED control without pressing the physical buttons. This demonstrates true two-way communication between hardware and software.


## Code Structure and Explanation

### 1. `bicon.ino` (Arduino Program)
- Configures LED pins as outputs and button pins as inputs
- Detects button press events using state change detection
- Sends button identifiers (`R`, `G`, `B`) to Python via Serial
- Receives commands (`1`, `2`, `3`) from Python
- Toggles the corresponding LED based on received commands

Key concepts demonstrated:
- Serial read and write operations
- Button debouncing using state tracking
- Real-time LED control


### 2. `bicon.py` (Python Program)
- Establishes a serial connection with Arduino
- Continuously listens for messages from Arduino using a separate thread
- Sends control commands back to Arduino based on received messages
- Allows manual LED control via keyboard input

Key concepts demonstrated:
- Multithreading for non-blocking serial communication
- Hardware–software synchronization
- Real-time command handling


## Hardware Components Used
- Arduino Uno
- RGB LED
- Push buttons (3)
- Resistors
- Breadboard
- Jumper wires
- Computer with Python installed

## Pin Configuration

### LEDs
| Pin | LED |
|-----|-----|
| 7 | Red |
| 6 | Green |
| 5 | Blue |

### Buttons
| Pin | Button |
|-----|--------|
| 12 | Button 1 |
| 11 | Button 2 |
| 10 | Button 3 |


## Files Included
- `bicon.ino` – Arduino bidirectional control program
- `bicon.py` – Python serial communication program


## Conclusion
This laboratory activity successfully demonstrates bidirectional serial communication between Arduino and Python. By allowing both hardware inputs and software commands to control LEDs, the activity highlights essential IoT principles such as real-time interaction, feedback systems, and device interoperability.

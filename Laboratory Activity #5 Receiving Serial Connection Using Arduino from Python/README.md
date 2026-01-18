# Laboratory Activity #5

## Receiving Serial Connection Using Arduino from Python

### Course
**COSC 111 – Internet of Things**


## Overview
This laboratory activity demonstrates **serial communication between an Arduino microcontroller and a Python application**. It shows how external software can send commands to Arduino through a serial connection and control hardware components in real time.

This activity highlights **cross-platform communication**, a fundamental concept in Internet of Things (IoT) systems where microcontrollers interact with computers, servers, or applications.

## Objectives
The objectives of this activity are to:
- Understand serial communication between Arduino and Python
- Receive and process serial commands on Arduino
- Control multiple output devices using software input
- Implement modular programming using header files
- Apply bidirectional communication principles


## Description
In this activity, an **RGB LED** is controlled using commands sent from a **Python program** to the Arduino via a serial connection. The Python program provides a text-based menu that allows the user to toggle individual LED colors or control all LEDs at once.

The Arduino receives single-character commands through the Serial port and performs corresponding actions, such as turning LEDs ON, OFF, or toggling their states. Feedback messages are sent back to the Python program to confirm the executed command.

This setup simulates real-world IoT scenarios where microcontrollers receive control commands from external applications.

## Code Structure and Explanation

### 1. `led_control.h`
This header file contains:
- Pin assignments for the RGB LED
- State variables for each LED color
- Functions to toggle individual LEDs
- Functions to turn all LEDs ON or OFF

Using a header file improves code organization and reusability.

### 2. `serial_led_control.ino`
This Arduino sketch:
- Initializes serial communication
- Calls LED setup functions
- Listens for incoming serial commands
- Executes LED control functions based on received input
- Sends status messages back through the Serial port

Supported commands:
| Command | Action |
|-------|--------|
| `r` | Toggle Red LED |
| `g` | Toggle Green LED |
| `b` | Toggle Blue LED |
| `a` | Turn all LEDs ON |
| `o` | Turn all LEDs OFF |
| `x` | Exit / Turn all LEDs OFF |


### 3. `serial_led_control.py`
This Python program:
- Establishes a serial connection with Arduino
- Displays a menu for user interaction
- Sends command characters to Arduino
- Reads and displays Arduino responses
- Allows real-time control through keyboard input

The program demonstrates how software applications can directly interact with embedded hardware.


## Hardware Components Used
- Arduino Uno
- RGB LED
- Resistors
- Breadboard
- Jumper wires
- Computer with Python installed


## Pin Configuration
| Pin | Component |
|-----|----------|
| 8  | Red LED |
| 9  | Green LED |
| 10 | Blue LED |


## Files Included
- `serial_led_control.ino` – Arduino main program
- `led_control.h` – LED control functions
- `serial_led_control.py` – Python serial control program

## Conclusion
This laboratory activity demonstrates successful serial communication between Arduino and Python for hardware control. It reinforces key IoT concepts such as software-to-hardware interaction, modular programming, and real-time command execution, which are essential in modern embedded and IoT systems.

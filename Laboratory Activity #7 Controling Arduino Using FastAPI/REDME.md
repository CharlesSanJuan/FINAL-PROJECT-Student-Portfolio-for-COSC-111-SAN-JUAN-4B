## Laboratory Activity #7 – Controlling Arduino Using FastAPI
## Controlling Arduino Using FastAPI
### Course
**COSC 111 – Internet of Things**

## Overview
This laboratory activity focuses on integrating an Arduino microcontroller with a FastAPI backend to enable hardware control through a web-based interface. The activity demonstrates how digital outputs on an Arduino can be controlled using physical inputs, serial communication, and RESTful API endpoints.

## Objectives
The objectives of this activity are to:
- Understand serial communication between Arduino and a computer  
- Control digital outputs using physical buttons and software commands  
- Integrate Arduino with a FastAPI server  
- Apply basic REST API concepts in an IoT context  

## Description
In this activity, an Arduino is programmed to control three LEDs (Red, Green, and Blue). The LEDs can be toggled using physical push buttons connected to the Arduino or through serial commands sent by a FastAPI application.

The FastAPI server acts as a bridge between the user and the Arduino hardware. By sending HTTP requests to specific API endpoints, users can turn LEDs ON, turn LEDs OFF, or toggle them individually. This setup demonstrates a simple but practical example of remote hardware control using web technologies.

## Code Explanation
### Arduino Code (`arduino_fastAPI.ino`)
- `setup()` initializes serial communication, configures LED pins as OUTPUT, and button pins as INPUT_PULLUP.
- `loop()` continuously checks for button presses and toggles the corresponding LED.
- The Arduino listens for single-character serial commands sent over the Serial Monitor or FastAPI.
- Invalid or multi-character inputs are rejected to prevent incorrect commands.

Key concepts demonstrated:
- Digital input and output control  
- Button debouncing using delay  
- Serial communication and command parsing  

### FastAPI Code (`arduino_fastAPI.py`)
- Establishes a serial connection between the computer and the Arduino.
- Defines REST API endpoints to control LED states.
- Uses a helper function to send single-character commands to the Arduino.

Key concepts demonstrated:
- RESTful API design  
- Hardware control using Python  
- Serial communication from a backend service  

## Hardware Components Used
- Arduino Uno (or compatible board)
- Red, Green, and Blue LEDs
- Push buttons
- Resistors
- Breadboard
- Jumper wires
- USB cable

## Files Included
- `arduino_fastAPI.ino`
- `arduino_fastAPI.py`
- `README.md`

## Conclusion
This activity demonstrates how Arduino hardware can be controlled through a FastAPI-based web service. It provides hands-on experience in combining embedded systems with web technologies and serves as a foundation for more advanced IoT and smart device applications.

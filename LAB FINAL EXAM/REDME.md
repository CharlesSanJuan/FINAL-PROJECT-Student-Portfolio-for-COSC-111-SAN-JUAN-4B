## LAB FINAL EXAM – Arduino Group Control Using FastAPI
## Arduino Serial Client and Group-Based LED Control
### Course
**COSC 111 – Internet of Things**

## Overview
This final laboratory exam demonstrates a complete IoT workflow using Arduino, Python, serial communication, and a FastAPI backend. The activity shows how a physical button press on an Arduino can trigger a web API request that controls a group of devices or LEDs remotely.

The system highlights real-world IoT concepts such as event-driven communication, client-server architecture, and hardware-to-software integration.

## Objectives
The objectives of this final lab exam are to:
- Implement reliable button input using debouncing
- Transmit data from Arduino to a computer via serial communication
- Develop a Python client that interacts with a FastAPI server
- Control devices using group-based API endpoints
- Apply IoT concepts in a full end-to-end system

## Description
In this activity, an Arduino is configured with a push button assigned to a specific group number. When the button is pressed, the Arduino sends the group number through the serial port.

A Python client listens for incoming serial data from the Arduino. Once a valid group number is received, the client sends an HTTP request to a FastAPI server endpoint responsible for toggling the LED state of that specific group.

This setup simulates a distributed IoT system where physical actions trigger network-based control logic.

## Code Explanation
### Arduino Code (`finallab.ino`)
- Configures a push button using `INPUT_PULLUP`.
- Implements software debouncing to ensure reliable button detection.
- Sends a predefined group number to the serial port when the button is pressed.
- Uses serial communication to notify the Python client of button events.

Key concepts demonstrated:
- Digital input handling
- Button debouncing
- Serial data transmission
- Event-based signaling

### Python Client Code (`finalLab.py`)
- Establishes a serial connection to the Arduino.
- Continuously listens for incoming serial data.
- Validates received data to ensure it is numeric.
- Sends an HTTP GET request to the FastAPI server using the group number.
- Displays API response status for monitoring and debugging.

Key concepts demonstrated:
- Serial communication using Python
- REST API consumption
- Client-server interaction
- Error handling and validation

## Hardware Components Used
- Arduino Uno (or compatible board)
- Push button
- Resistor
- Breadboard
- Jumper wires
- USB cable

## Software and Libraries Used
- Python
- FastAPI (server-side)
- PySerial
- Requests library


## Conclusion
This final laboratory exam demonstrates a complete IoT solution that integrates hardware input, serial communication, Python-based clients, and web APIs. It reflects real-world IoT system behavior where physical interactions trigger networked actions, reinforcing key concepts in embedded systems and Internet of Things development.

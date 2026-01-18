# Laboratory Activity #2

## Working with Analog Signals

### Course
**COSC 111 – Internet of Things**

## Overview
This laboratory activity introduces the concept of **analog signal behavior** through timing-based control using an Arduino microcontroller. While the outputs are digital, the activity demonstrates how varying time and sequencing can simulate gradual or step-based signal behavior commonly associated with analog systems.

## Objectives
The objectives of this activity are to:
- Understand the difference between digital and analog signals
- Observe how timing can affect output behavior
- Control multiple LEDs using sequential logic
- Apply Arduino programming concepts relevant to analog signal simulation


## Description
In this activity, an Arduino is programmed to control multiple LEDs connected to digital output pins. Each LED turns ON and OFF sequentially with a fixed delay, creating a visible pattern that represents controlled signal transitions over time.

Although the LEDs operate using digital states (**HIGH** and **LOW**), the timing between transitions demonstrates how analog-like behavior can be represented through step-based output control. This concept is important in IoT systems where sensors and actuators often rely on timed or variable signal changes.


## Code Explanation
The Arduino program consists of two main functions:

- `setup()`  
  Initializes digital pins 8 to 12 as OUTPUT pins.

- `loop()`  
  Turns the LEDs ON one by one with a delay, then turns them OFF in the same sequence. The delay controls the timing between each signal change.

Key concepts demonstrated:
- Output pin configuration
- Signal sequencing
- Timing-based control using `delay()`
- Step-based signal behavior related to analog concepts


## Hardware Components Used
- Arduino Uno
- LEDs
- Resistors
- Breadboard
- Jumper wires


## Files Included
- Arduino source code (`.ino` file)
- Circuit diagram image (`.jpg`)


## Conclusion
This laboratory activity demonstrates how timing and sequencing can be used to represent analog signal concepts using digital outputs. It reinforces the relationship between digital control and analog behavior, which is essential for understanding sensor readings and actuator control in IoT applications.

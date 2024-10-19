# Arduino-Based Robotic Assistive Arm

## Overview

This project implements a robotic assistive arm using an Arduino and a motor shield. The arm can be controlled using push buttons and is equipped with a Force Sensing Resistor (FSR) to detect pressure. The arm consists of a stepper motor that moves the arm forwards and backwards, and a DC motor that can perform additional functions based on button presses.

## Components Used

- Arduino board (in this case, I chose to use the Arduino Uno)
- Motor Shield (Version 1)
- Stepper motor (2038 steps per revolution)
- DC motor
- Force Sensing Resistor (FSR)
- Push buttons (3)
- Connecting/Jumper wires
- Breadboard

## Circuit Diagram

![Circuit Diagram](path/to/your/circuit_diagram.png) <!-- Replace with the path to your diagram -->

## Code Explanation

The main components of the code are:

- **Libraries**: The code includes the AFMotor library to control the motors.
  
- **Pin Definitions**: Analog pins for the FSR and push buttons are defined at the beginning of the code.

- **Motor Initialization**: A stepper motor and a DC motor are initialized with their respective pins.

- **Setup Function**: Initializes serial communication, sets pin modes, and defines motor speeds.

- **Loop Function**: Contains the main logic to control the motors based on button presses and FSR readings.

### Key Features

- **Stepper Motor Control**: 
  - The stepper motor moves forwards when button 1 is pressed until the FSR detects pressure.
  - When enough pressure is detected, the stepper stops and prepares to move backward when button 1 is pressed again.

- **DC Motor Control**: 
  - The DC motor moves forwards or backwards based on button presses 2 and 3, respectively.
  
- **Pressure Detection**: 
  - The FSR provides real-time feedback to determine when the stepper motor should stop moving.

## Installation

1. **Hardware Setup**: Connect the motors, FSR, and push buttons to the Arduino according to the provided circuit diagram.

2. **Software Setup**:
   - Install the [AFMotor library](https://github.com/adafruit/AFMotor) in your Arduino IDE.
   - Copy the code provided above into the Arduino IDE.
   - Upload the code to your Arduino board.

## Usage

- Press **Button 1** to move the stepper motor forwards.
- When the FSR detects pressure, the stepper motor will stop.
- Press **Button 1** again to move the stepper motor backwards.
- Press **Button 2** to move the DC motor forwards.
- Press **Button 3** to move the DC motor backwards.

## Notes

- Ensure that the motors are rated for the power supplied by the motor shield.
- Adjust motor speeds as necessary for smooth operation.


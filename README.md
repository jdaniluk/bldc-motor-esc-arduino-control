# bldc-motor-esc-arduino-control
Arduino-based brushless DC motor control project using ESC calibration, PWM throttle control, and drone motor testing.
# BLDC Motor and ESC Control with Arduino

## Overview
This project demonstrates brushless DC (BLDC) motor control using an Arduino, electronic speed controllers (ESCs), PWM throttle signals, and drone motor hardware. The project focused on understanding how BLDC motors operate, how ESC calibration works, and how a microcontroller can generate the control signals needed to drive drone-grade brushless motors.

## Demo Video
YouTube demo: https://youtu.be/MRJz46-yLXg?si=deSyqKNJrO5m1BNs

## Final Report
- `BLDC_Motor_ESC_Arduino_Control_Report.pdf`

## Project Goal
The goal of this project was to build and demonstrate a practical BLDC motor control setup using low-cost hardware. The system was used to test motor response, ESC calibration, throttle mapping, and basic drone motor operation.

## Hardware Used
- Arduino Uno
- Arduino Nano
- DJI 2212 920KV brushless motors
- C1606 brushless motors
- 30A ESCs
- 4-in-1 ESC module
- 3S 11.1V LiPo battery
- 10 kΩ potentiometer
- Breadboard and jumper wires
- Drone frame and motor hardware

## Control Method
The Arduino generated PWM-style servo control signals for the ESC. The ESC interpreted the control signal and electronically commutated the three-phase BLDC motor. A potentiometer was used as a throttle input, allowing the motor speed command to be adjusted manually.

The basic control path was:

1. Potentiometer input is read by the Arduino.
2. The analog value is mapped to a throttle command.
3. The Arduino sends the command to the ESC.
4. The ESC drives the BLDC motor phases.
5. Motor speed changes based on throttle input.

## ESC Calibration
A major part of the project was calibrating the ESC throttle range. The ESC had to learn the maximum and minimum throttle signal values before responding correctly. This required careful startup sequencing, throttle positioning, and repeated testing.

## Engineering Work Demonstrated
- BLDC motor theory
- ESC calibration
- Arduino PWM signal generation
- Potentiometer-based throttle control
- Electrical wiring and power setup
- Drone motor testing
- Troubleshooting inconsistent motor response
- Comparing individual ESCs with a 4-in-1 ESC module
- Embedded control fundamentals

## Results
The final setup successfully demonstrated Arduino-based BLDC motor control. After troubleshooting signal timing, ESC calibration, and wiring issues, the motors responded to throttle input and produced consistent motor spin.

The project showed that an Arduino can interface with ESCs and provide the basic signal pathway needed for drone-style motor control.

## Challenges
- ESC calibration timing was sensitive
- Early throttle mapping was inconsistent
- Individual ESC wiring was more difficult to manage
- Motor response depended heavily on correct power sequencing
- Open-loop control limited precise speed regulation
- The 4-in-1 ESC setup was more stable than the earlier individual ESC setup

## Future Improvements
- Add IMU feedback using an MPU-6050
- Implement closed-loop stabilization
- Build a basic flight controller
- Add wireless control
- Improve wiring and power distribution
- Test multi-motor synchronization
- Develop toward a custom drone platform

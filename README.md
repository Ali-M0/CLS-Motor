# CLS-Motor: A compact solution for stepper motors
<br>
<br>

<img width="816" height="774" alt="Screenshot 2025-07-10 at 8 18 01 PM" src="https://github.com/user-attachments/assets/3adc6257-9fb7-45ce-b775-6831fe6973de" />

<br>
<br>


  ![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)        ![Open Source: Yes](https://img.shields.io/badge/Open%20Source-%E2%9D%A4-green.svg)


<br>
Why not improve the capabilities of an already abundant and capable motor rather than create an environment where people are forced in buying an expensive motor and control system to enter the developing field of robotics, therefore lowering the barrier of entry.
<br>
YouTube Video Demo and Guide: 
<br>

## Key Features

<br>
- Real-time closed-loop correction using MT6816 magnetic encoder
<br>
- **Communication via CAN bus:** By utilizing a CAN bus communication protocol, you inherently gain several benefits to your system, the main benefits being a robust communication protocol that was made with low EMI in mind, along with a more accurate system that decreases the amount of wires needed and scalability with other CLS-Motor systems.
<br>
- **6-layer custom PCB:** Designed in KiCad for signal integrity and thermal performance
<br>
- **Onboard STM32F103CBT6:** Handles encoder data and CAN communication
<br>
- Power regulation via LP2992AIM5-3.3 linear regulator
<br>
- Fully custom C++ to come (CLion environment)

<br>
<br>

## Motivation
In robotic systems—especially robotic arms—accuracy and reliability are critical. While working on my own robotic arm project, I noticed that traditional open-loop stepper motors often missed steps under load, compromising precision.
<br>
<br>
To solve this, I developed the Closed-Loop Stepper (CLS) Motor system—an integrated hardware/software solution that enables real-time position correction through encoder feedback and control logic.
<br>
<br>
<br>


NEW UPDATES COMING SOON
<br>

># Correction Software for CLS Motor
>
><br>
><br>
>
> Explanation about my STM32 programming coming soon with demo and visuals.
> <br>
> Implementation of a diagnostic serial output to aid in tuning and debugging the control loop in real-world conditions.
> <br>
> Custom C++ software using a PID control system and FOC controller to detect missing steps, sending signals to then correct the lost steps
> <br>
>




<br>
<br>
<br>
<br>


## Technical Specifications/Overview

<br>

A closed-loop control system designed to stack with stepper motors and provide real-time feedback using a magnetic encoder. It detects missed steps and corrects them using an onboard STM32 microcontroller while also supplying your communication line through the CAN bus ports to your main microcontroller.

  
  <br>

In the field of robotics, precision and reliability in motor control are essential. During the development of my robotic arm project, I identified the limitations of traditional open-loop stepper systems, particularly their inability to self-correct under load. To address this, I designed and implemented a closed-loop stepper motor driver, combining custom hardware and software to enable real-time position correction.

  
  <br>

This project involved designing a 6-layer PCB in KiCad, optimized for signal integrity and thermal performance. At its core is an STM32F103CBT6 microcontroller, chosen for its surprisingly high processing speed, rich I/O capabilities, and the fact that its only main purpose is to power the encoder and CAN transceiver, along with any other I/O necessary within the board. I integrated an MT6816 magnetic rotary encoder on the rear shaft of a NEMA 17 stepper motor to provide high-resolution feedback, enabling the system to compare target and actual positions. Through custom correction software written in C++ using CLion, the CLS system adjusts its actuation based on the previous and current step resolution. The CLS motor system also integrates an SN65HVD232 CAN transceiver that, on the surface, enables communication between the main CAN controller located on the main MCU, that being a Teensy 4.1, and the CAN bus ports, supplying my system with its communication signal.

  
  <br>

You also may be wondering how my system is powered. That's done through a cascade power system that cascades through a daisy chain design and supplies power to all motors using the CLS motor system, being ultimately powered by a +5V power supply that's soldered to the PCB's positive and negative solder pads added to the top and bottom of the board. The system regulates the +5V power supply to a +3.3V output rail through an LP2992AIM5-3.3 linear regulator, and this then provides power to all the necessary components within my system.






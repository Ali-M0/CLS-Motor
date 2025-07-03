# CLS-Motor: A compact solution for stepper motors
<br>
<br>

//Insert Photo

<br>
<br>


  ![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)        ![Open Source: Yes](https://img.shields.io/badge/Open%20Source-%E2%9D%A4-green.svg)


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
>Explination about my STM32 programming comming soon with demo and visuals.
><br>
>I implemented diagnostic serial output to aid in tuning and debugging the control loop in real-world conditions.
><br>
>C++ software using a PID control system to correct for detect missing steps, sending signal to then correct the lost steps
><br>
>




<br>
<br>
<br>
<br>




* A closed-loop control system designed to stack with stepper motors and provide real-time feedback using a magnetic encoder. It detects missed steps and corrects them using an onboard STM32 microcontroller while also supplying your communication line through the CAN bus ports to your main microcontroller.

* In the field of robotics, precision and reliability in motor control are essential. During the development of my robotic arm project, I identified the limitations of traditional open-loop stepper systems, particularly their inability to self-correct under load. To address this, I designed and implemented a closed-loop stepper motor driver, combining custom hardware and software to enable real-time position correction.

* This project involved designing a 6-layer PCB in KiCad, optimized for signal integrity and thermal performance. At its core is an STM32F103CBT6 microcontroller, chosen for its surprisingly high processing speed, rich I/O capabilities, and the fact that its only main purpose is to power the encoder and CAN transceiver, along with any other I/O necessary within the board. I integrated an MT6816 magnetic rotary encoder on the rear shaft of a NEMA 17 stepper motor to provide high-resolution feedback, enabling the system to compare target and actual positions. Through custom correction software written in C++ using CLion, the motor adjusts its actuation based on the current step resolution.

* The system is powered through a cascade power architecture that distributes power via a daisy chain design.




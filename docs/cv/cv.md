---
template: "cv.html"
icon: lucide/contact
title: "CV"
hide:
  - toc
---


## Summary

-----------

Electrical engineer with experience in embedded systems and power converter control.

You can reach out to me via [LinkedIn](https://www.linkedin.com/in/mtl-guerreiro/).

-----------

## Education

-----------

### Dr.-Ing. (Doctor of Engineering) <span class="cv-date">08/2020 - current</span>
*RPTU Kaiserslautern-Landau, Kaiserslautern, Germany*

- Proposed a grid-forming control strategy for the boost, Ćuk, and SEPIC converters. The strategy uses feedback linearization and model predictive control to regulate the energy of these converters and provide the grid-forming behavior, while accounting for duty cycle and input current constraints.
- Designed and implemented a real-time controller based on the Zynq-7000 SoC, using one core of the processor to serve a TCP-based command-line interface, the second core to run real-time control algorithms, and the FPGA to interface with power converters by generating PWM signals and reading ADCs
- Created Python-based tools to parametrize and fetch data from networked real-time controllers for debugging, operation and automation purposes
- Built several prototypes for research and teaching, including a minimal 700 V dc grid for experiments with supercapacitors, a [four-switch buck-boost converter](prototypes.md#fsbb), and an [isolated Ćuk converter](prototypes.md#cuk)
- Supervised 7 master theses and 5 bachelor theses
- Published 7 research papers and attended 5 international conferences

### Master of Science in Electrical Engineering <span class="cv-date">09/2018 - 08/2020</span>
*Federal University of Technology - Paraná, Pato Branco, PR, Brazil*

- Thesis: Implementation of frequency-domain algorithms for ultrasonic imaging based on interpolation-free Stolt migration
- Implemented and optimized time-domain and frequency-domain algorithms for ultrasonic imaging with Python

### Undegraduate Exchange Student in Electrical Engineering <span class="cv-date">08/2015 - 05/2016</span>
*The University of Vermont, Burlington, VT, USA*

- Designed and prototyped a device for monitoring ICU patients as final project.

### Bachelor of Science in Electrical Engineering <span class="cv-date">11/2012 - 09/2018</span>
*Federal University of Technology - Paraná, Pato Branco, PR, Brazil*

- Thesis: A comparative study and analysis between the compressed sensing and undersampling techniques
- Physics teaching assistant (10/2014 - 05/2015)
- Physics research assistant (10/2013 - 04/2015)
    - Simulation of tapered fiber optics to detect water quality
- Tutored workshops
    - Introduction to Matlab (4h, 09/2017) 
    - Introduciton to Python (4h, 09/2018)


### Electronics technician <span class="cv-date">02/2009 - 12/2011</span>
*Technical School of Electronics (ETEL), Ipaussu, SP, Brazil*

-----------

## Work experience

-----------

### Developer at Tree (Startup) <span class="cv-date">10/2016 - 07/2020</span>
*Pato Branco, PR, Brazil*

- Project hosted by the business incubator at the Federal University of Technology - Paraná to develop a smart irrigation automation system based on soil moisture measurements
- Co-authored two successful grant proposals, obtaining funding for the research and development of the smart irrigation system
- Wrote the firmware for an irrigation controller with sectoring capabilities and moisture parametrization using C and FreeRTOS
- Designed and prototyped a wired capacitive soil moisture sensor
- Supervised the development of a wireless capacitive soil moisture sensor using LoRa for data transmission

### Developer at Xpert Automation Technology <span class="cv-date">11/2017 - 09/2018</span>
*Pato Branco, PR, Brazil*

- Analyzed, simulated and prototyped analog circuits for magnetostrictive sensors for fuel gauging
- Wrote firmware in C to interface NXP microcontrollers to time-of-flight ICs

### Research assistant at the University of Vermont <span class="cv-date">05/2016 - 07/2016</span>
*Burlington, VT, USA*

- 10-week summer internship at the Dunlop Lab
- Prototyped a platform for holding test tubes and exposing them to controlled LED illumination for optogenetics experiments
- Cultured bacteria and conducted optogenetics experiments

### Teaching assistant at National Service of Industrial Training <span class="cv-date"> <span>07/2013 - 12/2013</span> <span>02/2015 - 06/2015</span></span>
*Pato Branco, PR, Brazil*

- Lectured on digital electronics and microcontrollers with C programming
- Supervised students' final projects

### Developer at Chiptronic Automotive Technology <span class="cv-date">02/2012 - 11/2012</span>
*Piraju, SP, Brazil*

- Wrote firmware in Assembly to interface PIC microcontrollers to RFID key fobs and flash memories, including seed-key codification

-----------

## Projects

-----------

### [OPiL](https://gitlab.rhrk.uni-kl.de/lrs/opil) — an Open Processor-in-the-Loop framework

- OPiL is a framework that enables Processor-in-the-Loop testing independent of the simulation platform and the real-time target
- Its main use is to allow the development and validation of complex controllers (e.g., model predictive controllers) in a closed-loop environment


### [OCP](https://github.com/mtguerreiro/ocp) — the Open Controller Project 

- OCP is a framework for automating tests of embedded controllers
- It contains a C library for the real-time target that manages the selection and parametrization of controllers, a scope functionality to store measurements and internal signals during transients, and runs a TCP server to provide an external interface
- It contains a Python module to interface with the real-time target in order to write and read parameters, making it possible to automate testing


### [pyctl](https://github.com/mtguerreiro/pyctl) — A Python package for predictive control

- A python package to simulate linear model predictive control of discrete-time systems
- Capable of C code generation with the option to use a custom QP solver or OSQP
- Contains control design functions for some dc-dc converter topologies

-----------

## List of selected publications

-----------

- M. Guerreiro, S. Kharade, P. Santos and S. Liu, "*Power Electronics Control with System-on-a-Chip-Based Platforms*," 2022 IEEE 20th International Power Electronics and Motion Control Conference (PEMC), Brasov, Romania, 2022, pp. 353-359, doi: 10.1109/PEMC51159.2022.9962949.

- M. Guerreiro, W. Becker, P. Santos and S. Liu, "*An Open Processor-in-the-Loop Framework for Power Converter Control*," IECON 2023- 49th Annual Conference of the IEEE Industrial Electronics Society, Singapore, Singapore, 2023, pp. 1-6, doi: 10.1109/IECON51785.2023.10312423.

- M. Guerreiro, P. Santos and S. Liu, "*Voltage Control of the Ćuk Converter for Grid-Forming in DC Grids: An Energy-Based Approach*," in IEEE Journal of Emerging and Selected Topics in Industrial Electronics, vol. 5, no. 4, pp. 1388-1395, Oct. 2024, doi: 10.1109/JESTIE.2024.3425518.

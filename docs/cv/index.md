---
template: "cv.html"
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

### Doctoral student <span class="cv-date">08/2020 - current</span>
*RPTU University Kaiserslautern-Landau, Kaiserslautern, Germany*

In my research, I proposed a different approach to grid-forming control of power converters. At a fundamental level, grid-forming is about power balancing. So instead of approaching grid-forming as a voltage control problem (the usual approach), I looked at approaching it as an energy regulation problem. It turns out that controlling the energy of some nonlinear nonminimum phase dc-dc converters is much simpler than controlling their voltage. During my research, I also:

- Investigated real-time implementation of model predictive controllers on the Zynq-7020 SoC using hardware and software co-design
- Designed and implemented a real-time control framework for the Zynq-7020 SoC, using one core for real-time control, one core for interfacing, and the FPGA for signal generation and acquisition
- Created Python-based tools to parametrize and fetch data from networked real-time controllers for debugging, operation and automation purposes
- Built several prototypes for research and teaching, including a minimal 700 V dc grid for experiments with supercapacitors, a 700 V boost converter, a four-switch buck-boost converter, and an isolated Ćuk converter
- Supervised 7 master theses and 5 bachelor theses
- Published 8 research papers and attended 5 international conferences

### Master of Science in Electrical Engineering <span class="cv-date">09/2018 - 08/2020</span>
*Federal University of Technology - Paraná, Pato Branco, PR, Brazil*

During my master's, I worked with ultrasonic imaging for nondestructive testing (NDT). I investigated frequency-domain algorithms for ultrasonic data processing, and my thesis focused on adapting an algorithm from synthetic aperture radar to ultrasonic imaging. During this time, I also:

- Implemented classic time and frequency-domain ultrasonic imaging algorithms in Python
- Used CIVA to simulate NDT using full-matrix capture and plane-wave imaging techniques


### Undegraduate Exchange Student in Electrical Engineering <span class="cv-date">08/2015 - 05/2016</span>
*The University of Vermont, Burlington, VT, USA*

During my undergraduate studies I spent two semesters as an exchange student at UVM. I had the opportunity to take courses in power electronics, power systems, and synthetic biology. I also:

- Took the two-semester capstone design project where I worked with the UVM College of Medicine to design and prototype a device to monitor ICU patients

### Bachelor of Science in Electrical Engineering <span class="cv-date">11/2012 - 09/2018</span>
*Federal University of Technology - Paraná, Pato Branco, PR, Brazil*

I did my bachelor's in electrical engineering with a focus on embedded systems. In my thesis, I compared compressed sensing and undersampling for digital signal reconstruction. Other activities I did during my undegraduate studies were:

- Physics teaching assistant (10/2014 - 05/2015)
- Physics research assistant (10/2013 - 04/2015)
    - Simulation of tapered fiber optics to detect water quality
- Tutored workshops for undegraduate students
    - Introduction to Matlab (4h, 09/2017) 
    - Introduction to Python (4h, 09/2018)


### Electronics technician <span class="cv-date">02/2009 - 12/2011</span>
*Technical School of Electronics (ETEL), Ipaussu, SP, Brazil*

During high school, I also earned a qualification as an electronics technician.

-----------

## Work experience

-----------

### Developer at Tree (Startup) <span class="cv-date">10/2016 - 07/2020</span>
*Pato Branco, PR, Brazil*

I took part in a project hosted by the business incubator at the Federal University of Technology - Paraná to develop a smart irrigation automation system based on soil moisture measurements. During this time, I

- Co-authored two successful grant proposals, obtaining funding for the research and development of the smart irrigation system
- Wrote the firmware for an irrigation controller with sectoring capabilities and moisture parametrization using C and FreeRTOS
- Designed and prototyped a wired capacitive soil moisture sensor
- Supervised the development of a wireless capacitive soil moisture sensor using LoRa for data transmission

### Developer at Xpert Automation Technology <span class="cv-date">11/2017 - 09/2018</span>
*Pato Branco, PR, Brazil*

I started at Xpert as an engineering intern and became part of the team upon completion of the internship. During my time at Xpert, I

- Analyzed, simulated and prototyped analog circuits for magnetostrictive sensors for fuel gauging
- Wrote firmware in C to interface NXP microcontrollers to time-of-flight ICs

### Research assistant at the University of Vermont <span class="cv-date">05/2016 - 07/2016</span>
*Burlington, VT, USA*

After completing my two semesters abroad at UVM, I did a 10-week summer internship at the Dunlop Lab, where I
- Prototyped a platform for holding test tubes and exposing them to controlled LED illumination for optogenetics experiments
- Cultured bacteria and conducted optogenetics experiments

### Teaching assistant at National Service of Industrial Training <span class="cv-date"> <span>07/2013 - 12/2013</span> <span>02/2015 - 06/2015</span></span>
*Pato Branco, PR, Brazil*


- Lectured on digital electronics and microcontrollers with C programming
- Supervised students' final projects

### Developer at Chiptronic Automotive Technology <span class="cv-date">02/2012 - 11/2012</span>
*Piraju, SP, Brazil*

I started at Chiptronic as a technician intern and became part of the team upon completion of the internship. During my time at Chiptronic, I

- Wrote firmware in Assembly to interface PIC microcontrollers to RFID key fobs and flash memories
- Decoding seed-key algorithms to unlock RFID devices

-----------

## Projects

-----------

### [OPiL](https://gitlab.rhrk.uni-kl.de/lrs/opil) — an Open Processor-in-the-Loop framework

OPiL is a framework that enables Processor-in-the-Loop testing independent of the simulation platform and the real-time target. I use OPiL mainly to 

- Validate and profile the firmware of controllers in a closed-loop environment
- Profile the execution time of model predictive controllers in embedded systems
- Validate and profile hardware and software co-design of model predictive controllers on SoCs


### [OCP](https://github.com/mtguerreiro/ocp) — the Open Controller Project 

OCP is a framework that I use to automate tests on embedded controllers. OCP consists of

- A C library for the real-time target that manages the selection and parametrization of controllers, a scope functionality to store measurements and internal signals during transients, and a TCP server to provide an interface
- A Python module to interface with the real-time target in order to write and read parameters, making it possible to automate testing at a high level


### [pyctl](https://github.com/mtguerreiro/pyctl) — A Python package for predictive control

pyctl is a Python package that I developed to simulate linear model predictive control of discrete-time systems. Some of the features of pyctl are

- Capable of C code generation with the option to use a custom QP solver or OSQP
- Contains control design functions for some dc-dc converter topologies

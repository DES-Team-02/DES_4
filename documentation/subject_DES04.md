# **DES Project - PDC(Park Distance Control) System**

</br>


- [**DES Project - PDC(Park Distance Control) System**](#des-project---pdcpark-distance-control-system)
  - [Introduction](#introduction)
  - [Project Goals and Objectives](#project-goals-and-objectives)
  - [Technical Requirements](#technical-requirements)
  - [Project Timeline](#project-timeline)
  - [Submission](#submission)
  - [Evaluation](#evaluation)
  - [References](#references)

</br>

## Introduction

The goal of this project is to enhance the Piracer by integrating a Park Distance Control (PDC) system, running on a Raspberry Pi (RPi) inside the head unit. The PDC system will utilize ultrasonic sensors to detect the distance between the vehicle and any obstacles, and provide an audible response to the driver. In addition, the full stack feature development will be integrated into the existing Yocto image, creating a comprehensive and fully functional system. The project aims to provide hands-on experience in developing and integrating advanced driver-assistance features, as well as provide a deeper understanding of the software and hardware involved in modern vehicles. The following sections will provide further details on the technical requirements, system architecture, software design, implementation, results, and references for this project.  
</br>


## Project Goals and Objectives

Project Goals:

* To design and implement a Park Distance Control (PDC) system for the piracer, which will make use of ultrasonic sensors to measure the distance between the car and any obstacles in its path.
* To integrate the full-stack feature development of the PDC system into the existing Yocto image running on the Raspberry Pi inside the head unit.
* To provide an audible response to the driver, indicating the distance to obstacles, thereby enhancing safety and convenience while parking.

Project Objectives:

* To research and evaluate the feasibility of using ultrasonic sensors for PDC system.
* To design and implement a complete software architecture for the PDC system, including all required communication protocols, drivers, and libraries.
* To test and validate the PDC system to ensure accurate measurement of distance and smooth integration with the existing Yocto image.
* To refine and improve the system based on the results of testing, making necessary updates and improvements to meet the project goals.

</br>


## Technical Requirements

the following technical requirements must be considered for the implementation of the Park Distance Control (PDC) system:

1. Hardware Requirements:
    * RPi: The project requires a Raspberry Pi as the main processing unit.
    * Ultrasonic sensors: A set of ultrasonic sensors will be used to measure the distance between the car and any objects in front of it.
    * CAN bus: The CAN bus will be used to connect the ultrasonic sensors to the RPi for data transfer.
    * Yocto: The Yocto project will be used as the base for building the required software stack for the RPi.
2. Software Requirements:
    * Operating System: A custom Linux-based operating system will be developed using Yocto, which will run on the RPi.
    * CAN driver: A CAN driver will be implemented on the Yocto image to enable communication between the ultrasonic sensors and the RPi over the CAN bus.
    * Ultrasonic sensor driver: A custom driver will be implemented to interface the ultrasonic sensors with the RPi.
    * Park Distance Control (PDC) software: A software application will be developed that implements the PDC functionality and integrates it with the existing head unit software.
3. Functional Requirements:
    * Distance measurement: The software must be able to measure the distances between the car and objects in front of it accurately.
    * Audible response: The software must provide an audible response to the driver to indicate the distance between the car and an object.
    * Display integration: The PDC functionality must be integrated into the existing head unit software and displayed on the screen.
4. Non-Functional Requirements:
    * Performance: The PDC software must be able to process distance measurements in real-time, with low latency.
    * Reliability: The software must be robust and reliable, with minimal downtime.
    * Maintainability: The code must be well-documented and easy to maintain, with a modular design.


</br>

## Project Timeline

The following is a tentative timeline for the implementation of the Park Distance Control (PDC) system on the RPi inside the head unit of the Piracer:

1. Initial research and planning: 3 days

    This stage involves reviewing existing literature and documentation on PDC systems, ultrasonic sensors, Yocto image, and determining the best approach for integration with the existing system.

2. Procurement of hardware and software components: 2 days

    This stage involves ordering ultrasonic sensors, necessary cables and connectors, as well as acquiring the necessary software components such as the Yocto image and IPC libraries.

3. Hardware setup: 2 days

    This stage involves mounting the ultrasonic sensors on the Piracer, connecting them to the RPi, and ensuring that the sensors are functioning correctly.

4. Software integration: 3 weeks

    This stage involves integrating the PDC software into the existing Yocto image, adding the audible response feature, and testing to ensure that the PDC system is working correctly.

5. User interface design and implementation: 1 weeks

    This stage involves designing the user interface for the PDC system and integrating it into the head unit of the Piracer.

6. System testing: 1 weeks

    This stage involves testing the PDC system under various conditions to ensure that it is working correctly and meets the desired specifications.

7. Documentation and final touches: 2 days

    This stage involves documenting the steps taken in the implementation process, as well as making any necessary final adjustments to the PDC system.


This timeline assumes that there will not be any major obstacles or delays during the implementation process and is subject to change if necessary. The goal is to complete the implementation of the PDC system within 7 weeks.  
</br>


## Submission

Turn in a github repository with following information:

* Detailed technical specifications of the ultrasonic sensors used in the project.
* Schematics and wiring diagrams for the park distance control system.
* Source code for the park distance control system, including any necessary libraries and dependencies.
* Test results and performance data for the park distance control system.
* A list of online resources and tutorials used in the project.
* Any additional material that supports the understanding of the project and provides context to the reader.

</br>

## Evaluation
In this project, every team must host ONE final submission demo & presentation (max. 30 mins) in front of all the other teams. Each team must find a way to organize this presentation making sure that all the other teams can be present and participate actively (Please work out what date/time works the best for every team). The date and time of each team's presentation must be communicated to staff well in advance (at least a week in advance). It is presenting team's responsibility to make sure that all the forms are filled in **immediately** after the presentation.
FORMS will be available soon...

</br>

## References

Raspberry Pi Foundation. (2021). Raspberry Pi Documentation. https://www.raspberrypi.org/documentation/

Yocto Project. (2021). Yocto Project Documentation. https://www.yoctoproject.org/documentation/

Inter-Process Communication. (2021). Wikipedia. https://en.wikipedia.org/wiki/Inter-process_communication

Controller Area Network. (2021). Wikipedia. https://en.wikipedia.org/wiki/Controller_Area_Network
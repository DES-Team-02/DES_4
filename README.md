**!! UNDER CONSTRUCTION !!**

# DES04 - Parking Distance Control (PDC) and Advanced Driver Assistance Systems (ADAS) <br>

## Table of contents
  - [Introduction](#introduction)
  - [Collaborators](#collaborators)
  - [Demonstration Video](#demonstration-video)
  - [Project Structure](#project-structure)
  - [Architecture](#architecture)
  - [Documentation](#documentation)

## Introduction
This project merges the requirments of [Park-Distance-Control (DES04)](https://github.com/SEA-ME/DES_PDC-System) and [autonomous lane detection (ADS01)](https://github.com/SEA-ME/ADS_Autonomous-Lane-Detection) into a scalable open-source E/E Architecture. <br>

The goal of this project is to enhance integrating a new embedded in-vehicle feature <Park Distance Control (PDC) system> and a new in-vehicle feature for ADAS Lane Keeping Assist System (LKA). <br>
The PDC system utilizes ultrasonic sensors to detect the distance between the vehicle and any obstacles, and provide an response to the driver. In addition, the full stack feature development will be integrated into the existing Yocto image, creating a comprehensive and fully functional system. <br>
Furthermore, the intersection of virtual simulations and real-world applications is used to enable  mechanisms of the Lane Keeping Assist System (LKA), a pivotal Level 1 autonomous driving feature. Using advanced simulation platforms and hardware implement an LKAS that can operate both virtually and in the real world. 

The following sections will provide further details on the technical requirements, system architecture, software design, implementation, results, and references for this project.

## Collaborators
If you find any kinds of bugs or issues, please contact 
[Kian](https://github.com/kianwasabi), 
[Jinghong](https://github.com/Lagavulin9), 
[Seungwoo](https://github.com/SeungWoo-L), 
[Nikas](https://github.com/NikDoh)👌🏽

## Demonstration Video
The following videos demonstrate the features of the project. <br>

Demo Feature 1: <br>
<img src="./documentation/images/.gif" width="40%" margin="120%"> <br>

## E/E Architecture
The image below shows the centralized E/E architecture. <br>
It is devided into two layers: <br>
  - **Computing Layer** <br>
  - **Sensor Layer**<br>

In the **Computing Layer**, you will find the central computing Unit, the ADAS Unit and the Cloud-Connector Unit. <br>
The **Sensor Layer** is sub-devided into Zones: 
  - **Front Zone** <br>
  - **Central Zone** <br>
  - **Rear Zone** <br>

The Front Zone contains the PDC System. 
The Central Zone contains the Drive-Train & Battery Control. 
The Rear Zone contains the Speed Sensor System. <br>
<img src="./documentation/images/ee_architecture.png" width="75%" margin="120%"> <br>

## Project Structure

This repository is structured as followed. <br>
- `apps`: [submodules](/apps) for the **Computing Layer** <br> 
  - [Cloud Connector / Fleet Manager](https://github.com/DES-Team-02/fleet-manager)<br>
  - [Front Zone CAN Receiver](https://github.com/DES-Team-02/can_front)<br>
  - [Rear Zone CAN Receiver](https://github.com/DES-Team-02/can_rear) <br>
  - [ADAS (Lane Assistance)](https://github.com/DES-Team-02/lane_assistant) <br>
  - [Drive Train Controller](https://github.com/DES-Team-02/car_control) <br>
  - [Battery Information](https://github.com/DES-Team-02/battery_info) <br>
- `image`: [submodule](/image/) for the Central Control Units Yocto image.
  - [Meta Team2](https://github.com/DES-Team-02/meta-team2)
- `sensors`: [submodules](/sensors/) for the **Sensor Layer**. <br>
  - [Park Distance Control](https://github.com/DES-Team-02/pdc_sensor)<br>
  - [Speed Sensor](https://github.com/DES-Team-02/rpm_sensor)<br>
- `documentation`: Please see submodules README.md for detailed informations. Additional project documentation can be found [here](/documentation/). <br>

## Software- and Harware Architecture
The following image gives a brief overview about the [software structure](/documentation/software_structure.md) that runs on the cars' [system structure](/documentation/system_structure.md). <br>
Each application serves a different functional purpose and uses different peripheral interfaces and devices. <br> 
BMWs' [CommonAPI](/documentation/common_api.md) ensures the communication between the applications in the **Computing Layer** via **Scalable Service-Oriented Middleware over IP (SOME/IP)**. It is easy to add more apps by using our [CI/CD workflows for CommonAPI](/documentation/workflows.md). <br>
The rear zone controller feeds speed sensor messages to the cars' **CAN Bus (interface 1)**. <br>
The front zone controller feeds distance informations of a sonar o the cars' **CAN Bus (interface 0)**.
The Central Computing Unit operates with a **custom-made Yocto Image** deployed on a **Raspberry Pi4B**. 
The ADAS runs on a **NVIDIA Jetson Nano**. <br>
The NVIDIA Jetson Nano is connected to the Raspberry Pi via **Ethernet**. <br>

## Continuous Integration and Continuous Deployment (CI/CD)

> _The development in each submodule is done individually by the assigned developer following the teams' [project conventions](/documentation/project_conventions.md)._ <br>

### Continuous Integration (CI)
The CI is done by the developers in the submodules. <br>
Once a change is pushed to the main branch, the CI will be triggered. <br>
### Continuous Deployment (CD)
The Meta Team2 submodule is the only submodule that has a CD workflow. <br>
It fatches the latest changes from the submodules and builds the Yocto Image. <br>
To roll out the software, the sensors' controller and the ECU needs to be flashed. <br> 
A OTA update is not implemented yet. <br>

## Documentation
1) Requirements Gathering: 
    - [🧑🏽‍🏫 subject DES04](/documentation/subject_DES04.md) 
    - [🧑🏽‍🏫 subject ADS01](/documentation/subject_ADS01.md) 
    - [📝 project requirments](/documentation/project_requirments.md)
2) Planning Design, System & Software:
    - [🧑🏽‍🎨 Human Machine Interface design](/documentation/design.md)
    - [🏎 system structure](/documentation/system_structure.md)
    - [👨🏽‍💻 software structure](/documentation/software_structure.md)
3) Team Collaboration:
    - [🔓 conventions](/documentation/project_conventions.md)
    - [📋 kanban board](https://github.com/orgs/DES-Team-02/projects/1)
4) Integration: <br>
    - Technologies: tbd. <br>
    - Apps & Sensors: see submdoules's README.md <br>
5) Testing: 
    - [📝 checklist requirments](/documentation/project-requirments.md)






# DES03 Project - Head Unit

!! UNDER CONSTRUCTION !! <br>

## Table of contents
  - [Introduction](#introduction)
  - [Demonstration Video](#demonstration-video)
  - [Architecture](#architecture)
  - [Project Structure](#project-structure)
  - [Documentation](#documentation)
  - [Collaborators](#collaborators)
  <!-- - [Known Issues](#known-issues) -->

## Introduction
This project is part of the [embedded software development cirriculum at SEA-ME](https://github.com/SEA-ME/DES_Head-Unit). <br>

This project aims to develop a **Head Unit application** running on a Raspberry Pi (RPi as ECU) alongside the previously developed PiRacer **Instrument Cluster application**. <br> 
The Head Unit application will provide additional features like **ambient lighting, gear selection, and a media app**. Furthermore, the project will use **Scalable Service-Oriented Middleware(vSOME/IP)** for the in-vehicle communication and **Yocto as the build system** for the ECU. <br> 

## Collaborators
If you find any kinds of bugs or issues, please contact 
[Kian](https://github.com/kianwasabi), 
[Jinghong](https://github.com/Lagavulin9) or 
[Seungwoo](https://github.com/SeungWoo-L). 

## Demonstration Video
The following videos demonstrate the features of the project. <br>

Head-Units' Media Player : <br>
<img src="./documentation/images/media_player.gif" width="40%" margin="120%"> <br>
Ambient Lighting Control via Head-Unit: <br>
<img src="./documentation/images/gear_selection.gif" width="40%" margin="120%"> <br>
Gear Selection by Head-Unit: <br>
<img src="./documentation/images/instrument_cluster.gif" width="40%" margin="120%"> <br>
Essential Car Information on Dashboard: <br>
<img src="./documentation/images/car_info.gif" width="40%" margin="120%"> <br>
 
## Project Structure

This repository contains all the submodules that were used in this project. <br>
The following image shows the "DES_03_Head-Unit" projects' structure and workflow. <br>
This repository is devided into these folders: <br>
- `apps`: Contains submodules that hold the source code to run the car. <br> 
- `sensors`: Contains submodules for the sensors' controller that feed the cars' CAN bus. <br>
- `image`: Contains a submodule that holds everything needed to bitbake the cars' ECU yocto image. <br>
- `documentation`: Contains all the documentations. <br>
The workflow is as follows: <br>
Sensors: <br>
1. Clone DES_3_Head-Unit repository. <br>
2. Flash the sensors' controller (via Arduino IDE).<br>
Yocto Image: <br>
1. Clone DES_3_yocto repository. <br>
2. Build the yocto image. The recipes are directly fetching the applications source code from the submodules repos. <br>
3. Push the yocto image to repository. <br>
4. Flash the yocto image on the ECU (by loading the image on a SD-Card and plug it in the Raspberry Pi). <br>

<img src="./documentation/images/project_structure.png"> <br>

## Architecture
! Insert a diagram of the architecture here. ! <br>

For a more detailed explanantion, see: [software architecture](/documentation/software_structure.md). <br>

## Documentation
- Requirements Gathering: 
  - [🧑🏽‍🏫 subject](/documentation/subject.md)
  - [📝 project requirments](/documentation/project-requirments.md)
- Planning Design, System & Software:
  - [🧑🏽‍🎨 frontend design](/documentation/design.md)
  - [🏎 system strucutre](/documentation/system-structure.md)
  - [👨🏽‍💻 software strucutre](/documentation/software_structure.md)
  - [🔓 conventions](/documentation/project_conventions.md)
  - [📋 project kanban ](https://github.com/users/Lagavulin9/projects/2)
- Integration:
  - Applications: 
    - [1️⃣ head unit](/documentation/headunit.md)
    - [2️⃣ dashboard](/documentation/dashboard.md)
    - [3️⃣ can bus receiver](/documentation/can_receiver.md)
    - [4️⃣ car control](/documentation/car_control.md)
    - [5️⃣ car information](/documentation/car_info.md)
  - Sensors: 
    - [6️⃣ rpm speed sensor](/documentation/rpm_speedsensor.md)
  - Technologies:
    - [🔛 can bus](/documentation/common_api.md)
    - [🔛 vSOME/IP & CommonAPI](/documentation/common_api.md)
    - [🤖 CI/CD workflows](/documentation/workflows.md)
    - [🍪 Yocto](/documentation/yocto.md)
- Testing: 
  - [📝 test requirments](/documentation/project-requirments.md)

<!-- ## Known Issues 
Issues we found while testing. <br>
| Issue | Description |
| --- | --- | -->



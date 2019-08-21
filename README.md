> DEUTSCH: [**fischertechnik Lernfabrik 4.0 (de)**](README_de.md)

# fischertechnik Training Factory Industry 4.0 (en)
This project contains the C/C++ library *TxtSmartFactoryLib* and the main (*TxtFactoryMain*) and client (*TxtFactoryClient*) programs
for the fischertechnik [**Training Factory Industry 4.0**](https://www.fischertechnik.de/en/service/elearning/teaching/lernfabrik-4). The library requires at least the TXT firmware version 4.5.0.

## Overview
The factory consists of the following stations:
* **SSC**: Sensor Station with Camera
* **HBW**: High-Bay Warehouse
* **VGR**: Vacuum Gripper Robot
* **DPS**: Delivery and Pickup Station
* **MPO**: Multi-Processing Station with Oven
* **SLD**: Sorting Line with Color Detection

The next picture shows the network overview with the TXT controllers.
![Overview Network](doc/Overview_Network.PNG "Overview Network")

## Installation
The programs can be copied using the TXT [WEB server](doc/WEBServer.md).

## User Programs
The default programs you will find in the [bin](https://github.com/fischertechnik/txt_training_factory/tree/master/bin) folder:
* **TxtFactoryMain.cloud** (local MQTT broker, MQTT bridge, MQTT client for SSC)
* **TxtFactoryMPO** [[Finite State Machine MPO](https://fischertechnik.github.io/txt_training_factory_doc/html/dot_TxtMultiProcessingStationRun.png)]
* **TxtFactoryHBW** [[Finite State Machine HBW](https://fischertechnik.github.io/txt_training_factory_doc/html/dot_TxtHighBayWarehouseRun.png)]
* **TxtFactoryVGR** (main flow control) [[Finite State Machine VGR](https://fischertechnik.github.io/txt_training_factory_doc/html/dot_TxtVacuumGripperRobotRun.png)]
* **TxtFactorySLD** [[Finite State Machine SLD](https://fischertechnik.github.io/txt_training_factory_doc/html/dot_TxtSortingLineRun.png)]

The programs for parking position you will find in the [bin](https://github.com/fischertechnik/txt_training_factory/tree/master/bin) folder:
* **TxtParkPosSSC**
* **TxtParkPosMPO**
* **TxtParkPosHBW**
* **TxtParkPosVGR**

## MQTT Interface
The [MQTT Interface](TxtSmartFactoryLib/doc/MqttInterface.md) describes the topics and the payload of the MQTT clients and the configuration of the mosquitto MQTT bridge. 

## API Reference C/C++ Library
The Doxygen documentation of the C/C ++ library classes can be found in the [API Reference](https://fischertechnik.github.io/txt_training_factory_doc/html/index.html).

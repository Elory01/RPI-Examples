# IoT JumpWay Raspberry Pi Basic LED Example

![IoT JumpWay Raspberry Pi Basic LED Example Docs](../images/Raspberry-Pi-Basic-LED-Example.png)

## Introduction
Want to take your first steps into the magical world of the Internet of Things, or want to find out how easy it is to use the IoT JumpWay as your secure IoT communication platform? This tutorial is for you an will hold your hand through setting up your first Raspberry Pi project powered by the IoT JumpWay.

## What Will We Build?

This tutorial is a simple tutorial that will help you take your first steps to using the IoT JumpWay to connect your IoT devices and applications to the Internet of Things.

The tutorial will use IoT JumpWay Python MQTT Library for communication, a Raspberry Pi with an added LED, and an application that can control the LED via the IoT JumpWay.

## Python Versions

- 2.7
- 3.4 or above

## Software Requirements

1. Jessie
2. [IoT JumpWay Python MQTT Client](https://github.com/iotJumpway/JumpWayMQTT "IoT JumpWay Python MQTT Client")

## Hardware requirements

![IoT JumpWay Raspberry Pi Basic LED Example Docs](../images/Hardware.jpg)

1. Raspberry Pi.
2. 1 x LED.
3. 1 x 220 ohm Resistor
4. 2 x Jumper Wires
5. 1 x Breadboard

## Before You Begin

There are a few tutorials that you should follow before beginning, especially if it is the first time you have followed any of our Raspberry Pi tutorials or if it is the first time you have used the IoT JumpWay Developer Program. If this is the first time you have used the IoT JumpWay in your IoT projects, you will require a developer account and some basics to be set up before you can start creating your IoT devices. Visit the following [IoT JumpWay Developer Program Docs (5-10 minute read/setup)](https://github.com/iotJumpway/IoT-JumpWay-Docs/ "IoT JumpWay Developer Program Docs (5-10 minute read/setup)") and check out the guides that take you through registration and setting up your Location Space, Zones, Devices and Applications (About 5 minutes read).

- [IoT JumpWay Developer Program Docs (5-10 minute read/setup)](https://github.com/iotJumpway/IoT-JumpWay-Docs/ "IoT JumpWay Developer Program Docs (5-10 minute read/setup)")

- [Preparing Your Raspberry Pi](https://github.com/iotJumpway/IoT-JumpWay-RPI-Examples/blob/master/_DOCS/1-Raspberry-Pi-Prep.md "Preparing Your Raspberry Pi")

## Preparing Your Raspberry Pi 3

Take some time to ensure your Raspberry Pi firmware and packages are up to date, and that your device is secure by following the [Raspberry Pi 3 Preparation Doc](https://github.com/iotJumpway/IoT-JumpWay-RPI-Examples/blob/master/_DOCS/1-Raspberry-Pi-Prep.md "Raspberry Pi 3 Preparation Doc") tutorial.

## Cloning The Repo

You will need to clone this repository to a location on your Raspberry Pi 3. Navigate to the directory you would like to download it to and issue the following commands.

    $ git clone https://github.com/iotJumpway/IoT-JumpWay-RPI-Examples.git

## Install Requirements

    $ cd IoT-JumpWay-RPI-Examples/Basic-LED/Python
	$ (sudo) pip install --upgrade pip
    $ (sudo) pip install -r requirements.txt

## Setting Up Your Raspberry Pi

![IoT JumpWay Raspberry Pi Basic LED Example Docs](../images/Blinking.jpg)

First of all you need to connect up an LED to your Raspberry Pi. To connect the LED you will need a breadboard, a 220 ohm resistor, and two jumper wires.

1. Place the LED on your breadboard.
2. Connect the short leg of the LED to pin 18 of your Raspberry Pi using a jumper wire.
3. Connect one end of the resistor to the long leg of your LED.
4. Connect the other end of the resistor to the 3v output of the Raspberry Pi.

## Device / Application Connection Credentials & Sensor Settings

- Follow the [IoT JumpWay Developer Program (BETA) Location Device Doc](https://github.com/iotJumpway/IoT-JumpWay-Docs/blob/master/4-Location-Devices.md "IoT JumpWay Developer Program (BETA) Location Device Doc") to set up your device, and the [IoT JumpWay Developer Program (BETA) Location Application Doc](https://github.com/iotJumpway/IoT-JumpWay-Docs/blob/master/5-Location-Applications.md "IoT JumpWay Developer Program (BETA) Location Application Doc") to set up your application.

![IoT JumpWay Raspberry Pi Basic LED Example Docs](../../images/main/Device-Creation.png)

- Retrieve your connection credentials and update the config.json file with your new connection credentials and actuator (LED) settings.

```
"IoTJumpWay": {
    "Location": 0,
    "Zone": 0,
    "Device": 0,
    "DeviceName" : "",
    "App": 0,
    "AppName": ""
}
```

```
"Actuators": {
    "LED": {
        "ID": 0,
        "PIN": 18
    }
}
```

```
"IoTJumpWayMQTT": {
    "MQTTUsername": "",
    "MQTTPassword": "",
    "AppMQTTUsername": "",
    "AppMQTTPassword": ""
}
```

## Execute The Programs

    $ sudo python/python3 Device.py
    $ sudo python/python3 Application.py

## Viewing Your Data

Each command sent to the device is stored in the [IoT JumpWay](https://iot.techbubbletechnologies.com/ "IoT JumpWay"). You will be able to access the data in the [IoT JumpWay Developers Area](https://iot.techbubbletechnologies.com/developers/dashboard/ "IoT JumpWay Developers Area"). Once you have logged into the Developers Area, visit the [IoT JumpWay Location Devices Page](https://iot.techbubbletechnologies.com/developers/location-devices "Location Devices page"), find your device and then visit the Commands Data page to view the data sent from your device.

![IoT JumpWay Raspberry Pi Basic LED Example Docs](../../images/main/SensorData.png)

![IoT JumpWay Raspberry Pi Basic LED Example Docs](../../images/main/WarningData.png)

## Bugs/Issues

Please feel free to create issues for bugs and general issues you come across whilst using the IoT JumpWay Raspberry Pi Examples. You may also use the issues area to ask for general help whilst using the IoT JumpWay Raspberry Pi Examples in your IoT projects.

## Contributors

[![Adam Milton-Barker, Intel® Software Innovator](../../images/main/Intel-Software-Innovator.jpg)](https://github.com/AdamMiltonBarker)
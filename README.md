![jenkins-head-ci](https://github.com/jenkins-head/head-firmware/workflows/jenkins-head-ci/badge.svg)
[![CodeFactor](https://www.codefactor.io/repository/github/jenkins-head/jenkins-head-firmware/badge)](https://www.codefactor.io/repository/github/jenkins-head/jenkins-head-firmware)

# General

This Project is based on [platformio.io](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide#review-details) for the installation please follow the plug-in installation guide.

# BLE Interface
This GATT Server provides a service with the UUID `3bea760b-ea72-44d6-a189-2c27766bdcc4`. This service contains the following characteristics.

| characteristic | UUID |
| ---- | ---- |
| red | `2e252e00-2f8b-4326-91de-26742dda4aa7` |
| green | `6aeba5cd-4476-43b6-830b-021109ae6dea` |
| blue | `46f27bf3-5b1c-403e-bc20-90934a784e66` |
| brightness | `fc75589b-54ae-4b28-b54d-a35979f42b39` |


# System Overview

![Class Diagram](./doc/diagrams/out/ClassDiagramOverview/GATT-Server_overview.png)

## GattColorLedServer
This class implements the **BLECharacteristicCallbacks** Interface to handles following functions
- `onRead`
- `onWrite`

This interface is part of the BLE stack

## ColorHandlerInterface

This interface abstract a handler that can handle a RGB LED.

## NeoPixelHandler

This class implements the `ColorHandlerInterface` to handle the `setColor` function and controls a NEO Pixel(s).

# Flashing the firmware.bin
The [espurna](https://github.com/xoseperez/espurna) documentation describes the procedure in detail. Please follow the documentation [espurna/flashing](https://github.com/xoseperez/espurna/wiki/Binaries).

Eugen hat was geaendert
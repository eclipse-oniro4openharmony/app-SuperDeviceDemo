# Super Device Demo

## Table of Contents

1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Features](#features)
4. [Setup Instructions](#setup-instructions)
5. [Quick Start Guide](#quick-start-guide)
6. [Link](#link)

## Overview

This demo showcases a simple implementation of cross-device data synchronization using the `distributedKVStore` module in OpenHarmony. After pairing devices on the same network and verifying a PIN code, the sender device can push messages to the receiver device through a distributed key-value store. The receiver listens for data changes and updates its state accordingly.

UI effects are as follows:
![image1.jpg](./images/image1.jpg)

> **Note:**
>
> This example uses system interfaces, so you need to manually replace the Full SDK to compile successfully. For specific steps, refer to the [Replacement Guide](https://docs.oniroproject.org/application-development/environment-setup-config/full-public-sdk/).

## Requirements

* Two OpenHarmony-compatible devices (e.g., `Dayu200 Development Board` and `OpenHarmony Developer Phone`)
* Valid network connection
* Proper permissions (`ACCESS_SERVICE_DM` and `DISTRIBUTED_DATASYNC`)

## Features

* Discover nearby devices on the same network
* Authenticate and pair discovered devices using a PIN code
* Send data from one device to another in real time

## Setup Instructions

**1. Clone the repository**

```bash
git clone https://github.com/eclipse-oniro4openharmony/app-SuperDeviceDemo
```

**2. Build and Deploy**

* Ensure you are using API level 11
* Confirm your app is a `system-level` application
* Sign the application with valid signature configurations
* Connect two OpenHarmony-compatible devices (e.g., Dayu200 Development Board and OpenHarmony Developer Phone)
* Ensure both devices are connected to the same network
* Click the `Run` button in DevEco Studio to install the application

> **Note:**
>
> See this [tutorial](https://docs.oniroproject.org/application-development/codeLabs/) for how to configure the project as a `system-level` application.

## Quick Start Guide

**1. Install the app on both devices**
Ensure both devices support OpenHarmony and are connected to the same network.

**2. Pair devices**

* Tap the **Find Nearby Device** button
* Select the receiver device from the pop-up list
* A verification box will appear on the receiver device; after it is accepted, a random PIN code will be generated
* Enter the PIN code on the sender device
* Pairing is complete

**3. Determine roles**
Once paired, the initiating device is labeled as the `Sender`, and the other as the `Receiver`.

**4. Send data**

* On the `Sender`, enter text in the input box
* Tap **Send** to push the message

**5. Receive data**
The `Receiver` will automatically receive and display the message.

**6. Unbind if needed**

* Tap **Unbind** to disconnect the paired device and reset the session

## Link

For detailed code explanations, architecture deep-dives, and step-by-step implementation guides, please refer to this [tutorial](./Tutorial.md).

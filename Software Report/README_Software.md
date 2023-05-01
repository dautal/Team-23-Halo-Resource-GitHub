<h1 align="center">Software Report</h1>

<p align="center"><b>Team 23: Halo</b></p>

<br/>


## Navigation

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#software-report">Title</a>
    </li>
    <li>
      <a href="#overview">Overview</a>
    </li>
    <li>
      <a href="#repositories">Repositories</a>
    </li>
    <li>
      <a href="#setup">Setup</a>
    </li>
  </ol>
</details>

<br/>


## Overview

The project consists of two repositories, one for the iOS app and another for the Arduino code. The Arduino code measures voltage and accelerometer data and transmits it over Bluetooth Low Energy (BLE) using the ArduinoBLE library. The code includes functions for collecting and computing the average voltage and acceleration data. The iOS app allows users to connect to the Smart Drink Protector device and view information about the product, including a video demonstration and instructions on how to use it. The app also notifies the user if the cover has been removed from their drink. To set up the device, the Arduino code is preloaded onto the Arduino, and the iOS app can be installed from the App Store or built from the Github repository using Xcode. The app requires Bluetooth access and the option to enable notifications to function properly.

<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


## Repositories


There are 2 repositories, one for the Arduino code and another for the iOS app.

* <a href="https://github.com/dautal/HaloApp">Arduino Code</a>
  * The Arduino code consists of two main components: measuring the voltage and accelerometer data and transmitting that data over Bluetooth Low Energy (BLE). The sketch begins by including the necessary libraries, including the ArduinoBLE and Arduino_LSM9DS1 libraries.
  * The code sets up a BLE service and characteristic for transmitting the voltage data. The program then initializes the IMU (inertial measurement unit) to read accelerometer data. In the loop function, the program waits for a central device to connect to the peripheral. Once a connection is established, the program enters a loop that updates the voltage and accelerometer data at a specified refresh rate (dispRefresh). This data is then transmitted to the central device over BLE using the VoltageChar.writeValue() function.
  * The collectPoints() function collects a series of analog. The number of readings collected is determined by the AVG_WINDOW constant, and the sampleInterval specifies the time between each reading. The computeAvg() function then computes the average of the readings. The updateVoltage() function first calls collectPoints() to collect a series of voltage readings, and then computes the average voltage and the acceleration data from the IMU. This data is then formatted as a string and sent over BLE using VoltageChar.writeValue(). The voltage data is also stored in the voltage variable for reference. Overall, this code reads voltage and accelerometer data and transmits it over BLE using the ArduinoBLE library.
  * <a href="https://github.com/dautal/HaloApp/blob/main/README.md">README</a>
* <a href="https://github.com/dautal/Halo-Smart-Drink-Protector">iOS app</a>
  * The iOS application allows the user to connect the Smart Drink Protector to their phone, view information about the product, and access the website. The info button allows the user to watch a video demonstration as well as view instructions to better understand how to use the product. The website button takes the user to the website. The connect button allows the user to connect their device to their phone. The app features a start scanning button which will then show a list of discovered devices. Once connected the app will display whether the cover is on the drink. A green light means the cover is still on. A red light means the cover has been removed. If the cover is removed a notification will be sent to the user.
  * <a href="https://github.com/dautal/Halo-Smart-Drink-Protector/blob/main/README.md">README</a>
<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


### Setup
Each Halo device will have the Arduino with preloaded software. Once published to the App Store, the iOS app installation is simple and can be done by downloading the app from the App Store. The app will ask to access Bluetooth and to enable notifications. Bluetooth is required for the app to operate. The notifications are optional, but it is best to enable them to ensure the user knows when the cover has been removed. 

To install the app without using the App Store: 
* Download the code from the Github repository https://github.com/dautal/HaloApp
* Open the project in Xcode 
* Make the build, connect the device and upload the app onto it
* For the app to be successfully installed from the build, one should let the iOS device trust the developer certificate in the settings.
<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>

<h1 align="center">Engineering Addendum</h1>

<p align="center"><img src="Images/HaloLogo.png" width=500 height=300></p>
<p align="center"><b>Team 23</b></p>
<p align="center">Zirui Chen</p>
<p align="center">Alan Dautov</p>
<p align="center">Gabrielle Kuntz</p>
<p align="center">Pengyu Wu</p>
<p align="center">Chenyuan Zhao</p>

<br/>


## Navigation

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#engineering-addendum">Title</a>
    </li>
    <li>
      <a href="#project-overview">Project Overview</a>
    </li>
    <li>
      <a href="#repositories">Repositories</a>
    </li>
    <li>
      <a href="#current-status">Current Status</a>
    </li>
    <li>
      <a href="#future-work">Future Work</a>
    </li>
  </ol>
</details>

<br/>


## Project Overview

In recent years, the occurrence of drink spiking has increased globally, with college students being the primary targets. Drink spiking involves surreptitiously adding drugs or other substances to someone's drink without their knowledge or consent, which can have serious short and long-term health consequences, including memory loss, inability to speak, and blurred vision.

To address this issue and prevent drink spiking incidents, we have developed the Halo Smart Drink Protector, a battery-powered device that can seal the top of common glass types. It is a portable and user-friendly device that aims to offer a proactive solution to the problem. Halo's innovative features include a detection algorithm with a high success rate and a flexible and adjustable cover that fits various cup sizes. The device is easy to use and can be carried around, making it a convenient option for people who want to prevent drink spiking. We hope that the Halo Smart Drink Protector will be accessible and affordable to everyone who wants to prevent the potential harm caused by drink spiking.
<br/>
<p align="center"><img src="Images/SystemOverview.png" width=600 height=375></p>
The final product consists of four primary components, which are the Arduino nano 33 BLE, the outer layer cover, an app, and strain gauge sensor. The Arduino has two built-in sensors, a gyroscope and an accelerometer, which can sense rotations and acceleration, and a strain gauge with the amplifying module connected to it. By combining the accelerometer and gyroscope with the strain gauge module, Halo is able to recognize and detect potential cover removals and eliminate false positives, such as simple cup movement. The Arduino is equipped with a Bluetooth module that is capable of sending signals and connecting to the iOS app, which will send a notification to the user whenever the device senses a potential cover removal.

<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


## Repositories

Two repositories in addition to this one. One contains the Arduino code and the other contains the code for the iOS app.

* <a href="https://github.com/dautal/Halo-Smart-Drink-Protector">Arduino Code</a>
  * The Arduino code measures voltage (strain gauge) and accelerometer data, and then transmits the data over Bluetooth Low Energy (BLE). It includes necessary libraries, sets up a BLE service and characteristic, and initializes the IMU to read accelerometer data. Once a connection is established, the program enters a loop that updates the data at a specified refresh rate, collects a series of analog readings, computes the average, and then formats and sends the data over BLE using the ArduinoBLE library.

* <a href="https://github.com/dautal/HaloApp">iOS App Code</a>
  * The iOS app allows users to connect the Smart Drink Protector to their phone, view product information, and access the website. It has a connect button to connect the device and a start scanning button to show a list of discovered devices. The app displays whether the cover is on the drink using a green light (on) or a red light (off), and sends a notification to the user if the cover is removed. The info button provides a video demonstration and instructions.
<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>

## Challenges Faced
### Strain Gauge
A strain gauge is a device used to measure the strain or deformation of an object. It works on the principle that when a metal wire or foil is stretched, its resistance changes in proportion to the amount of strain. Strain gauges are extremely fragile and require careful installation and bonding to the surface of the object being measured. Any errors in the installation process can break the straing gauge or lead to innacurate readings. Additionally, the strain gauge must be mounted in a way that allows it to measure the strain in the desired direction. With these challenges, numerous strain gauges were broken and new ones needed to be resoldered to the amplifier module.
### Voltage Amplifier Module
A voltage amplifier is required for strain gauge measurements because the output signal of a strain gauge is typically very small, typically in the microvolt range. This small signal is difficult to measure directly, as it can be easily overwhelmed by noise and other electrical interference. The problem we faced is that for some reason not every amplifier actually works as intended. Some of them provided random negative values and the potentiometer did not work at all. We recommend using the certain amplifier module, which is listed in the Hardware Report. 
<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>

## Current Status
### Hardware
Right now all of the components are attached to a 3D printed surface, which is attached to the cloth cover. The hard surface is needed because it makes the  installation and removal of the cover onto the cup more convenient. The electric components are covered with the epoxy to make them water resistant and it also made the overall device light, since we do not have to use the 3D printed enclosure. 
<p align="center"><img src="Images/Final_prototype.jpg" width="50%" height="50%"></p>

### Software
Right now the iOS app is capable of connecting to the device, showing the current status of the cover, send the notifications if the possible cover removal is sensed. It also has the button that navigates the user to the Halo website which includes more info about the device and drink spiking. The  Arduino script is capable of measuring the strain gauge and acceleroemter data, and then transmitting the data to the iOS app. 
<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


## Future Work

One of the next steps would be to make the product more accessible to consumers, since right now a the unit cost of a signle Halo device is around $40. The desirable unit cost which the Halo team wants to achieve should be in the $20-$25 range. An approach to reduce the price of the device is to integrate all the components onto a PCB. This approach not only reduces the size and weight of the device, but it also helps lower the cost of manufacturing. By optimizing the design of the PCB, the number of components required can be reduced, leading to a reduction for the overall cost of each unit. Additionally, with fewer components, the manufacturing process will be simplified, leading to a reduction in assembly cost. 

Another step would be to improve the iOS app functionality and design. Features that could be included are a way for users to report where drink spiking incidences have occurred and a way for users to contact the police or an emergency contact. The overall UI could also be improved to make the overall experience more user friendly.

<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>

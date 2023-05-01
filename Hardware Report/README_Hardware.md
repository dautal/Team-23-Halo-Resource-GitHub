<h1 align="center">Hardware Report</h1>

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
      <a href="#bill-of-materials">Materials</a>
    </li>
    <li>
      <a href="#data-sheets">Data Sheets</a>
    </li>
    <li>
      <a href="#setup">Setup</a>
    </li>
  </ol>
</details>

<br/>


## Overview

This project aims to address the problem of drink spiking by introducing the Halo Smart Drink Protector, which is designed to detect and report any attempts of tampering with a drink. The device uses an Arduino Nano 33 BLE microcontroller, which is connected to an iOS app via Bluetooth technology, and is powered by two CR2032 batteries. The device detects the removal of a cup cover using an accelerometer and a strain gauge, which enables more accurate detection and eliminates false positives and negatives. The Arduino then communicates with the iOS app, which sends a notification to alert the user if their drink may be exposed. This section provides some useful information about the components used and how to set up the hardware for required by the project.


<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


## Bill Of Materials
<table>
    <tbody>
        <tr>
            <td colspan="1" rowspan="1">
                <p></p>
                <p align=center>No.</p>
            </td>
            <td colspan="1" rowspan="1">
                <p></p>
                <p align=center>Materials</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>Manufacturer</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>Quantity</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>Cost($)</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>Buying Links</p>
            </td>
        </tr>          
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Arduino Nano 33 BLE</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Arduino</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>30.00</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://www.amazon.com/Arduino-Nano-33-BLE/dp/B07WV59YTZ">Arduino</a></p>
            </td>
        </tr>
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>2</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Voltage Amplifier Module</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>CFsunbird</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>5.89 </p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://www.aliexpress.com/i/2251832629283875.html?gatewayAdapt=4itemAdapt">Amplifier</a></p>
            </td>
        </tr>
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>3</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Strain Gauge (BF350)</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>DAOKI</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>0.89</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://www.amazon.com/DAOKI-BF350-3AA-High-Precision-Pressure-Resistance/dp/B07X87CJD8/ref=sr_1_5?keywords=Strain+Gauges&qid=1682903267&sr=8-5">Strain Gauge</a></p>
            </td>
        </tr>
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>4</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>CR2032 Battery Holder</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>LampVPath</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>1.29</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://www.amazon.com/LAMPVPATH-cr2032-Battery-Holder-CR2032/dp/B07BXDHT4B/ref=asc_df_B07BXDHT4B/?tag=hyprod-20&linkCode=df0&hvadid=241973970700&hvpos=&hvnetw=g&hvrand=11993828507842142469&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1018127&hvtargid=pla-459538444737&psc=1">Battery Holder</a></p>
            </td>
        </tr>
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>5</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Cloth Cover</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>VIKOS Products</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>0.99</p>
            </td>
             <td colspan="1" rowspan="1">
                <p align=center><a href="https://www.amazon.com/dp/B0BHYGZ3DZ?psc=1&ref=ppx_yo2ov_dt_b_product_details">Cloth Cover</a></p>
            </td>
        </tr>
        <tr>
            <td colspan="4" rowspan="1">
                <p>Total Cost</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>40.64</p>
            </td>
        </tr>
    </tbody>
</table>

<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


## Data Sheets

<table>
    <tbody>
        <tr">
            <td colspan="1" rowspan="1">
                <p align=center>No.</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>Device</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center>Datasheet</p>
            </td>
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>1</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Arduino Nano 33 BLE</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://docs.arduino.cc/static/b640e8d82246763c38057a29a2d1e280/ABX00030-datasheet.pdf">link</a></p>
            </td>
        </tr>
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>2</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Strain Gauge</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://docs.arduino.cc/static/b640e8d82246763c38057a29a2d1e280/ABX00030-datasheet.pdf">link</a></p>
            </td>
        </tr>                                                                                                                             
        <tr>
            <td colspan="1" rowspan="1">
                <p align=center>2</p>
            </td>
            <td colspan="1" rowspan="1">
                <p>Voltage Amplifier Module</p>
            </td>
            <td colspan="1" rowspan="1">
                <p align=center><a href="https://datasheet.lcsc.com/lcsc/1908071505_Vishay-Micro-Measurements-CEA-06-062UWA-350_C404310.pdf">link</a></p>
            </td>
        </tr>                                                                                                                                                                                                                                                          
    </tbody>
</table>

<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>

                                        
## Device Setup

To make a working device (powered by a computer), three main compenents are required: Arduino Nano 33 BLE, amplifier module with a strain gauge, and a cloth cover.
                                        
The amplifer module has GND, VCC, and OUT pins:
* VCC should be connected to the 3.3v pin on the Arduino
* GND should be connected to the GND pin on the Arduino
* OUT should be connected to the voltage output pin, which is A4 in code that is in the Software repo. The A5 pin should be connected to the GND

After the device is properly connected, the strain gauge module should be attached to the side of the cloth protector as shown below. 
![straingauge](https://user-images.githubusercontent.com/75428513/235388934-b8cf5efd-c64a-4d06-af74-bfcdb16eb043.jpeg)




### Setup Procedure
                                      
* The Halo Smart Drink Protector uses two CR2023 3V lithium batteries to operate. Load two batteries into the battery cover located on the top of the device.
* To protect the drink, simply unwrap the cloth of the protector, stretch the elastic band of cloth, and cover the cup.
* Turn on the power switch located at the top of the protector. The processor in the protector will then send Bluetooth signals to the user’s cell phone. 
* The name of the protector will soon appear on the Bluetooth device list inside the application. Simply connect the device to the user’s phone by tapping its name.
* The protector will then detect any attempt to open the protector. When one tries to lift the cloth of the protector, the strain gauge on the elastic band of the cloth senses the change and alerts the user. 
* The protector detects any kind of action that includes the removal of the cloth. However, actions such as pressing on the cover, tapping the cup, or moving the cup will not send out an alert.
* When not using, turn off the power switch and simply wrap the protector with its cloth and carry it in your bag or in your pocket.

<br/>
<p align="center">(<a href="#navigation">to table of contents</a>)</p>


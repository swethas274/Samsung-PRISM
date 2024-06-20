# ZIGBEE AND BLUETOOTH

| S. No. | Bluetooth                                                                                                              | Zigbee                                                                                                                                                     |
|--------|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.     | The Bluetooth SIG (Special Interest Group) is the organization responsible for managing Bluetooth standards and devices. | The Zigbee Alliance is responsible for managing Zigbee and testing and approving Zigbee-based devices. IEEE standardizes all Zigbee-based protocols.         |
| 2.     | The frequency range supported in Bluetooth vary from 2.4 GHz to 2.483 GHz.                                             | The frequency range supported in Zigbee is mostly 2.4 GHz worldwide.                                                                                        |
| 3.     | There are seventy-nine RF channels in Bluetooth.                                                                       | There are sixteen RF channels in Zigbee.                                                                                                                    |
| 4.     | It uses GFSK modulation technique.                                                                                     | It also uses BPSK and QPSK modulation techniques like UWB.                                                                                                  |
| 5.     | There is a maximum of 8 cell nodes in Bluetooth.                                                                       | There are more than sixty-five thousand (65000) cell nodes in Zigbee.                                                                                       |
| 6.     | Bluetooth networks can be built using the point-to-point master-slave approach in which there is one master and up to seven slaves form a piconet, which leads to forming a scatter net which is a linking of two or more piconets. | Zigbee devices can be networked in a variety of generic topologies, including a star, mesh, and others. A cluster can be created by connecting different Zigbee-based network topologies. Zigbee Coordinator, Zigbee Router, and Zigbee Endpoint nodes make up any Zigbee network. |
| 7.     | Bluetooth requires low bandwidth.                                                                                      | Zigbee also requires low bandwidth but greater than Bluetooth’s bandwidth most of the time.                                                                 |
| 8.     | The radio signal range of Bluetooth is ten meters.                                                                     | The radio signal range of Zigbee is ten to one hundred meters.                                                                                              |
| 9.     | Bluetooth was developed under IEEE 802.15.1.                                                                           | Zigbee was developed under IEEE 802.15.4.                                                                                                                   |
| 10.    | Bluetooth batteries may be recharged.                                                                                  | Zigbee batteries cannot be recharged, but they last longer.                                                                                                 |
| 11.    | Bluetooth uses high data rates and a lot of power on large packet devices.                                             | Zigbee employs low data rates and little power on small packet devices.                                                                                     |
| 12.    | Bluetooth employs the Frequency Hopping Spread Spectrum. In frequency hopping, the carrier signal is made to fluctuate in frequency. | Zigbee employs the Direct Spread Spectrum technique. In direct spread spectrum, the original signal is mixed and recovered from a pseudo-random code at transmitter and receiver.                   |
| 13.    | A network speed of up to 250 megabits per second.                                                                      | A network speed of up to 1 megabit per second.                                                                                                              |
| 14.    | The time it takes to join a network using Bluetooth is about 3 seconds.                                                | The time it takes to join a network using Zigbee is about 30 milliseconds.                                                                                  |
| 15.    | Bluetooth’s protocol stack is 250K bytes in size.                                                                      | Zigbee’s protocol stack is 28K bytes in size.                                                                                                               |
| 16.    | Computer peripherals like wireless keyboards, mice, headsets, and other peripherals are the main use cases for Bluetooth-based applications. Additionally, several wireless remote controls and gesture-controlled devices communicate data via Bluetooth. | Systems built on the Zigbee protocol are intended for wireless sensor networking, and they are more popular with compact and energy-efficient gadgets. Zigbee-based networking is used in a variety of applications, including SCADA system sensors, medical devices, and television remote controls. |

| Modulation | Full Form                         | Use                                                                                                 |
|------------|-----------------------------------|-----------------------------------------------------------------------------------------------------|
| GFSK       | Gaussian Frequency Shift Keying   | Used in Bluetooth and other wireless systems for efficient and robust frequency modulation.         |
| BPSK       | Binary Phase Shift Keying         | Used in satellite communications and RFID systems for simple and robust binary phase modulation.     |
| QPSK       | Quadrature Phase Shift Keying     | Used in 4G LTE, satellite communications, and cable modems for efficient data transmission.          |

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20190610154515/Untitled-Diagram-130.png" alt="A thumbnail image" width="1000" height="auto">

#### ZIGBEE PROTOCOL VARIOUS TYPES:

1) **Zigbee Coordinator**: This device starts the network and usually acts as the bridge between the Zigbee network and other networks or the internet.

2) **Zigbee Router**: These devices can receive data from other devices and route them to the destination. They can also join additional devices to the network.

3) **Zigbee End Device**: These are typically battery-powered devices that send data to the network but do not route data for other devices. They can communicate directly with the coordinator or routers.

# ZIGBEE DIRECT

- updated version of Zigbee *`combination of zigbee and low energy bluetooth`*
- direct using a smart phone or other device without needing a hub

<img src="https://dsr-iot.com/static/f5b78c255f6e4b8a3ce640085d68d407/zigbee-direct-how-it-works.png" alt="A thumbnail image" width="1000" height="auto">

### *why Zigbee direct* ?
 - bluetooth low energy - universal onboarding devices
 - many don't have Zigbee radio
 - convenient
 - user-friendy
 - no hub
 - no IP
 - **connect Zigbee device with Bluetooth devices**

| Audience         | Goals                                    |
|------------------|------------------------------------------|
| **For Developers** | - Reduce system complexity                |
|                   | - Simplify design and development        |
| **For Installers** | - Manage installations efficiently       |
|                   | - Reduce chances of errors               |
| **For Consumers** | - Ensure ease of use                     |

#### OVERVIEW / TERMINOLOGY

`ZIGBEE DIRECT DEVICE` **ZDD** - light bulb, air conditioner

`ZIGBEE VIRTUAL DEVICE` **ZVD** - phone, smart speaker, PCs

- ZDD & ZVD establish a secure connection
- communication : Bluetooth Low Energy
- ZVD send command to ZDD

#### ZIGBEE BLE

| Feature       | Description                                                  |
|---------------|--------------------------------------------------------------|
| **Security**  | - Authentication and encryption of BLE communications        |
|               | - Secure pairing mechanisms                                   |
|               | - Role-based access control                                  |
|               | - Data integrity and privacy                                 |
|               | - Secure firmware updates                                    |
| **Commissioning** | - Easy setup and configuration of BLE devices             |
|               | - Provisioning and management of network credentials         |
|               | - Integration with mobile apps for user-friendly setup      |
| **Tunneling** | - Encapsulation of BLE traffic over IP networks             |
|               | - Tunneling protocols (e.g., TCP, UDP) support               |
|               | - Ensuring reliable and secure data transmission            |
|               | - Compatibility with IoT gateways and cloud services         |

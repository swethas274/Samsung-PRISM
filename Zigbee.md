# ZIGBEE AND BLUETOOTH

| S. No. | Bluetooth                                                                                             | Zigbee                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| 1.     | Managed by Bluetooth SIG.                                                                             | Managed by Zigbee Alliance and standardized by IEEE.                                        |
| 2.     | Frequency range: 2.4 GHz to 2.483 GHz.                                                                | Frequency range: 2.4 GHz worldwide.                                                         |
| 3.     | Seventy-nine RF channels.                                                                             | Sixteen RF channels.                                                                        |
| 4.     | Uses [GFSK](#modulation) modulation.                                                                 | Uses [BPSK](#modulation) and [QPSK](#modulation) modulation.                                                              |
| 5.     | Maximum of 8 cell nodes.                                                                              | Over 65,000 cell nodes.                                                                     |
| 6.     | Networks: point-to-point master-slave (piconet), can form scatter nets.                               | Networks: star, mesh, cluster with Coordinator, Router, Endpoint nodes.                     |
| 7.     | Requires low bandwidth.                                                                               | Requires low bandwidth, slightly higher than Bluetooth.                                     |
| 8.     | Radio signal range: 10 meters.                                                                        | Radio signal range: 10 to 100 meters.                                                       |
| 9.     | Developed under IEEE 802.15.1.                                                                        | Developed under IEEE 802.15.4.                                                              |
| 10.    | Batteries can be recharged.                                                                           | Batteries last longer but cannot be recharged.                                              |
| 11.    | High data rates, high power for large packets.                                                        | Low data rates, low power for small packets.                                                |
| 12.    | Uses Frequency Hopping Spread Spectrum.                                                               | Uses Direct Spread Spectrum.                                                                |
| 13.    | Network speed up to 250 Mbps.                                                                         | Network speed up to 1 Mbps.                                                                 |
| 14.    | Network join time: about 3 seconds.                                                                   | Network join time: about 30 milliseconds.                                                   |
| 15.    | Protocol stack size: 250K bytes.                                                                      | Protocol stack size: 28K bytes.                                                             |
| 16.    | Used in wireless keyboards, mice, headsets, remote controls, gesture devices.                        | Used in wireless sensor networks, SCADA systems, medical devices, TV remote controls.       |

<a name="modulation"></a>
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


<img src="https://csa-iot.org/wp-content/uploads/2022/04/Zigbee-Devices-New-Feature-Blog-01-768x403.png" alt="A thumbnail image" width="1000" height="auto">

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



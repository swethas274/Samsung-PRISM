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

### ZIGBEE FOR HOME AUTOMATION

<img src="https://csa-iot.org/wp-content/uploads/2022/04/Zigbee-Devices-New-Feature-Blog-01-768x403.png" alt="A thumbnail image" width="1000" height="auto">

- Home Automation is an ideal solution to conserve power.
- Because it easily connect multiple electronic devices in the home and control them remotely.
- Bluetooth, Wi-Fi and Zigbee are few examples of wireless technology
- Due to the Zigbee alliance, most of the smart devices are designed as per the Zigbee Home Automation standard.
- often connected to the Internet, making them able to be remotely controlled.
- `based on EEE 802.15.4 standard`
- low distance communication and consumes less power
- *eg: smart home light switch*
- **The biggest advantage of this protocol is that it uses a mesh network.**
- There are three main types of devices in this technology, i.e. coordinator, routers and end devices
  
1) **Zigbee Coordinator**: central or home network

2) **Zigbee Router**: smart devices fully powered and repeat the signals

3) **Zigbee End Device**: battery-powered devices (out of range) but connected to the network via routers.

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

<img src="https://docs.silabs.com/zigbee-direct/0.1/images/image2.png" alt="A thumbnail image" width="1000" height="auto">
  
**The Zigbee Direct Protocol is composed of three main services:**

- Zigbee Direct Security Service: A mandatory service that establishes a secure BLE connection between the ZVD and ZDD.

- Zigbee Direct Commissioning Service: A mandatory service that enables the ZVD to control certain actions of the ZDD.

- Zigbee Direct Tunnel Service: An optional service that allows the ZVD to send and receive Zigbee Network Packets to and from the ZDD.

**State Diagram showing the ZDD's provisioning**

<img src="https://docs.silabs.com/zigbee-direct/0.1/images/image3.png" alt="A thumbnail image" width="1000" height="auto">

### Open to be Provisioned State
- **BLE Advertisements:** ZDD sends out BLE advertisements.
- **BLE Link Establishment:** ZVD receives advertisements and establishes a BLE link with ZDD.
- **Provisioning Session:** Secure BLE connection established between ZDD and ZVD.
- **Network Configuration:** ZVD configures ZDD with network information for joining the Zigbee network.
- **Timeout Handling:** If no provisioning occurs within the timeout period, ZDD transitions to BLE Interface OFF state.
- **Reactivation Required:** Power-cycling or user interaction needed to reopen the BLE interface and re-enter Open to be Provisioned state.

### Open to Connect ZVD State
- **Network Connection:** ZDD is connected to a Zigbee network.
- **BLE Interface On:** ZDD allows authorized ZVD access to the Zigbee network.
- **Provisioning Session:** Unprovisioned ZVDs can establish a provisioning session with ZDD.

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


## Connecting Zigbee-direct Devices with Bluetooth or Zigbee Devices

### Connecting Zigbee to Zigbee Devices

#### Using a Zigbee Coordinator
- A Zigbee network requires a coordinator that initializes and manages the network.
- Devices are added to the network by putting them in pairing mode and allowing the coordinator to discover and connect to them.
- Software platforms like Zigbee2MQTT or Home Assistant can help manage Zigbee devices through a Zigbee coordinator (e.g., a USB dongle connected to a computer or a standalone hub).

#### Forming a Mesh Network
- Once connected, Zigbee devices can communicate with each other directly or through intermediate devices, forming a mesh network.
- This setup increases range and reliability as each device can act as a repeater.

### Connecting Zigbee to Bluetooth Devices

Directly connecting Zigbee devices to Bluetooth devices is generally not possible due to the differences in their communication protocols. However, there are ways to integrate both types of devices into a cohesive system:

#### Using a Hub/Gateway
- A hub or gateway that supports both Zigbee and Bluetooth can bridge the communication gap between the two protocols.
- Examples include smart home hubs like Samsung SmartThings, which can connect to and control both Zigbee and Bluetooth devices.
- The hub acts as an intermediary, translating commands and data between Zigbee and Bluetooth devices.

#### Using a Software Platform
- Platforms like Home Assistant, OpenHAB, or Domoticz can integrate multiple protocols.
- These platforms run on a computer or a Raspberry Pi and use USB dongles or built-in radios to connect to Zigbee and Bluetooth devices.
- Automation scripts and routines can be set up to create interactions between Zigbee and Bluetooth devices (e.g., a Bluetooth button press turning on a Zigbee light).

#### Custom Solutions
- In some cases, custom hardware or software solutions may be necessary.
- For example, a microcontroller (like an ESP32) with both Zigbee and Bluetooth capabilities can be programmed to act as a bridge between the two protocols.

### Steps to Connect Using a Hub

1. **Set Up the Hub**
   - Connect and configure the hub according to the manufacturer's instructions.
   - Ensure the hub supports both Zigbee and Bluetooth.

2. **Add Zigbee Devices**
   - Put the Zigbee devices in pairing mode.
   - Use the hub's app or interface to discover and add the Zigbee devices to the network.

3. **Add Bluetooth Devices**
   - Put the Bluetooth devices in pairing mode.
   - Use the hub's app or interface to discover and add the Bluetooth devices.

4. **Create Automations**
   - Use the hub’s app or interface to set up automations and interactions between Zigbee and Bluetooth devices.
   - For example, create a rule where a Bluetooth sensor triggers a Zigbee light.

### Conclusion

While Zigbee and Bluetooth operate on different protocols, integrating them into a unified system is possible through the use of hubs or gateways, software platforms, or custom solutions. By understanding the capabilities and limitations of each protocol, you can effectively connect and manage a diverse set of devices in your home or industrial setup.


#### REFERENCES

- https://www.linkedin.com/pulse/how-use-zigbee-home-automation-mvavaindustrialco-ltd-/
- https://docs.silabs.com/d/zigbee-direct/0.1/

# 🌐 4.6 Wireless Media

**Cisco Networking Academy | Solent University**

**Course:** CCNA: Introduction to Networks  
**Module:** 04 - Physical Layer  
**Focus Area:** Wireless Transmission, Wireless Technologies and Wireless LANs

## 🎯 Objective

Understand how wireless media transmit data using electromagnetic waves, identify common wireless technologies, and explain the components, advantages and limitations of wireless LANs.

## 🧠 4.6.1 Properties of Wireless Media

**Wireless media** transmit data through electromagnetic waves, without requiring physical cables between communicating devices.

Wireless signals travel through the air using radio frequencies (RF) or other electromagnetic frequencies.

### Advantages

- Supports mobility, allowing devices to remain connected while moving.
- Allows devices to connect without dedicated physical cabling.
- Provides flexibility where installing cables is difficult or expensive.

### Limitations

- **Coverage area:** Signal strength decreases with distance and can be affected by obstacles (certain construction materials used in buildings and structures).
- **Interference:** Other wireless devices and electrical equipment (like microwave ovens) can disrupt signals.
- **Shared medium:** The wireless medium is shared amongst all wireless users. When multiple devices use it simultaneously, the available throughput for each device may decrease.
- **Security:** Wireless signals can extend beyond physical boundaries, increasing the risk of unauthorised access.

> **NOTE:** Wireless networks are generally more susceptible to interference and environmental conditions than wired networks.
> **NOTE:** Although wireless is increasing in popularity for desktop connectivity, copper and fibre are the most popular physical layer media for connecting intermediary network devices, such as router and switches.

## 🧠 4.6.2 Types of Wireless Media

The IEEE and telecommunications industry standards for wireless data communications cover both the data link and physical layers.

In each of these standards, the specifications include areas like: 
- Data to radio signal encoding.
- Frequency and power of transmission.
- Signal reception and decoding requirements.
- Antenna design and construction.

### Common wireless communication technologies include:

#### 1. Wi-Fi (IEEE 802.11)

- Uses radio waves to connect devices within a Wireless Local Area Network (WLAN).
- Commonly operates in the 2.4 GHz and 5 GHz frequency bands, with 6 GHz supported by newer technologies where permitted.
- Uses Carrier Sense Multiple Access/Collision Avoidance (CSMA/CA Protocol) - The wireless NIC must first listen before transmitting to determine if the radio channel is clear.

**Example:** Commonly used in homes, universities, offices and public hotspots.

#### 2. Bluetooth (IEEE 802.15)

- This is a wireless personal area network (WPAN) standard
- Designed for short-range wireless communication (1 to 100m).
- Commonly operates in the 2.4 GHz frequency band.
- It uses a device pairing process to communicate.

**Example:** wireless headphones, keyboards, mice and other personal devices.

#### 3. WiMAX (IEEE 802.16)

- WiMAX (Worldwide Interoperability for Microwave Access)
- Provides wireless Internet over large areas using base stations and compatible WiMAX receivers or modems.
- Designed to connect homes and businesses without wired broadband.
- Supports connections over several kilometres.
- Largely replaced by 4G LTE and 5G cellular networks.

#### 4. Zigbee (IEEE 802.15.4)

- Low-power wireless technology designed for short-range communication, low-data rate and long battery life.
- Commonly used in smart homes, industrial and Internet of Things (IoT) devices for data collection.
- Supports communication between devices using very little energy.

**Example:** Smart lights, temperature sensors and home automation systems.

#### 5. Cellular Broadband

- Uses mobile network infrastructure to provide wireless connectivity over wide geographical areas.
- Includes technologies such as 4G LTE and 5G.
- Commonly used by smartphones, tablets and mobile routers.

#### 6. Satellite Broadband

- Uses communication satellites to provide Internet connectivity.
- Useful in remote locations where terrestrial infrastructure is unavailable.
- Performance and latency depend on the satellite system and orbit.

## 🧠 4.6.3 Wireless LAN

A **Wireless Local Area Network (WLAN)** allows devices to connect to a local network using wireless signals instead of Ethernet cables.

WLANs commonly use **IEEE 802.11 (Wi-Fi)** technology.

### Wireless LAN Components

**Wireless Access Point (AP)**

- Provides wireless connectivity to devices.
- Commonly connects to the wired LAN through an Ethernet cable.
- Bridges traffic between wireless clients and the wired network.

**Wireless Network Interface Card (Wireless NIC)**

- Enables devices to send and receive wireless signals.
- Commonly integrated into laptops, smartphones and tablets.

### Wireless LAN Operation

1. A wireless access point advertises its network using a network name called the **SSID (Service Set Identifier)**.
2. A wireless device discovers the network and requests to connect.
3. The device authenticates as required and associates with the access point.
4. The device exchanges data with the network through wireless signals.

## 📌 Key Concepts to Remember

- **Wireless Media:** Transmit data using electromagnetic waves instead of physical cables.
- **RF (Radio Frequency):** Electromagnetic frequencies used by many wireless technologies.
- **Wi-Fi (IEEE 802.11):** Technology used for wireless LAN communication.
- **Bluetooth:** Short-range wireless communication technology.
- **WLAN:** Local network connecting devices wirelessly.
- **Access Point (AP):** Provides wireless connectivity and commonly connects clients to a wired LAN.
- **Wireless NIC:** Enables a device to communicate wirelessly.
- **SSID:** Identifies a wireless network.
- **CSMA/CA:** Helps reduce transmission collisions on shared wireless channels.

## 🔐 Security Relevance

- **Unauthorised Access:** Wireless signals can extend outside buildings, allowing nearby attackers to attempt network connections.
- **Eavesdropping:** Wireless transmissions can be intercepted, making strong encryption important.
- **Rogue Access Points:** Unauthorised access points can introduce security vulnerabilities.
- **Denial of Service (DoS):** Wireless interference and jamming can disrupt network availability.
- **Preventive Measures:** Use WPA2-AES or WPA3 where supported, strong authentication, secure AP configuration and regular firmware updates.
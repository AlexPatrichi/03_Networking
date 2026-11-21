# Lab 03: Use Wireshark to View Network Traffic

**Network Applications | Solent University**

Course: CCNA: Introduction to Networks  
Platform: Wireshark & Windows Command Prompt
Focus Area: ICMP, IPv4, MAC Addressing & Network Traffic Analysis


## 🎯 Objective

Capture and analyse network traffic using Wireshark to understand how ICMP packets travel between devices on local and remote networks.

Examine source and destination IP addresses, MAC addresses, and the differences between local and remote communication.

## 🧪 Lab Implementation

**Wireshark** is a software protocol analyzer, or "packet sniffer" application, used for network troubleshooting, analysis, security investigations, software and protocol development, and education. 

This lab investigates ICMP traffic to understand how IP packets and Ethernet frames carry information between devices.

### Part 1: Capture and Analyze Local ICMP Data in Wireshark

**Objective:** Capture ICMP Echo Requests and Echo Replies between the PC and the default gateway on the local network.

#### Step 1: Retrieve your PC interface addresses.

Opened Windows Command Prompt and used the `ipconfig /all` command to identify the active network interface and its configuration. 

Identified the following information:

- Active network interface: Wi-Fi
- IPv4 address
- Subnet mask
- Default gateway
- Physical address (MAC address)

> **NOTE:** The PC is connected to the home network through Wi-Fi. 
> The default gateway will be used to test local ICMP traffic before capturing packets sent to a remote network.

#### Step 2: Capture and Analyse Local ICMP Traffic

Opened Wireshark and selected the active Wi-Fi interface to capture network traffic.  
Applied the following display filter: `icmp`  
Used Command Prompt to send ICMP packets to the default gateway: `ping 192.168.1.254`  

> **NOTE:** Wireshark captured ICMP Echo Requests from the PC and Echo Replies from the default gateway. The successful replies confirmed communication between the devices.

#### Step 3: Examine Ethernet and IP Headers

Selected an ICMP Echo Request in Wireshark and examined the following protocol headers:

- **Ethernet II:** Contains the source and destination MAC addresses.
- **Internet Protocol Version 4:** Contains the source and destination IP addresses.
- **Internet Control Message Protocol:** Identifies the Echo Request or Echo Reply.

### Part 2: Capture and Analyse Remote ICMP Data in Wireshark

**Objective:** Investigate ICMP communication with a remote server and compare its IP and MAC addressing with local communication.

#### Step 1: Capture Remote ICMP Traffic

Restarted the packet capture in Wireshark and followed the same steps as **Part 1**, but this time pinged Google's public DNS server: `ping 8.8.8.8`

#### Step 2: Examine and Analyse Remote ICMP Traffic

Selected an ICMP Echo Request and examined its IP and Ethernet headers to identify the destination IP and MAC addresses.

**Observation:**
- **Destination IP:** The final destination - Google's DNS server (`8.8.8.8`).
- **Destination MAC:** The next hop on the local network - The default gateway's MAC address.

Unlike local communication, the IP packet is addressed to the remote server, while the Ethernet frame is addressed to the default gateway.

## 🧰 Tools Used

- Wireshark
- Windows Command Prompt
- `ipconfig /all`
- `ping`
- ICMP display filter
- Home Wi-Fi network

## 🔐 Security Relevance

- Wireshark allows network administrators and security analysts to inspect traffic and investigate connectivity problems.
- ICMP analysis helps identify unreachable devices, packet loss, and network communication issues.
- Examining IP and MAC addresses helps distinguish local communication from traffic routed to other networks.
- Packet captures may contain sensitive network information and should be reviewed before being shared publicly.

## 📌 Lessons Learned

- Learned how to capture and filter ICMP traffic using Wireshark.
- Identified ICMP Echo Requests and Echo Replies.
- Examined Ethernet frames and IP packet headers.
- Verified successful communication with the default gateway.
- Understood how MAC addresses support local delivery while IP addresses identify the source and final destination.
- **Recognised the importance of protecting network information when documenting practical investigations.**
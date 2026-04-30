# *This project has been created as part of the 42 curriculum by ehossain*

## Description
This is the first project in the 42 curriculum that introduces us to the basics of networking. You will learn how to configure IP addresses and connect devices
through a router, and understand the role of a gateway within a network.

In simple terms, it puts you in front of small network scenarios (hosts, switches, routers) where things are intentionally broken, and your job is to fix them by correctly setting:

IP addresses
Subnet masks
Routing tables
Default gateways

Instead of memorizing theory, you learn by debugging connectivity: “Why can’t this machine reach that one?” and then systematically solving it.

The goal is to build a solid intuition for:

How packets move through a network
How routers decide where to send data
How addressing and subnetting define communication boundaries

## Instructions
Firstly, download the project from the intra. Extract it and you will find an executable program called `run.sh`.
Check if you have permission to run `run.sh`, else do `chmod +x run.sh`
Run the program and it will open a tab in your default browser(Chrome-based browser is preferred).

### How to export configurations??
Once you have validated a level, you will find a button in the header section called `get my config`. You can get your `.json` file by downloading. 

### Submission requirements
If you have finished all the levels, you will have 10 `.json` file 
Please, all the 10 exported configuration files `.json` (one per level).
They must be placed at the repository root.

## What is a Network and Networking?
A Network is a collection of interconnected devices (such as computers, servers, smartphones, printers, etc.) via cables (Ethernet cables) or wireless signals (wi-fi). Networking refers to the practice of connecting multiple devices so that they can communicate with each other and share resources such as files, data, documents, etc. A network can be as small as two devices connected directly or as large as the global internet. Devices within a network communicate using Protocols, which are a set of rules that define how data is transmitted and received between devices on a network, allowing them to communicate effectively. It ensures that the devices can exchange resources and information regardless of their different hardware or software.

## Types of Networks: 
Networking can be classified based on the size and scope of the network, as well as the underlying technology. Here are some common types of networks:

- Local Area Network (LAN)
- Wireless Local Area Network (WLAN) 
- Wide Area Network (WAN)
- Metropolitan Area Network (MAN)
- Personal Area Network (PAN)

## Key Networking Concept

### IP Addressing:
Every device connected to a network must have a unique identifier called IP(Internet Protocol) address. This allows data to be routed safely to the correct destination.

There are 2 types of IP addresses:

1. IPv4 : The most common used version consists of 4 sets of number separeted by dots (.) like (198.168.0.1). Each of these 4 parts can go from 0 to 255. 
    - The reason each number can only reach up to 255 is that each of the numbers is really an eight-digit binary number (sometimes called an octet). In an octet, the number zero would be 00000000, while the number 255 would be 11111111, the maximum number the octet can reach. That IP address we mentioned before (192.168.1.34) in binary would look like this: 11000000.10101000.00000000.00000001.
2. IPv6 : A newer version designed to replace IPv4, with a larger address space to accommodate more devices (2001:0db8:85a3:0000:0000:8a2e:0370:7334). 
    - [IPv6 address explained](https://itintrail.com/2025/04/20/ipv6-address-structure-explained/)

### Subnetting:
Subnetting is the process of dividing a larger network into smaller sub-networks (subnets). This is done to improve network management, reduce traffic congestion, and enhance security by isolating certain parts of the network.

### Media Access Control (MAC) Address:
A MAC (Media Access Control) address is a unique identifier assigned to a network interface controller (NIC) for communication within a physical network. Unlike IP addresses, MAC addresses are fixed and embedded into the hardware.

### Domain Name System (DNS):
The Domain Name System (DNS) is a system that translates human-readable domain names (like www.example.com) into IP addresses that computers use to identify each other. Without DNS, users would have to memorize IP addresses to visit websites.

### Protocols:
Networking relies on protocols, which are rules that control how data is transmitted between devices. Commonly used protocols:

1. TCP/IP (Transmission Control Protocol/Internet Protocol): The backbone protocol of the Internet, responsible for routing data packets between devices.
2. HTTP/HTTPS (Hypertext Transfer Protocol/Secure): The protocol used to transfer web pages and other content over the internet.
3. FTP (File Transfer Protocol): Used for transferring files between a client and server on a network.

## The OSI and TCP/IP Models
The OSI(Open System Interconnection) is an 7 layer framework that standardizes how data is transmitted over the network. The TCP/IP (Transmission Control Protocol/Internet Protocol) is 4 layer framework that is more practical and widely used today for internet communication.

### The OSI Model:
1. Physical Layer: Deals with the physical medium of communication, such as Ethernet cables and wifi signals. 
2. Data Link Layer: Handles data transfer between directly connected devices and error detection. 
3. Network Layer: Responsible for routing data packets between devices. Here, the IP addressing occurs.
4. Transport Layer: Ensures reliable 192.172.250.0data transfer, often using TCP for error correction.
5. Session Layer: Manages sessions between applications.
6. Presentation Layer: Converts data into a format that can be used by the application layer (data encoding, encryption).
7. Application Layer: The top layer where user applications interact with the network (e.g., web browsers, email clients).

### The TCP/IP Model:
1. Network Interface Layer: Combines the physical and data link layers of the OSI.
2. Internet Layer: Manages logical addressing and routing (equivalent to the network layer in OSI).
3. Transport Layer: Ensures reliable data transfer.
4. Application Layer: Includes all protocols that users interact with, such as HTTPS, FTP, and SMTP.

### How data flows through a network
When you send a message, such as an email or a web request, the data follows a specific path through the network, passing through the OSI or TCP/IP layers:

1. Encapsulation: The data is broken down into smaller packets and passed through each layer of the OSI or TCP/IP model, where each layer adds its own header information.
2. Transmission: The data is transmitted over the physical network (e.g., Ethernet, Wi-Fi) to the destination device.
3. Decapsulation: On the receiving end, each layer removes its corresponding header as the data moves back up the model until the original message is reconstructed and delivered to the intended application.

### IP Address
An IP address contains 2 parts:
1. Network identifier.
2. Host Part.

### Subnet Musk
In order to identify which part of the full IP Address corresponds to the
Network and which corresponds to the Host, we must apply to it a Network
Mask (or Subnet Mask).
A Mask is also a 32-bit number divided into four 8-bit blocks. However, its
purpose is to identify which bits are actively part of the Network
identification. To do so, it marks with 1s the network bits.

### 2 IP address can never be used
#### 1st Network Address
This is the first IP address of the network.
- It represents the network itself, not a device.
- It is used by the routers to identify the network.

#### 2nd the Broadcast Address
This is the last IP of the network
- It is used to send a message to ALL devices in the network
- cannot assign to a single machine

some note:
A subnet (subnetwork) is just a smaller piece of a big network.
A subnet mask is the one that tells which part of the IP is the network and which part is the devices, like a separator.

example:
If my IP is `192.172.250.0` and my subnet mask is `255.255.255.0`
My subnet (subnetwork) is `192.172.250.0` and the mask will tell me that `192.172.250` is the part of my network part and `0` is the part of my host part.

In this scenario, my network address will be `192.172.250.0` 
and my broadcast address will be `192.172.250.255` 


---
## References
All the files inside the `./References` folder and some links are provided below.

1. [Introduction to Subnetting](https://www.geeksforgeeks.org/computer-networks/introduction-to-subnetting/)
2. [Introduction to basic networking](https://medium.com/infosecmatrix/what-is-networking-an-introduction-to-basic-networking-concepts-42fdb9c02a20)
3. [Introduction to Ip-addressing and Subnetting](https://www.techtarget.com/searchnetworking/tip/Introduction-to-IP-addressing-and-subnetting)
4. [Free CCNA 200-301 NetworkChuck](https://www.youtube.com/playlist?list=PLIhvC56v63IJVXv0GJcl9vO5Z6znCVb1P)
5. [What is a Default gateway](https://www.cbtnuggets.com/blog/technology/networking/what-is-default-gateway)
6. [What is a router/cisco?](https://www.cisco.com/site/us/en/learn/topics/small-business/what-is-a-router.html)
7. [What is a router/cloudflare?](https://www.cloudflare.com/learning/network-layer/what-is-a-router/)
8. [What is a network switch? | Switch vs. router](https://www.cloudflare.com/learning/network-layer/what-is-a-network-switch/)
9. [What is the OSI Model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
10. [What is the Internet Protocol?](https://www.cloudflare.com/learning/network-layer/internet-protocol/)
11. [TCP/IP: What It Is & How It Works](https://www.splunk.com/en_us/blog/learn/tcp-ip.html)

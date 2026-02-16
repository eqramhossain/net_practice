## What is a Network and Networking ?
A Network is a collection of interconnected devices (such as computer, servers, smartphones, printers etc.) via cables (ethernet cables) or wireless signals (wi-fi). Networking referes to the practice of connecting multiple devices so that they can communicate with each other and share resources such as files, data, documents etc. A network can be as small as two devices connected directly or as large as the global internet. Devices withing a network communicate using Protocols, which are set of rules that defines how data is transmitted and received between devices on a network, allowing them to communicate effectively. It ensures that the devices can exchange the resources and information regradless of their different hardware or software.

## Types of Networks: 
Networking can be classified based on the size and scope of the network, as well as the underlying technology. Here are some common types of networks:

- Local Area Network (LAN)
- Wireless Local Area Network (WLAN) 
- Wide Area Network (WAN)
- Metropolitan Area Network (MAN)
- Personal Area Network (PAN)

## Key Networking Concept

### Ip Addressing:
Every Devices connected to a network must have a unique identifier called IP(Internet Protocol) address. This allows data to routed safely to the correct destination.

There are 2 types of IP address:

1. IPv4 : The most common used version consists of 4 sets of number separeted by dots (.) like (198.168.0.1). Each of this 4 parts can go form 0 to 255. 
    - The reason each number can only reach up to 255 is that each of the numbers is really an eight digit binary number (sometimes called an octet). In an octet, the number zero would be 00000000, while the number 255 would be 11111111, the maximum number the octet can reach. That IP address we mentioned before (192.168.1.34) in binary would look like this: 11000000.10101000.00000000.00000001.
2. IPv6 : A newer version designed to replace IPv4, with a larger address space to accommodate more devices (2001:0db8:85a3:0000:0000:8a2e:0370:7334). 
    - [IPv6 address explained](https://itintrail.com/2025/04/20/ipv6-address-structure-explained/)

### Subnetting:
Subnetting is the process of dividing a larger network into smaller sub-networks (subnets). This is done to improve network management, reduce traffic congestion, and enhance security by isolating certain parts of the network.

### Media Access Control (MAC) Address:
A MAC (Media Access Control) address is a unique identifier assigned to a network interface controller (NIC) for communication within a physical network. Unlike IP addresses, MAC addresses are fixed and embedded into the hardware.

### Domaine Name System (DNS):
The Domain Name System (DNS) is a system that translates human-readable domain names (like www.example.com) into IP addresses that computers use to identify each other. Without DNS, users would have to memorize IP addresses to visit websites.

### Protocols:
Networking relies on protocols which are rules that control how data is transmitted between divices. Commnly used protocols:

1. TCP/IP (Tranmission Control Protocol/Internet Protocol): The backbone protocol of the internet, responsible for routing data packets between devices.
2. HTTP/HTTPS (Hypertext Transfer Protocol/Secure): The protocol used to transfer web pages and other content over the internet.
3. FTP (File Transfer Protocol): Used for transferring files between a client and server on a network.

## The OSI and TCP/IP Models
The OSI(Open System Interconnection) is an 7 layer framework that standerdizes how data is transmitted over the network. The TCP/IP (Tranmission Control Protocol/Internet Protocol) is 4 layer framework that is more practical and widly used today for internet communication.

### The OSI Model:
1. Physical Layer: Deals with the physical medium of communication, such as ethernet cables and wifi signals.
2. Data Link Layer: Handle data transfer between directly connected devices and error detection.
3. Network Layer: Responsible for routing data packets between devices. Here the ip addressing occurs.
4. Transport Layer: Ensures reliable data transfer, often using TCP for error correction.
5. Session Layer: Manages sessions between application.
6. Presentation Layer: Converts data into a format that can be used by the application layer (data encoding, encryption).
7. Application Layer: The top layer where user applications interact with the network (e.g., web browsers, email clients).

### The TCP/IP Model:
1. Network Interface Layer: Combines the physical and data link layers of OSI.
2. Internet Layer: Manages logical addressing and routing (equivalent to the network layer in OSI).
3. Transport Layer: Ensures reliable data transfer.
4. Application Layer: Includes all protocols that users interact with, such as HTTPS, FTP, and SMTP.

### How data flows through a network
When you send a message, such as an email or a web request, the data follows a specific path through the network, passing through the OSI or TCP/IP layers:

1. Encapsulation: The data is broken down into smaller packets and passed through each layer of the OSI or TCP/IP model, where each layer adds its own header information.
2. Transmission: The data is transmitted over the physical network (e.g., Ethernet, Wi-Fi) to the destination device.
3. Decapsulation: On the receiving end, each layer removes its corresponding header as the data moves back up the model until the original message is reconstructed and delivered to the intended application.

---
# References
1. [Introduction to Subnetting](https://www.geeksforgeeks.org/computer-networks/introduction-to-subnetting/)
2. [Introduction to basic networking](https://medium.com/infosecmatrix/what-is-networking-an-introduction-to-basic-networking-concepts-42fdb9c02a20)
3. [Introduction to Ip-addressing and Subnetting](https://www.techtarget.com/searchnetworking/tip/Introduction-to-IP-addressing-and-subnetting)

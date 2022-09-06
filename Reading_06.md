Dean Weiss <br>
6 Sept 2022
<br>
<br>
# OSI Model Layer 2 and 3
<br>
Open Systems Interconnection (OSI) model is a series of layers through which computer systems use to communicate.
<br>
The OSI model has seven layers:
<ol>
  <li>Physical</li>
  <li>Data Link</li>
  <li>Network</li>
  <li>Transport</li>
  <li>Session</li>
  <li>Presentation</li>
  <li>Application</li>
</ol>
<br>
 ## Layer 2; Data Link
Layer 2 is split into two parts: Medac Access Controll (MAC) sub layer and the data link sub layer. 
<br>
### MAC Sub Layer
The MAC Address, also known as the Physical Address, is a serial number permanetly attached to a device. It is an effective way to route traffic between small communities. This is handled by layer 2 switches. A MAC Address consists of a series of 12 hexidecimal numbers. The first six are useful in identifying the manufacturer of the network interface card (NIC). The last six are assigned by the manufacturer to provide a unique address. This makes it so that two devices don't have the same MAC on the same network.
<br>
### Data Link Sub Layer
Establish protocols that relate to the structure of data frames that are placed on the network for data transmission. 

"Each frame includes the MAC address of the source of the frame and the MAC address of the intended recipient. When a device sends a packet to the broadcast MAC address (FF:FF:FF:FF:FF:FF), it is delivered to all stations on the local network.

In the early days of networks, MAC addressing worked well, with only a few computing devices on a single flat network. Because of this, it was unnecessary to extend the network past its limited physical boundaries. Through a process associated with linking a computing device name to its MAC address, either by way of a table or through broadcast protocols like Microsoft’s NetBEUI, devices were able to effectively communicate.

However, as networks grew, network traffic grew and traffic congestion became problematic. As a consequence, a second layer of addressing designed to facilitate connecting two or more networks together became necessary to deal with both traffic congestion and latency issues. Thus, the data link sub layer was born." - https://www.comptia.org/blog/layers-2-and-3-osi-model

## Layer 3; Network
Provides structure relating to how data can be efficiently transferred from one network to aother.
<br>
At layer 3 we use TCP/IP suite of protocols to communicate across the network. We create a envelope over the layer 2 frame that has a layer 3 address of sender and recipient on it. Once it's determined that the recipients address is outside of the senders network address the packets are sent to the router for handling.
<br>
Ip Address: 172.16.1.12
Network: 172.16.
Subnet: 1.
Hoste: 12

## What I want to Know More About

How much more complicated is IPv6 to IPv4 when it comes to layer 3?










source: https://www.comptia.org/blog/layers-2-and-3-osi-model

Dean Weiss <br>
14 Sept 2022

# How To Capture Network Traffic? SPAN vs TAP

Port Mirroring, also known as SPAN or roving analysis, is a method of monitoring network traffic which forwards a copy of each incoming and/or outgoing packet from one (or several) port(s) (or VLAN) of a switch to another port where the analysis device is connected. Port mirroring can be managed locally or remotely.

Port mirroring is the most commonly used solution for capturing traffic because it is inexpensive, flexible in terms of how much traffic can be captured at once, and remotely configurabl

Drawbacks: Can consume significant CPU resources, a risk of not receiving some packets, traffic congestion at the switch level can cause port mirroring to drop some traffic, better solution for long-term monitoring may be a passive TAP or hub.

Advantages of port mirroring
<ul>
  <li> Low cost (this feature is embedded in most switches) </li> 
  <li> Can be configured remotely through IP or Console port </li>
  <li> The only way to capture intra-switch traffic </li>
  <li> A good way to capture traffic on several ports at once </li>
</ul>
Drawbacks of port mirroring
<ul>
  <li> Not adequate for fully utilized full-duplex links (packets may be dropped) </li>
  <li> Filters out physical errors </li>
  <li> Impact on the switch’s CPU </li>
  <li> Can alter the timing of the frame (with an impact on response time analysis) </li>
  <li> SPAN has a lesser priority than port to port data transfer </li>
</ul>
How to capture network traffic: Network TAP
A network TAP (Terminal Access Point) is a hardware device which can passively capture traffic on a network. It is commonly used to monitor the traffic between two points in the network. If the network between these two points consists of a physical cable, a network TAP may be the best way to capture traffic.

The network TAP has at least three ports: an A port, a B port, and a monitor port. To place a tap between points A and B, the network cable between point A and point B is replaced with a pair of cables, one going to the TAP’s A port, the other one going to the TAP’s B port. The TAP passes all traffic between the two network points, so they are still connected to each other. The TAP also copies the traffic to its monitor port, thus enabling an analysis device to listen.

Network TAPs are commonly used by monitoring and collection devices such as APS. TAPs can also be used in security applications because they are non-obtrusive, are not detectable on the network, can deal with full-duplex and non-shared networks, and will usually pass-through traffic even if the tap stops working or loses power.

Advantages of TAPs
<ul>
No risk of dropped packets </li>
Monitoring of all packets (including hardware errors (MAC & media)) </li>
Provides full visibility, including congestion situations </li>
</ul>
Drawbacks of TAPs
<ul>
<li> The device may require two listening interfaces on the analysis device </li>
<li> Costly </li>
<li> No visibility on intra-switch traffic </li>
<li> Not appropriate for the observation of a narrow traffic range </li>
</ul>



source: https://accedian.com/blog/capture-network-traffic-span-vs-tap/

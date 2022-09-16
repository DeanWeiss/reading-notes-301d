Dean Weiss <br>
16 Sept 2022

# What is a Port Scanner and How Does it Work?
<p> A port scanner is a computer program that checks network ports for one of three possible statuses - open, closed, or filtered. </P

<p> Attackers can also use port scanners to detect possible access points for infiltration and to identify what kinds of devices you are running on the network, like firewalls, proxy servers or VPN servers. A port scanner sends a network request to connect to a specific TCP or UDP port on a computer and records the response. It essentially sends a packet  of network data to a port to check the current status. To check if your web server was operating correctly, you would check the status of port 80. </P>

## What is a Port?
<p> A port is a virtual location where networking communication starts and ends. There are two kinds of ports on each computer. 65,536 each for a toal of 131,082 network ports. TCP and UDP. Each computer has an IP address, which is how the network knows which computer to send packets to. If you send a packet to the IP address, the computer knows what port to route this packet to based on the application or packet contents. Each service running on a computer needs to 'listen' on a designated port.</P>
<p> The first 1023 TCP ports are the well-known ports reserved for applications like FTP(21), HTTP(80) or SSH(22) and the Internet Assigned Numbers Authority (IANA) reserves these points to keep them standardized. TCP ports 1024-49151 are available for use by service or applications, and you can register them with IANA, so they are considered semi-reserved. Ports 49152 and higher are free to use.</p>
## Port Scanner Basics.
<p> A port scanner sends a TCP or UDP network packet and asks the port about their current status. There are three options.</p>
<ol>
  <li> Open, Accepted: The computer responds and asks if there is anything it can do for you. </li>
  <li> Closed, Not Listening: The computer responds that the port is not open at this time. </li>
  <li> Filtered, Dropped, Blocked: The computer doesn't even bother to respond. </li>
</ol>

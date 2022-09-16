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
<br>
<p> Port scanners occur early in the cyber kill chain, during reconnassiance and intrusion. Attackers will use port scans to detect targets with open and unused ports that they can repurpose for infilitration, command and control, and data exfiltration or discover what applications run on that computer to exploit a vulnerability in that application. </p>

## Port Scanning Techniques
<ul>
  <li> Ping Scan: The simplest scan, a ping scan looks for any ICMP replies indicating if a target is alive. </li>
  <li> TCP Half Open: A fast and common scan that requests an ACK packet from a computer. Also called a SYN scan. </li>
  <li> TCP Connect: Similiar to the TCP Half Open scan, but the TCP Connect scan completes the TCP connection.</li>
  <li> UDP: Slower than a TCP scan, a UDP scan works best when you send a specific payload to a target, such as a DNS request.</li>
  <li> Stealth Scanning: Quiet and unobvious, stealth scanning is commonly used by hackers for this reason.</li>
  <li> TCP ACK scan: To map firewall rulesets.</li>
  <li> TCP Window Scan: Can differentiate open ports from closed ports but only works on a minority of systems.</li>
  <li> -scanflags: For the advanced user that wants to send their custom TCP flags in a scan, you can do that in Nmap.</li>
</ul>

<p> Some available tools for port scanning; Nmap, Solarwinds Port Scanner, Netcat, Advanced Port Scanner, NetScan Tools. </p>

## How to Detect a Port Scan
<p> You can use a dedicated port scan detector software application, like PortSentry or Scanlogd.  Netcat includes port scanning functionality as well as the ability to create a simple chat server or program different packets for testing purposes. 

Intrusion Detection Systems (IDS) are another way to detect port scans. You need one that uses a wide variety of rules to detect various kinds of port scans that aren't merely threshold-based.
</p>






source: https://www.varonis.com/blog/port-scanning-techniques

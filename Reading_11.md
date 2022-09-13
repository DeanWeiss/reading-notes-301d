Dean Weiss<br>
13 Sept 2022

# Network Address Translation (NAT)
The idea of NAT is to allow multiple devices access too to the internet through a single public address. To do this all private IP addresses must be translated into public ip addresses. It also masks the port number. NAT generally operates on a router or firewall.
<br>
If NAT runs out of addresses the packet will be dropped and an Internet Control Message Protocol(ICMP) host unreachable packet to the destination is sent.
<br>
If the ports are not also masked then if a destination port receieves a request from two different sources at the same time from the same port number, it won't know which port it received it from. 
<br>
Inside local address – An IP address that is assigned to a host on the Inside (local) network. The address is probably not an IP address assigned by the service provider i.e., these are private IP addresses. This is the inside host seen from the inside network. 
<br>
Inside global address – IP address that represents one or more inside local IP addresses to the outside world. This is the inside host as seen from the outside network. 
<br>
Outside local address – This is the actual IP address of the destination host in the local network after translation. 

<ol>
<li> Outside global address – This is the outside host as seen from the outside network. It is the IP address of the outside destination host before translation. 
Static NAT – In this, a single unregistered (Private) IP address is mapped with a legally registered (Public) IP address i.e one-to-one mapping between local and global addresses. This is generally used for Web hosting. These are not used in organizations as there are many devices that will need Internet access and to provide Internet access, a public IP address is needed. Suppose, if there are 3000 devices that need access to the Internet, the organization has to buy 3000 public addresses that will be very costly. </li>
 
<li> Dynamic NAT – In this type of NAT, an unregistered IP address is translated into a registered (Public) IP address from a pool of public IP addresses. If the IP address of the pool is not free, then the packet will be dropped as only a fixed number of private IP addresses can be translated to public addresses. 
Suppose, if there is a pool of 2 public IP addresses then only 2 private IP addresses can be translated at a given time. If 3rd private IP address wants to access the Internet then the packet will be dropped therefore many private IP addresses are mapped to a pool of public IP addresses. NAT is used when the number of users who want to access the Internet is fixed. This is also very costly as the organization has to buy many global IP addresses to make a pool. </li>
 

<li> Port Address Translation (PAT) – This is also known as NAT overload. In this, many local (private) IP addresses can be translated to a single registered IP address. Port numbers are used to distinguish the traffic i.e., which traffic belongs to which IP address. This is most frequently used as it is cost-effective as thousands of users can be connected to the Internet by using only one real global (public) IP address. </li>
</ol>

  <bold>Advantages of NAT – </bold>
<ul> 
  <li> NAT conserves legally registered IP addresses. </li>
 
  <li> It provides privacy as the device’s IP address, sending and receiving the traffic, will be hidden. </li>
 
  <li> Eliminates address renumbering when a network evolves. </li>
</ul>

  <bold>Disadvantage of NAT – </bold>
<ul> 
  <li> Translation results in switching path delays. </li>
 
  <li> Certain applications will not function while NAT is enabled. </li>
 
  <li> Complicates tunneling protocols such as IPsec. </li>
  
  <li> Also, the router being a network layer device, should not tamper with port numbers(transport layer) but it has to do so because of NAT. </li>
</ul>
## What I want to know more about

Nothing at this moment in time.

source: https://www.geeksforgeeks.org/network-address-translation-nat/

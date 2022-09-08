Dean Weiss<br>
8 Sept 2022

# VirtualBox Network
<ul>
  <li> Not Attached </li>
  <li> NAT </li>
  <li> NAT Network </li>
  <li> Bridged Adapter </li>
  <li> Internal Network </li>
  <li> Host-Only Adapter </li>
  <li> Generic Driver </li>
</ul>

## Virtual Network Adapters
<p> Each Vbox VM can use up to eight virtual network adapaters, which are called Network Interface Controller(NIC). Four network adapters can be can configured in the VBox GUI. All eight can be configured with the VBoxManage Modifyvm command. VBoxManage is a command line management tool. </p>

## Types of Virtual Network Adapters in VBox.
"A virtual network adapter is a software-emulated physical device. There are six virtual adapter types that can be virtualized by VirtualBox.
<ul>
  <li> <strong>AMD PCnet-PCI II (Am79C970A).</strong> This network adapter is based on AMD chip and can be used in many situations. As for Windows guests, this network adapter can be used for older Windows versions (such as Windows 2000) because newer Windows versions such as Windows 7, 8 and 10 do not contain a built-in driver for this adapter. Originally, the Am79C970A PCI device contained a single chip 10-Mbit controller and the DMA engine was integrated. This network adapter also supports AMD’s Magic Packet technology for remote wake-up.</li>

  <li> <strong>AMD PCnet-FAST III (Am79C973).</strong> This virtualized network adapter is supported by almost all guest operating systems that can run on VirtualBox. GRUB (the boot loader) can use this adapter for network boot. Similarly to the previous network adapter, this one is based AMD chip.
Intel PRO/1000 MT Desktop (82540EM). This adapter works perfectly with Windows Vista and newer Windows versions. The most of Linux distributions support this adapter as well. </li>

  <li> <strong>Intel PRO/1000 T Server (82543GC).</strong> Windows XP recognizes this adapter without installing additional drivers.</li>

  <li> <strong>Intel PRO/1000 MT Server (82545EM).</strong> This adapter model is useful to import OVF templates from other platforms and can facilitate import process. </li>

  <li> <strong>Paravirtualized Network Adapter (virtio-net)</strong> is a special case. Instead of virtualizing networking hardware that is supported by most operating systems, a guest operating system must provide a special software interface for virtualized environments. This approach allows you to avoid the complexity of networking hardware emulating and, as a result, can improve network performance.</li>
</ul>

<br>  

The industry standard virtIO networking drivers are supported by VirtualBox. VirtIO networking drivers are a part of the KVM project and are open-source. These drivers are available for Linux with kernel 2.6.25 or later, and Windows including older versions such as Windows 2000, XP and Vista.
  
#### Jumbo frames support
VirtualBox provides limited support for jumbo frames (Ethernet frames that can carry packets which size is more than 1,500 bytes). If you need to use jumbo frames, select an Intel virtualized network adapter, and configure that adapter to work in bridged mode. AMD-based virtual networks adapters don’t support jumbo frames. If you try to enable jumbo frames for AMD-based virtual network adapters, jumbo frames will be dropped silently for input and output traffic. Jumbo frames are disabled by default." - https://www.nakivo.com/blog/virtualbox-network-setting-guide/

## VirtualBox Network Modes
<strong>Not Attached -</strong> A virtual network is installed but noot connected. Similiar to having the ethernet cable unplugged from a physical network adapter. 

<strong>NAT-</strong> The default setting byr virtual network adapters. Best used for Guests, they can use it for internet access. A guest machine is not accessible from a host machine, or from other machines in the network when the NAT is in use.

<strong>NAT Network-</strong> NAT Network mode can allow several virtual machines to communicate with each other via the network. External machines outside the physical network cannot access the VM's. 

<strong>Bridged Apadter-</strong> Used for connecting the virtual network of a virtual machine to a physical network which a physical netwoork adapter of the the Virtualbox is connected. This cann be used so that you can access a host machine, hosts of the physical and external networks including internet from a VM.

<strong>Internal-</strong> Connected to an isolated virtual network. VM's on this network can connect to each other but not with the Vbox host or anyone else outside the network. 

<strong> Host-Only Adapter-</strong> Used for communicating between a host and guests. A VM can communicate with other VM's connected to the network and with the host machine. The Host can access all VMs connected to the host-only network.

<strong> Generic Drive-</strong> Allows you to share the generic network interface. Two sub-modes are available for VirtualBox Generic Driver mode-

  UDP Tunnel and VDE (Virtual Distributed Ethernet) Networking.

  UDP Tunnel - Virtual machines that run on different hosts can communicate transparently by using an existing network infrastructure.

  VDE Networking - Virtual machines can connect to a virtual distributed switch on Linux or FreeBSD hosts. You need to compile VirtualBox from sources to use VDE networking since standard VirtualBox packages don’t include this feature.



source: https://www.nakivo.com/blog/virtualbox-network-setting-guide/

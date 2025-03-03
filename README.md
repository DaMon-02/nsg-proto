<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- I will create a resource group in Azure that includes two virtual machines: one running Windows 10 and the other running Ubuntu/Linux. Additionally, I will set up a virtual network with subnets. During this process, I'll configure network security groups and firewalls on the virtual machines to manage their interactions. I'll access both virtual machines using Remote Desktop, starting with logging into VM-1. Once logged in, I'll install Wireshark on VM-1 to monitor the network traffic between the two VMs. Using PowerShell, I'll establish communication between the VMs and track the inbound and outbound traffic in Wireshark. I'll initiate a continuous ping from the Windows 10 VM to the Ubuntu VM, then open the NSG for the Ubuntu VM in Azure to disable inbound ICMP traffic, effectively creating a firewall. Finally, I’ll filter and monitor traffic for SSH, DHCP, DNS, and RDP

<h2>Actions and Observations</h2>

![Screenshot 2025-03-03 144524](https://github.com/user-attachments/assets/b8f6711b-3812-4eb8-825d-2b506122cb87)

</p>

<p>
This shows that I created two virtual machines: one running Microsoft Windows Server and the other running Linux (Ubuntu). While creating the first virtual machine with Windows, I allowed it to create a new virtual network and subnet. Later, when creating my Linux server, I selected the resource group associated with the Windows VM to ensure that both virtual machines are using the same virtual network, which will be important later.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

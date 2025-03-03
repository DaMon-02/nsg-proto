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
- Various Network Protocols (SSH & ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- I will create a resource group in Azure that includes two virtual machines: one running Windows 10 and the other running Ubuntu/Linux. Additionally, I will set up a virtual network with subnets. During this process, I'll configure network security groups and firewalls on the virtual machines to manage their interactions. I'll access both virtual machines using Remote Desktop, starting with logging into VM-1. Once logged in, I'll install Wireshark on VM-1 to monitor the network traffic between the two VMs. Using PowerShell, I'll establish communication between the VMs and track the inbound and outbound traffic in Wireshark. I'll initiate a continuous ping from the Windows 10 VM to the Ubuntu VM, then open the NSG for the Ubuntu VM in Azure to disable inbound ICMP traffic, effectively creating a firewall. Finally, I’ll filter and monitor traffic for ICMP & SSH

<h2>Actions and Observations</h2>

![Screenshot 2025-03-03 144524](https://github.com/user-attachments/assets/b8f6711b-3812-4eb8-825d-2b506122cb87)

</p>

<p>
This shows that I created two virtual machines: one running Microsoft Windows Server and the other running Linux (Ubuntu). While creating the first virtual machine with Windows, I allowed it to create a new virtual network and subnet. Later, when creating my Linux server, I selected the resource group associated with the Windows VM to ensure that both virtual machines are using the same virtual network, which will be important later.
</p>
<br />

<p>

![Annotation 2025-03-03 201511](https://github.com/user-attachments/assets/a9d25280-e4d1-4301-b358-e86e126fe84f)




<strong>-Needed!-</strong>
Here I am downloading Wireshark, it is essential for examining network traffic as it captures and analyzes packets, helping to monitor and troubleshoot communication between devices. It provides detailed insights into protocols, packet flow, and potential issues, making it a vital tool for diagnosing network problems and ensuring security.
</p>
<br />

<p>

![icmp traffic](https://github.com/user-attachments/assets/e97e9cfb-de80-45cc-9886-56b6c00549e0)
![Screenshot 2025-03-03 160517](https://github.com/user-attachments/assets/ccc4b744-e254-4112-8b33-e2d15388dc6b)
![Annotation 2025-03-03 211331](https://github.com/user-attachments/assets/b3fbbdba-864f-4b71-bcac-77114e2cacf5)
![Annotation 2025-03-03 213201](https://github.com/user-attachments/assets/b5c167b1-c9a5-4858-b579-50282157ad24)

<p>
I launched PowerShell within the virtual machine to monitor network packets, filtering and analyzing ICMP traffic while focusing on the data flow. Next, I configured the Linux VM's cloud firewall and network security group to block all incoming ping traffic, effectively stopping any further ping requests. In the screenshot, you can see this happening as "Request Timed Out" is repeatedly displayed. Finally, I connected to the Linux VM, filtered for SSH traffic, and observed the continuous flow of SSH traffic across the network.
</p>
<br />

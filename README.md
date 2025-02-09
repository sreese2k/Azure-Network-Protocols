# <p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

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

- Step 1: Setting Up the Azure Virtual Machine
- Step 2: Connecting it to the windows app/Remote Desktop
- Step 3
- Step 4
- Step 5

<h2>Actions and Observations</h2>

<p>
<img src="https://imgur.com/EHvgUgh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>To begin, we created a resource group to deploy a Virtual Machine (VM) in Azure with a public IP address, ensuring that it has appropriate inbound rules to allow connections, such as RDP for Windows (port 3389) or SSH for Linux (port 22). This allows us to access the VM remotely. Once the VM is running, we install Wireshark, a powerful network protocol analyzer, to capture and inspect packets traveling to and from the VM.

</p>
<br />

<p>
<img src="https://imgur.com/4jDFLvN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>Going more in depth, we use a Virtual Machine (VM) to connect to Remote Desktop which lets you access a computer in the cloud from anywhere. First, we create a Windows VM in Azure and make sure Remote Desktop (RDP) is turned on by allowing traffic through port 3389 in the security settings. Then, we find the VM’s public IP address in the Azure portal and use the Remote Desktop Connection (RDC) app on our own computer to connect. After entering the login details, we can control the VM just like a regular computer—opening files, running programs, and managing settings remotely. This is useful for remote work, troubleshooting, and securely accessing cloud resources.

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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

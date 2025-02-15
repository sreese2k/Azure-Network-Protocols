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
- Step 3: Attempt to ping from within the Windows VM using the private IP address of the Linux-VM
- Step 4: Disable ICMP (ping) traffic for a Linux VM and to re-enable it
- Step 5: Obseerve different traffic protocols such as SSH, DHCP, DNS and RDP using PowerShell and Wireshark

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

<p>Going more in depth, we use a Virtual Machine (VM) to connect to Remote Desktop which lets you access a computer in the cloud from anywhere. First, we create a Windows VM in Azure and make sure Remote Desktop (RDP) is turned on by allowing traffic through port 3389 in the security settings. Then, we find the VM’s public IP address in the Azure portal and use the Remote Desktop Connection (RDC) app on our own computer to connect. After entering the login details, we can control the VM just like a regular computer opening files, running programs, and managing settings remotely. This is useful for remote work, troubleshooting, and securely accessing cloud resources.

</p>
<br />

<p>
<img src="https://imgur.com/dzmKrpg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>To retrieve the private IP address of the Ubuntu VM (Linux-vm), we go to the Azure portal, navigate to the VM’s network settings, and note the private IP assigned to it. Then, from the Windows 10 VM, we open PowerShell and use the ping command to test the connection to the Ubuntu VM using its private IP. At the same time, we run Wireshark on the Windows VM to capture and observe the ICMP (ping) requests and replies, confirming that the two VMs can communicate within the same network. Next, we try to ping a public website (like ping google.com) to see how external traffic behaves. If the ping is unsuccessful, it may indicate that outbound ICMP traffic is blocked by Azure’s Network Security Group (NSG) or firewall settings. This experiment helps us understand how network traffic flows between private and public networks in a cloud environment.

</p>
<br />

<p>
<img src="https://imgur.com/tbdmjqQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>To disable ICMP (ping) traffic for a Linux VM, go to its Network Security Group (NSG) in Azure, add an inbound rule to deny ICMP. To reenable it, delete or change the rule to allow ICMP. This controls whether the VM can receive ping requests from other machines.

</p>
<br />

<p>
<img src="https://imgur.com/qOukapZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>And lastly in this project, we worked with SSH, DHCP, DNS, and RDP to understand how they help computers communicate. SSH (Secure Shell) let us securely connect to a Linux VM using the command line. DHCP (Dynamic Host Configuration Protocol) automatically gave IP addresses to our VMs so they could connect to the network. DNS (Domain Name System) translated website names into IP addresses when we accessed online sites. RDP (Remote Desktop Protocol) allowed us to control a Windows VM remotely with a graphical interface. Using Wireshark, we observed how these protocols work by capturing IP assignments, website lookups, and remote connections, giving us a better understanding of cloud networking.

</p>
<br />

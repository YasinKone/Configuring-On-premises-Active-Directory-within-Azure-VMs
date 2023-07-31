<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: create a windows 10 virtual machine for the client and make another virtual machine for the domain controller be sure the image for it is windows server 2022 and it is under the same network. After those are done go to the networking setting on you domain controller via microsoft azure press the network interface, then go to ip configurations, press the line where it says the address is dynamic and then make it static.
- Step 2: Using Remote desktop protocol log into the domain controller and when the server manager appears press roles and features, then press next untill you reach server roles and check active directory domain services and install it then press the flag in the top right corner and promote the server to a domain controller and make the info such as the domain name and user as you like (you will be signed out jsut log back in). When logging back in the new format for your user name is (domainname).com\username
- Step 3: after logging back in go to tools and press active directory users and computers
- Step 4: under your folder with your domain name make some orgainizational units add users via a powershell script, give them permissions, and log into one of the users with the client virtual machine with the same format (domainname).com\username

<h2>Deployment and Configuration Steps</h2>

<p>
![image](https://github.com/YasinKone/Configuring-On-premises-Active-Directory-within-Azure-VMs/assets/98929107/350d4bdf-4199-4553-99f8-47f6f83ff904)

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

<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial guides you on how to deploy active directery using two virtual machines from Microsoft Azure creating a domain controller and client.<br />




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
<img src="https://i.imgur.com/NKbdZCu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
This is where you go to change the IP address to static if you look at the top of the image you can see the steps to take to get there virutal machines, DC-1 (thats what I named my domain controller so basically your domain controller), networking, your NIC, and finally IP configurations
</p>
<br />

<p>
<img src="https://i.imgur.com/etp0sdr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Press roles and features, then press next untill you reach server roles and check active directory domain services and install it then press the flag in the top right corner and promote the server to a domain controller and make the info such as the domain name and user as you like (you will be signed out jsut log back in). When logging back in the new format for your user name is (domainname).com\username
</p>
<br />

<p>
<img src="https://i.imgur.com/MqwfFC0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
under your folder with your domain name make some orgainizational units add users via a powershell script, give them permissions, and log into one of the users with the client virtual machine with the same format (domainname).com\username. As you can see I have made multiple groups Employees, Admins, and a security group that has sccounting in it.
</p>
<br />

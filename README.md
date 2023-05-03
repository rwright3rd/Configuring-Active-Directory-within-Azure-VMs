# Configuring-Active-Directory-within-Azure-VMs
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
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

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory
- Created Users using Powershell

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/E7RhYGg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I signed on to Microsoft Azure and created two virtual machines. The first is a "Client-1" Win 10 VM, which will be used as a "user" account. The second is my domain controler "DC-1" Win Server 22 VM. 
</p>
<br />

<p>
<img src="https://i.imgur.com/Yeenxuh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the virtual machines setup in Azure, I connected to the domain controler (DC-1/ WIN Server 22) VM with remote desktop using the public IP address.
</p>
<br />

<p>
<img src="https://i.imgur.com/QykQM1d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

I then setup a new forest with my new domian. For this example it was "mydomain.com". I then created new organizational units for EMPLOYEES and ADMIN. Active Directory is now setup with EMPLOYEES and ADMIN organizational units. You can now create or adjust password/username settings and policies.
</p>
<br />

<p>
<img src="https://i.imgur.com/9N7biKH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I then opened up Powershell ISE and ran a script to add hundreds of random users (randomly created) to my EMPLOYEES organizational unit in Active Directory.
</p>
<br />

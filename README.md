
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory constructed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Active Directory Domain Services
- Remote desktop
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

- Step 1: Install Active Directory on domain controller
- Step 2: Set up new forest/creating a domain name
- Step 3: Connect general cpu to domain name
- Step 4: Remote desktop on general cpu
- Step 5: Create additional users 

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Prior to installing Active Directory on on the Domain cpu I needed to create two virtural machines in Azure; the domain controllers operating system was Windows Server 2022 and the additional cpu (general cpu's) operating system used Windows 10.  I ensured that the two virtural machines were created on the same Vnet to establish connectivity.  Once that was successful, it was necessary to install Active Directory on the domain cpu. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As pictured above, the next step involved creating a domain name.  This can be created using any _____.com; I chose Palmerinc.com
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the domain name creation, I needed to log onto the general cpu system and connect it to the domain name created.  This process involed accessing Microsoft Azure and changing the general cpu's DNS settings to the domains private IP address.  I would then confirm the general cpu shows up in Active Directory Users and Computers on the domain cpu.  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once there was succusful completion in establishing connection to the domain name, remote desktop was used to ensure that other additonal users are able to log-in on the general cpu.   
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, Powershell was used to randomly generate other default users.  I was able to use a defalt user name created and log into the general cpu using the domain created.    
</p>
<br />

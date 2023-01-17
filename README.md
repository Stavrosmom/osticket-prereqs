# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Resource Group in Azure
- Windows 10 Virtual Machine in Azure
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/usZ0DCk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once a Windows 10 virtual machine has been created in Azure, log in with RDP. Once logged in, right click the start button and select "run". After selecting "run" type "control panel". Enter the Control Panel and select "Programs". 
</p>
<br />

<p>
<img src="https://i.imgur.com/yCD2Cqd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, select "Turn windows features on or off" and look for "Internet Information Services". Turn on "FTP Server", "Web Management Tools", and"World Wide Web Services". Expand "World Wide Web Services" and turn on "CGI". Select "Ok".
</p>
<br />

<p>
<img src="https://i.imgur.com/yIfYFHL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once CGI has been enabled, open click this link for access to the installation files. https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
</p>
<br />

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

- Download this file https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD
- Enable Internet Information Services (IIS)
- Install PHP
- Install MySQL
- Install HeidiSQL
- Install Microsoft Visual C++

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/S27tnyl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Xfq5of8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
Create a virtual machine using Azure. Must have 2 CPUs and 16 GB of RAM. 
</p>
<br />

<p>
</p>
<p>
 <img src="https://i.imgur.com/U8QMvcB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 After creating your VM log onto it and download the file at the start of this tutorial. Once downloaded go to your downloads folder and drag the osticket folder onto your desktop and extract the file. Make sure it goes it the osticket installtion folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/lo6Q8JE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <img src="https://i.imgur.com/sz5rSru.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Once you've completed the last step you'll need to enable IIS with CGI. To do this you'll need to go to the control panel and under programs click uninstall a program then click Turn Windows features on or off and check IIS box. After that you'll need to click World Wide Web Services then click Application Development Features and check the CGI box.
</p>
<br />

 <img src="https://i.imgur.com/zSEMtpl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 Now you need to install PHP to do this you go to the osTicket-Installation-Files click and open PHPManagerForIIS_V1 5.0 msi. After opening click I agree and next.

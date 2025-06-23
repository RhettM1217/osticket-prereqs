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



<img src="https://i.imgur.com/u2sWRxM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Then inside the osTicket-Installation-Files open rewrite_amd64_en-US.msi after that click agree to all the steps.



<img src="https://i.imgur.com/dDyu5KJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Create a directory called C:\PHP.



<img src="https://i.imgur.com/eHTpq8J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Back in the osTicket-Installation-Files click VC_redist.x86.exe and agree to all the terms to download.



<img src="https://i.imgur.com/SRmqQHP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Install MySQL 5.5.62 when you get to the choose setup screen select typical, after installing launch Configuration Wizard. When asked choose Standard Configuration.



<img src="https://i.imgur.com/5GFsP0N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Run IIS as an administrator. Now we have to register PHP in IIS manager to do this open PHP manager and click register new PHP then browse to the PHP folder made in the C drive. Once completed reload IIS.



<img src="https://i.imgur.com/bjQGZmo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Now we need to extract osTicket-v1.15.8.zip from osTicket-Installation-Files into the same location. Once extrated copy the upload folder and paste it inisde the Windows(C:) - inetpub - wwwroot folder and rename it osTicket then restart IIS.



<img src="https://i.imgur.com/RwAexRN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Go to the osTicket folder in IIS and click browse *.80 (http).



<img src="https://i.imgur.com/tnKhq6i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Now we need to make some configurations for osTicket in IIS. To do this go back to IIS and click Default - osTicket - PHP Manager and enable these 3 things  php_imap.dll, php_intl.dll, php_opcache.dll.


<img src="https://i.imgur.com/weGzJUY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Rename ost-sampleconfig.php to ost-config.php to do this go to files in Windows(C:) drive - inetpub - wwwroot - osTicket - include. Then search for the file that needs to be renamed.


<img src="https://i.imgur.com/istYBEg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Open the ost-config.php file and click Properties Security - Advanced - Disable Inheritance - Remove all inherited permissions. Then we have to add permissions to do this click select a principal and in the text box at the bottom type everyone and click ok.


<img src="https://i.imgur.com/vXbsorp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Go back to the osTicket page and click continue. Fill out the first half of the page (admin email and default email must be different).


<img src="https://i.imgur.com/FhzDiMi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vFLGEwt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Back in the osTicket-Installation-Files click HeidiSQL_12.3.0.6589_Setup then click agree and accept all terms to install. click New, username and password is Root.




# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1/  Create A resource group/  name it OsTicket 
- Item 2/  Create a virutal machine 
- Item 3/ Get the Public IP, and open remote desktop. Paste the IP address in the remote desktop screen.
- Item 4/ download the osTicket-Installation-Files.zip 
- Item 5/ Install / Enable IIS in Windows WITH CGI
- Item 6/ Install PHP Manager for IIS 
- Item 7/  Create the directory C:\PHP 
- Item 8/  install VC_redist.x86.exe., 
- Item 9/  install MySQL 5.5.62 (mysql-5.5.62-win32.msi),
- Item 10/ Open IIS as an Admin, go to PHP, and register it , 
- Item 11/ Install osTicket v1.15.8
- Item 12/ Go to sites -> Default -> osTicket
- Item 13/ Note that some extensions are not enabled
- Item 14/ Rename: ost-config.php
- Item 15/ Assign Permissions: ost-config.php
- Item 16/ Continue Setting up osTicket in the browser (click Continue)
- Item 17 Install HeidiSQL.
- Item 18/ Continue Setting up osTicket in the browser

<h2>Installation Steps</h2>

<p>
><img width="1905" height="894" alt="Screenshot 2025-07-30 145248" src="https://github.com/user-attachments/assets/4458d333-e9df-4171-bfb9-d6de584a76a7" />

</p>
<p>
Create A Resource Group in Azure/  name it OsTicket 
</p>
<br />

<p>
 <img width="1902" height="868" alt="Screenshot 2025-07-30 150010" src="https://github.com/user-attachments/assets/830a3cd1-0dd6-4212-af61-926ccbee961e" />

</p>
<p>
 create a virutal machine / Image  windows 10
</p>
<br />

<p>
<img width="944" height="675" alt="Screenshot 2025-07-30 151323" src="https://github.com/user-attachments/assets/a1f55871-1ae6-4661-819a-304003adee7a" />

</p>
<p>
Item 3 - Get the Public IP, and open remote desktop. Paste the IP address in the remote desktop screen.
</p>
<br />
<p><img width="961" height="648" alt="Screenshot 2025-07-30 151512" src="https://github.com/user-attachments/assets/5f0391ff-46c2-4f07-8cb7-e69d77de92a0" />
="https://github.com/user-attachments/assets/a1f55871-1ae6-4661-819a-304003adee7a" />

</p>
<p>
Item 4 download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files, then extract all 
</p>
<br />
<p>
 /><img width="857" height="601" alt="Screenshot 2025-07-30 152336" src="https://github.com/user-attachments/assets/6574855d-ce8a-458c-9360-dfac2443454b" />
<img width="978" height="686" alt="Screenshot 2025-07-30 152655" src="https://github.com/user-attachments/assets/2f98b010-3d3b-4628-a487-474875ac3343" />


</p>
<p>
Item 5- Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI, click the control panel in the search bar, go to uninstall programs under programs,  go to click features on or off, click and expand Internet Information Services, expand World Wide Web Services download CGI
</p>
<br />
<p>
><img width="979" height="685" alt="Screenshot 2025-07-30 153239" src="https://github.com/user-attachments/assets/2d00d9f0-6fe1-451a-8b41-6c6b2be396ed" />


</p>
Item 6 - From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) and install the Rewrite Module
</p>
<br />
<p>
><img width="833" height="633" alt="Screenshot 2025-07-30 153723" src="https://github.com/user-attachments/assets/4679c6d9-2220-4f6c-b4c0-57401beca758" />


</p>
<p>
Item 7 - Create the directory C:\PHP and extract all mhp files into the PHP folder
</p>
<br />
<p>
><img width="967" height="690" alt="Screenshot 2025-07-30 153913" src="https://github.com/user-attachments/assets/db4909b7-f8c4-424a-b978-930cd62bd26d" />


</p>
<p>
Item 8 - From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe., 
</p>
<br />
<p>
<img width="946" height="617" alt="Screenshot 2025-07-30 154348" src="https://github.com/user-attachments/assets/1de79f9b-d64a-475c-9423-7c50e1761c30" />
<img width="894" height="662" alt="Screenshot 2025-07-30 154741" src="https://github.com/user-attachments/assets/dc160856-faf0-47d4-8730-7f4d0547959f" />


</p>
<p>
Item 9 - install MySQL 5.5.62 (mysql-5.5.62-win32.msi), a datebase OsTicjet needs to store date. chppse typical setup 
. Launch it and have the word "root" as the username and password
</p>
<br />
<p>
><img width="991" height="700" alt="Screenshot 2025-07-30 155742" src="https://github.com/user-attachments/assets/55e7f2d6-fb67-43c6-8852-07be5e2e5da0" />


</p>
<p>
Item 10 - Open IIS as an Admin, go to PHP, and register it , 
</p>
<br />
<p>
><img width="988" height="699" alt="Screenshot 2025-07-30 160731" src="https://github.com/user-attachments/assets/35a66979-e368-4bd0-be7b-780b14187e2b" />


</p>
<p>
Item 11- Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br />
<p>
><img width="983" height="694" alt="Screenshot 2025-07-30 161257" src="https://github.com/user-attachments/assets/06ae5559-91c4-4f3c-90bf-a9c29b4a7f1e" />



</p>
<p>
Item 12 Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>
<br />
><img width="981" height="680" alt="Screenshot 2025-07-30 161818" src="https://github.com/user-attachments/assets/d03076a7-48e8-4788-90f8-537bb7db719f" />
<img width="984" height="680" alt="Screenshot 2025-07-30 162000" src="https://github.com/user-attachments/assets/d94150a4-9b07-49ab-bf1a-c9e3cc1cc71a" />


</p>
<p>
Item 13- Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
</p>
<br />
><img width="985" height="681" alt="Screenshot 2025-07-30 162801" src="https://github.com/user-attachments/assets/e5656690-051a-467b-b24f-e99c0ff71913" />


</p>
<p>
Item 14- Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />
><img width="983" height="674" alt="Screenshot 2025-07-30 163011" src="https://github.com/user-attachments/assets/bdb58d66-c427-4dca-a713-253f1d6a5cea" />


</p>
<p>
Item 15- Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
</p>
<br />


</p>
<p>
Item 16- Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
</p>
<br />
><img width="1007" height="696" alt="Screenshot 2025-07-30 164539" src="https://github.com/user-attachments/assets/f31ad2b3-1b5b-410e-9542-5e89f27d585d" />


</p>
<p>
Item 17 - From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”
</p>
<br />
<img width="1002" height="698" alt="Screenshot 2025-07-30 165038" src="https://github.com/user-attachments/assets/edfad61d-b28f-42cb-bfbb-a3752bdaf8af" />


</p>
<p>
Item 18 - Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”

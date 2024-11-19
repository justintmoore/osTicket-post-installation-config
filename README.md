<p align="center">
    <img src="https://i.imgur.com/Clzj7Xs.png" alt=osTicket logo"/>
    
## Technologies Used
- Microsoft Azure <br>
- Remote Desktop <br>
- Internet Information Service


## Operating Systems Used
- Windows 10 <br>
- Windows Server 2022
  
## Definitions
<b>Localhost</b>: is a loopback request represented by the address 127.0.0.1. Localhost is a tool for testing web applications, network testing, and blocking malicious websites. <br>
<br>
<b>Internet Information Services</b>: is a tool that runs on Windows systems that supports various protocols (HTTP, HTTPS, FTP, ect). IIS includes features managing sites, applications  and server performance.


## Prerequisites
<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/c9842e41-8621-45e4-b4ac-e42dae7213a3" height="50%" width="50%" alt="step one"/>
</p>

<p align="center"> In Microsoft Azure, to set up a Virtual Machine: click Virtual Machine -> create -> zone 3 -> Windows 10 -> username and password and then create. I copy the IP address and paste into the remote desktop and log in with the username and password set up. Finally, copy and paste the lab project into browser. The lab project has the files listed that are needed to set up osTicket. </p>
<br>

## Installing files
<p align="center">
    <img src="https://github.com/user-attachments/assets/f0799a35-207d-45f8-9e7e-21fa5686f488" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">After creating a virtual machine in azure and logging in. Download and unzip the osTicket installation files.</p>

<p align="center">
    <img src="https://github.com/user-attachments/assets/1e5dab0f-bf89-43d1-97d4-6a5ff60a2ff2" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Enable IIS in windows by following these steps: control panel -> windows features -> world wide web -> application development features -> CGI. To know this has worked is by doing a loopback address. In the browser type in 127.0.0.1. If you see a blue screen it has worked. If you see an error, then go back through the steps previously.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/b6d885ad-42dc-47fd-8215-d033ac849013"
 height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Install PHP manager and Rewrite Module. </p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/5617ec01-fae2-49cb-92b8-9b0531cc97be" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Go to files -> windows C: and create a directory named C:\PHP. </p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/b31cb80e-e719-4d78-98a0-e2a99d4178b7" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Unzip PHP 7.3.8 into the created directory. </p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/8e7bb78d-377f-4f6f-8f12-9226f15b04a3" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Install VC and MySQl.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/39b08ee7-4aaa-4203-9843-0cbd16b50bc2" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Set up MySQl by selecting Typical Setup -> launch configuration -> Standard Configuration -> type in an username and password.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/273c5dc1-6a08-43b1-9a2a-0f854542775f" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Open IIS as Admin.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/0cabe267-164a-4c5e-a63e-83af30e249c8" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Click on PHP manager and click register. Select php-cig.exe from the C:\PHP folder. And reload IIS.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/52c397b0-b1dd-4b4d-a6ec-f82a66fa5a42" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">In folders, unzip osTicket install files. Copy uploads into c:\inetpub\wwwroot and rename to osTicket.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/766b96b6-2d27-43ac-98e5-8461f86f8b05" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Reload IIS again and right click Browse *:80. This should open osTicket into the browser. If this did not happen then review the previous steps.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/859cf37d-12dd-44f2-a435-86109a8f6bb1" height="50%" width="50%" alt="step one"/>
</p>

<p align="center"> For osTicket to work these extensions should be enabled: php_imap.dll, php_intl.dll, php_opcache.dll. Refresh the browser and the x's shown should be green checks.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/0bc5db5e-b7a0-4481-b5bc-3ff77768298b" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Rename ost-smapleconfig.php to ost-config.php.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/a2fd8fe0-a5be-4e74-b082-0782fd12b591" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Right click ost-config.php, select properties, and select security. Here change permissions to everyone.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/926dfad7-f5d8-491a-9126-6da0832b51da" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">By now you should be on the set up page of osTicket; name, password, and email should be already placed in. In the bottom section will need a database file from Heidi SQL. Install Heidi SQL from the osticket install files folder. Create a new session, log in with the user and password created from MySQL. Connect to the session and create a database osTicket. Once the bottom section is filled out click continue.</p>

<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/b9e886dc-1efa-4ee5-bb1e-c2f0b37c15aa" height="50%" width="50%" alt="step one"/>
</p>

<p align="center">Congrats you have downloaded osTicket. From here you can learn the program and how to resolve tickets and create accounts.</p>





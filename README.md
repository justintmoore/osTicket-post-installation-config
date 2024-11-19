<p align="center">
    <img src="https://i.imgur.com/Clzj7Xs.png" alt=osTicket logo"/>  
    
Sorry about the change in format. As I continue to document my projects, I'm always looking for better ways to enhance my presentations! 
    
## Tools, Utilities, Services Used
- Microsoft Azure <br>
- Remote Desktop <br>
- Internet Information Service


## Environments Used
- Windows 10 <br>
- Windows Server 2022
  

## Program Walkthrough
<p align="center">
    In this lab we are just going to explore the osTicket portal a bit. Make some configurations before we creating and solving mock tickets. There are two main URLs we should be familiar with.
</p>
<br>
<p align="center">
    Admin Page: <a href="http://localhost/osticket/scp/login.php">http://localhost/osticket/scp/login.php</a> and the End User page:<a href="http://localhost/osticket">http://localhost/osticket</a>
</p>
<br>
<p align="center">
   Below is the admin portal, where we have control over settings and configurations.
</p>

<br>

<p align="center">Admin Portal</p>
<p align="center">
    <img src="https://i.imgur.com/yIvgXvG.png" height="60%" width="60%" alt="step one"/>
</p>

<br> 

<p align="center">End User Portal</p>
<p align="center">
    <img src="https://i.imgur.com/A2xk8gp.png" height="60%" width="60%" alt="step one"/>
</p>
<br>

<p align="center">The first thing we are going to do is configure roles, which in short is group users together based on job duties and function, and setting permissions to those created groups. To do this we must navigate Admin Panel -> Agents -> Roles. Here we can do a number of things, such as check the preconfigured roles and permissions, or you can add new roles. In this case click the button Add New Roles. It's good to mention that naming scheme may differ amongst the different ticketing services, it's typically the same in functionality.
</p>

<p align="center">
    <img src="https://i.imgur.com/Ei2ncZT.png" height="60%" width="60%" alt="step one"/>
</p>
<br>

<p align="center">
    Now we go into Permissions, and assign permissions based on Tickets, Tasks, and Ability to manage the Knowledgebase. Now select Add Role. Of course you are going to be specific to a persons actual job responsibilities, here we are just having a little fun. 
</p>

<p align="center">
    <img src="https://i.imgur.com/H8zul82.png" height="60%" width="60%" alt=""/>
</p>
<br>

<p align="center">
    Next we will configure departments (Help Desk, Interns, SysAdmins, Networking).
    To do this we must navigate to Admin Panel -> Agents -> Departments.
    We will add a new department in the shape of SysAdmins.
    There are many different configurations we can do, such as choosing specific SLA's, creating agents, etc. Much of this will be covered later in this project. For now, we will set the Parent, name, then select Create!
</p>

<p align="center">
    <img src="https://i.imgur.com/xrR7BDr.png" height="60%" width="60%" alt="step one"/>
</p>
<br>

<p align="center">
    Next we will create Teams. Teams is an entity where you can add different agents, from different departments, with different roles. To configure a Team navigate to Admin Panel -> Agents -> Teams. For my example I chose to name the Network Troubleshooting team. While we don't have any agents yet, This can consist of a network engineer, IT support specialist, and a sysadmin. Create your Team.
</p>

<p align="center">
    <img src="https://i.imgur.com/kb79kpR.png" height="60%" width="60%" alt=""/>
</p>
<br>

<p align="center">
    We must configure osTicket in a way that allows anyone to create tickets even if they aren't registered in the system. This includes End Users. To do this navigate to Admin Panel -> Settings -> User Settings (UNCHECK Registration Required)
</p>

<p align="center">
    <img src="https://i.imgur.com/FwZCMom.png" height="60%" width="60%" alt=""/>
</p>
<br>

<p align="center">
    We can now work on creating Agents. Navigate to Admin Panel -> Agents -> Add New Agent. Creating Agents is straight forward, you can set passwords (statically, or at next login), choose departments, roles, teams, etc. I will go ahead and creat a couple Agents, it's a good idea to mark them down in a text editor for future lab use.
</p>

<p align="center">
    <img src="https://i.imgur.com/KHJa5wl.png" height="60%" width="60%" alt=""/>
</p>

<p align="center">
     <img src="https://i.imgur.com/bNChVf9.png" height="60%" width="60%" alt=""/>
</p>
<br>

<p align="center">
    Now that we created Agents, it's time to create of End Users! Navigate to Agent Panel -> Users -> Add User. Compared to creating Agents, it's much simpler.
</p>

<p align="center">
     <img src="https://i.imgur.com/rXu1gtn.png" height="60%" width="60%" alt=""/>
</p>
<br>

<p align="center">
    Service Level Agreements or SLA for short. These are formal agreements between a service provider and a client that defines the expected service standards, such as response times, resolution times, and performance metrics, ensuring accountability and clarity for both parties. To create SLAs navigate to Admin Panel -> Manage -> SLA -> Add New SLA Plan.
</p>
<p>
    I will create 3 SLAs based on severity levels, A being the worst, and C being everyday ticket on low priority. If you need definitions of each field name, hover over the question mark. For an Example I have Sev-A, for Severity A. A Grace Period of 1 hour of receiving the ticket, in a 24/7 schedule. So it has to be resolved within an hour of being created. We will leave everything else blank.
</p>

<p align="center">
     <img src="https://i.imgur.com/7q4IwAY.png" height="60%" width="60%" alt=""/>
</p>
<br>

<p align="center">
    Lastly we will configure Help Topics. These will help categorize tickets such as password resets, networking issues, hardware issues, equipment requests, etc. Navigate to Admin Panel -> Manage -> Help Topics -> Add New Help Topic
</p>

<!--
<p align="center">
    <img src="https://github.com/user-attachments/assets/f0799a35-207d-45f8-9e7e-21fa5686f488" height="60%" width="60%" alt=""/>
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





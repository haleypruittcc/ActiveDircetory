<p align="center">
<img src="https://wiki.hornbill.com/images/d/d6/Activedirectory_logo.png"/>
</p>

<h1>Active Directory</h1>
Active Directory is a software bulit and maintained by Microsoft that centrally manage thousands of user accounts in a single place, allows you to manage devices on a large scale, and provieds a way to control access to resource on a large scale. This tutorial we're going to be learning how to deploying active directtory and creating useres.
<h2>Tools and Requirements used </h2>

- Computer with Internet Connection
- Microsoft Azure
- Vitural Machines (Window Server 2022 and Windows 10)
- Remote Desktop
- Active Directory
<h2>Configuration Steps</h2>


<h3>Step 1: Create Resource Group and Virtual Machine </h3>


<p align="center">
<img src="" height="80%" width="80%" alt="Azure Free Account"/>
  


- First going to create your Virtual Machine by naming (Windows Server 2022) "DC-1" and naming the other one "Client-1"
   - Make sure that both of your VMs are in the same Vnet (you can check the topology with Networker Watcher. If you don't know how , you can learn and following this tutorial [here](https://github.com/haleypruittcc/ResourcegroupandHelloworld).


<h3>Step 2: Ensure Connectivity between the client and Domain Controller </h3>

<p align="center">
<img src="https://i.imgur.com/5xs5hdE.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>

- Login to Client-1 with Remote Desktop and ping "-t ip address" 
- Login to the Domain Controller and enable ICMPv4 on the local windows Firewall.
- Go back to Client-1 to see the ping succeed.



<h3>Step 3: Install Active Directory </h3>

<p align="center">
<img src="" height="70%" width="70%" alt="Azure Free Account"/> <img src="" height="70%" width="70%" alt="Azure Free Services"/>
</p>

- First, login to "DC-01" on remote desktop and install Active Directory Domain Services
- Promote as a DC-1: Setup a new forest as "mydomain.com" or the name of your chose but make sure to remember it.
- Restart and then log back to "DC-1" on remote desktop by the user name you create earlier.


<h3>Step 4: Create an Admin and Normal User Account in AD </h3>

<p align="center">
<img src="https://i.imgur.com/5xs5hdE.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>

- In Active Dircetory Users and Computers (ADUC), create an Organizational Unit (OU) called 



<h3>Step 4: Create a Container and a file </h3>
 
 <p align="center">
<img src="https://i.imgur.com/ZemzOKX.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/Z01V8dO.png" height="70%" width="70%" alt="Azure Free Services"/> <img src="https://i.imgur.com/r71MgMU.png" height="70%" width="70%" alt="Azure Free Account"/> [<img src="https://i.imgur.com/kSumXSD.png" height="70%" width="70%" alt="Azure Free Account"/>] <img src="https://i.imgur.com/gSULz5Z.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>
 
- Click "Container" by scrolling down on the side of the Storage Account you created in Step 3.
- Create a "New Container" and type in the name of choice and select "Private (no anonymous access)", Click on Create.
- Open Notepad on your computer, type "Hello World," and then save the file to your desktop.
- Back to Container , Click "Upload" and Select your file form the desktop.
- Click on "View/edit" on your file you created and your file should appear. 
- Try editing the file. 
   - For an example type "My Edit" on the next line.  
- Click on "Save" and "Download" the file.
- Open back up the file and observe the change!



<h3>Step 5: How to Delete Resource Group </h3>


<p align="center">
<img src="https://i.imgur.com/I85PIqP.png" height="70%" width="70%" alt="Azure Free Account"/> 
</p>
 
 - Open your "Resource Group" in Step 2 
 - Click on "Delete Resource Group" 
 - Type the name of the Resource Group and Click "Delete".
   Finish!
  
  Tip: Delete your Resource Group will save your free $200 credits,SO MAKE SURE TO DELETE YOUR RESCOUCRE GROUPS AFTER YOU'RE DONE!  



🎉Congratulations! You have created your first Resoucre Group within Azure!🎉

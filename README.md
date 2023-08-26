<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/Io5N8d9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With osTicket now installed and set to go, we're all set to begin configuring it. First, let's head to <a href="http://localhost/osTicket/scp/login.php">osTicket for Admins/Agents</a> and utilize the login details we established during the osTicket Admins setup. Once you're logged in, we'll kick things off by configuring roles. Ensure that you're in the Admin Panel and not the Agent Panel by clicking on the top right of the page. This will toggle between Admin and Agent Panels. Once you're on the Admin Panel, navigate to:

- Admin Panel -> Agents -> Roles -> Add New Role -> Name New Role: Supreme Admin 
- Proceed to the Permissions tab and mark all the checkboxes under Tickets, Tasks, and Knowledgebase. Then Save.
</p>
<br />

<p>
<img src="https://i.imgur.com/IfJ7Px6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, let's configure departments. Navigate to Agents -> Departments -> Add New Department. Leave everything as default. Although under Manager, you can expand and choose whatever name is listed. Then Save.
</p>
<br />

<p>
<img src="https://i.imgur.com/jciMZb1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Moving on to configuring teams, navigate to Agents -> Teams. There should already be a team listed as 'Level I Support,' so we'll just create one more. Click on 'Add New Team' and name it 'Level II Support.' Under the Members tab, you can add any agent that's listed. Then Save.
</p>
<br />

<p>
<img src="https://i.imgur.com/loZl2aZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Additionally, we need to enable the option for anyone to create tickets. Navigate to Settings, then Users. Under the Settings section, ensure that the 'Registration Required' box is unchecked.
</p>
<br />

<p>
<img src="https://i.imgur.com/nOAGVbD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1PJ93RF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Let's create some agents by heading over to Agents -> Agents. You can name this agent whatever you wish, and as for the email, feel free to use a fake address like mary.jane@osticket.com. Click on 'Set Password,' uncheck both boxes, and set a simple password. Then, click 'Set' and move to the Access tab.

- Department: System Administrators
- Role: Supreme Admin.
- Extended Access: Support Click "Add"
- Extended Role: Supreme Admin. 
- Under the Teams tab, choose 'Level II Support,' then click 'Add,' and finally, press 'Create.'

Let's create one more agent, but with restricted access. Once more, choose any name you prefer and set a simple password. Under the 'Access' tab, configure the following settings:
- Department: Support
- Role: Limited Access
- Extended Access: Support.

IMPORTANT! Take note of both the agents' username and password, as well as for any future agents you might intend to create.
</p>
<br />

<p>
<img src="https://i.imgur.com/APBLeQa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, let's create some users. Switch to the Agent Panel, then go to the Users tab and click on 'Add User.' Provide a name and email of your choice, and then click 'Add User' to complete the process. Add one more using the same procedure, and then we'll move on to creating SLAs.
</p>
<br />

<p>
<img src="https://i.imgur.com/KUAjQv5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We'll establish a few Service Level Agreements (SLAs). Head back to the Admin Panel, then navigate to Manage and select SLA. Click on 'Add New SLA Plan.' Next, create the following:

- Name: SEV-A; Grace Period: 1 hour; Schedule: 24/7
- Name: SEV-B; Grace Period: 4 hours; Schedule: 24/7
- Name: SEV-c; Grace Period: 8 hours; Schedule: Business Hours

</p>
<br />

<p>
<img src="https://i.imgur.com/6S23tFR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
And finally we'll create some Help Topics. Simply go to Manage then Help Topics. Press "Add New Help Topic" and create the following:

- Topic: Business Critical Outage
- Topic: Personal Computer Issues
- Topic: Equipment Request
- Topic: Password Reset
</p>
<br />

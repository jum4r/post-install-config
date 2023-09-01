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

- Windows 10</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Add & Configure Roles
- Configure Departments & Teams
- Configure Agents (workers) & Users (customers)
- Configure Service Level Agreements (SLA)
- Configure Help Topics

<h2>Configuration Steps</h2>

### Add & Configure Roles
<img width="752" alt="image" src="https://i.imgur.com/Io5N8d9.png">

1. Head to [osTicket for Admins/Agents](http://localhost/osTicket/scp/login.php)
2. Login with sam_admin/Password1
3. Ensure you're in the Admin Panel and not the Agent Panel by clicking Admin/Agent at the top of the page to toggle between the two.
4. In the Admin Panel, navigate to:
   - Agents > Roles > Add New Role
   - Name New Role: Supreme Admin 
   - Permissions: Check all boxes under Tickets, Tasks, and Knowledgebase. Save.

### Add & Configure Departments
<img width="752" alt="image" src="https://i.imgur.com/IfJ7Px6.png">

1. Navigate to Agents > Departments > Add New Department
   - Name: System Administrators
   - Manager: Select the only user  
   - Leave everything else as default. Save.

### Add & Configure Teams
<img width="752" alt="image" src="https://i.imgur.com/jciMZb1.png">

1. Navigate to Agents > Teams > Add New Team
   - Name: Level II Support
   - Members: Add a member. Save.

### Ensure Anyone is Able to Create Tickets
<img width="752" alt="image" src="https://i.imgur.com/loZl2aZ.png">

1. Navigate to Settings > Users.
2. Under the Settings section, ensure that the 'Registration Required' box is unchecked.

### Add & Configure Agents
<img width="752" alt="image" src="https://i.imgur.com/nOAGVbD.png">

1. Navigate Agents > Agents > Add New Agent:
   - Name: mary jane
   - Email: mary.jane@osticket.com
   - Username: mary.jane
   - Click 'Set Password' and uncheck both boxes
   - Password: Password1
2. In the Access tab:
   - Department: System Administrators
   - Role: Supreme Admin.
   - Extended Access: Support (Click 'Add')
   - Extended Role: Supreme Admin 
3. In the Teams tab:
   - Teams: Level II Support (Click 'Add')
4. Once it's done, we'll create another:
   - Name: peter parker
   - Email: peter@osticket.com
   - Username: peter.parker
   - Password: Password1
6. In the 'Access' tab:
   - Department: Support
   - Role: Limited Access
   - Extended Access: Support

### Add Users
<img width="752" alt="image" src="https://i.imgur.com/APBLeQa.png">

1. Switch to the Agent Panel
2. Go to Users tab, 'Add User' 
   - Email: kate@osticket.com
   - Name: kate kate 
   - Click 'Add User'
3. Create another:
   - Email: nate@osticket.com
   - Name: nate nate 
   - Click 'Add User'

### Add & Configure Service Level Agreements (SLAs)
<img width="752" alt="image" src="https://i.imgur.com/KUAjQv5.png">

1. Switch back to the Admin Panel
2. Navigate to Manage > SLA > Add New SLA Plan
3. Create the following:
   - Name: SEV-A; Grace Period: 1 hour; Schedule: 24/7
   - Name: SEV-B; Grace Period: 4 hours; Schedule: 24/7
   - Name: SEV-C; Grace Period: 8 hours; Schedule: Business Hours

### Add Help Topics
<img width="752" alt="image" src="https://i.imgur.com/6S23tFR.png">

1. Finally go to Manage > Help Topics > Add New Help Topic
2. Create the following:
   - Topic: Business Critical Outage
   - Topic: Personal Computer Issues
   - Topic: Equipment Request
   - Topic: Password Reset


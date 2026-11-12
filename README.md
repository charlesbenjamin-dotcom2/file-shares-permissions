 # ✨ Lab: Network File Shares and Permissions

📋 Table of Contents

- [About the project]((#about-the-project))
- [Environments and Technologies Used]((#environments-and-technologies-used))
- [Operating Systems Used]((#operating-systems-used))
- [Steps]((#steps)) 


## 🔎 About the project
In this tutorial, we share resources over the network. Create File Shares to allow Read, Write, or Deny access to individual users or groups. 

---
### 🍂 Environments and Technologies used: 
  - Microsoft Azure ( Virtual Machines)
  - Remote Desktop
  - Active Directory Domain Services
----
### ⚙ Operating Systems Used: 
- Windows Server 2024
- Windows 11
---
### 📜 Steps 
- Step 1 : Log into your domain account as an admin
- Step 2 : On the C:\ drive create 4 folders
- Step 3 : Set folder permissions
- Step 4 : Log into dVM account as a normal user
- Step 5 : Access folders to verify permission levels


<h3> Step 1 : Log into your domain account as an admin</h3>
As mentioned in the environments and technologies section we will be utilizing Microsoft Azure, Remote Desktop and Active Directory Domain services. This lab follows after the configuring-active-directory lab. To replicate the steps you need to have set up two virtual VMs within Azure. One as a domaain controller utilizing Windows Server 2024 and the other as a client utilizing windows 11. Next we would also to have deployed our Active Directory environment with the appropriate groups and users. From there we utilize Remote Desktop to first log in to the Admmin account.


<h3> Step 2 : On the C:\ drive create 4 folders</h3>
After logging in as an admin, we head over to the C:\ drive to create 4 folders. The first named Accounting will be utilized to set group permissions. The other 3 wiil be used to set individual permissions

<h3> Step 3 : Set folder permissions</h3>
While still in the C:\ drive we then for all 3 individual user folders we follow these steps to give them teir respective permisions

  - Right click the folder and go to properties
  - Click on the Sharing tab of the properties window
  - Then click on share
  - type domain users in the search bar of the noetwrok acccess window
  - Click the add button to the right of the search bar
  - Once added domain users will appear in the box 
  - To the right of their name the permission level will be listed with an arrow that allows you to set the appropriate level
  - Then click on the share button at the bottom right of the network access window. 
  - Once folder has been shared click the done button is network access window
  
  
  
<h3> Step 4 : Log into VM account as a normal user</h3>
In this step you will log into the client virtual machine we previuosly created
<h3> Step 5 : Access folders to verify permission levels</h3>
From there we will click on all 4 four folders to verify the permisson level. 

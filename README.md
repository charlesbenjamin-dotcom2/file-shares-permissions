 # ✨ Lab: Network File Shares and Permissions


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
- Step 1: Log in to your domain account as an admin
- Step 2: On the C:\ drive, create 3 folders
- Step 3: Set folder permissions
- Step 4: Log in to the client account as a normal user
- Step 5: Access folders to verify permission levels 

#

<h3>🎯 Step 1: Log in to your domain account as an admin</h3>
As mentioned in the environments and technologies section, we will utilize Microsoft Azure, Remote Desktop, and Active Directory Domain Services. This lab follows the configuring-active-directory lab. To replicate the steps, you need to have set up two virtual VMs within Azure. One as a domain controller using Windows Server 2024 and the other as a client using Windows 11. We also need to have deployed our Active Directory environment with the appropriate groups and users. From there, we use Remote Desktop to log in to the Admin account.

#

<h3>🎯 Step 2: On the C:\ drive create 3 folders</h3>
After logging in as an admin, click on File Explorer, then click on the C:\ drive to create 3 folders. The names are not important, but to reduce confusion, we will name the folders according to the access level they will receive. So, no-access, read-access, and write-access.

#

<h3>🎯 Step 3: Set folder permissions</h3>
While still in the C:\ drive, we then set the permissions for all 3 folders. We follow these steps to give them their respective permissions.

  - Right-click the folder and go to properties
  - Click on the Sharing tab of the properties window
  - Then click on Share
  - Type Domain Users in the search bar of the Network Access window
  - Click the Add button to the right of the search bar
  - Once added, Domain Users will appear in the box below
  - To the right of their name, the permission level will be listed with an arrow that allows you to set the appropriate level
  - Then click on the Share button at the bottom right of the network access window. 
  - Once the folder has been shared, click the Done button in the network access window
  
  #
  
<h3>🎯 Step 4: Log in to VM account as a normal user</h3>
In this step, we log into the client virtual machine we previously created via Remote Desktop.

#

<h3>🎯 Step 5: Access folders to verify permission levels</h3>
After logging into the client VM, we click on File Explorer, then in the search bar, type \\dc-1. DC-1 is the name of the Domain Controller virtual machine we previously set up in our configuring-active-directory lab. From there, we can verify the permission level for each folder by following these steps

  - Double-click on the folder (In this step, both the read and the read-write folder would allow access into the folder, while the no-access folder would not)
  - While inside the folder, right-click, then click on New, then click on Text Document to create a new document ( In this step, the read-write folder would allow access, while the read folder would not)

# 🧠 Active Directory Homelab - Windows Server 2022

💻 Platform: VMware / VirtualBox
🛠️ Tools: Windows Server 2022, Active Directory Domain Services
## 📌 Objective
To install and configure Active Directory Domain Services on Windows Server 2022, create Organizational Units (OUs), and apply Group Policies.

## 🖥️ Environment Setup
Virtual Machine Setup

OS: Windows Server 2022

RAM: 16GB

Disk: 20GB

Joined to Internal Network


✅ VMware/VirtualBox VM settings
<img width="1266" height="872" alt="Install of Windows Server" src="https://github.com/user-attachments/assets/4413627f-f4c9-4622-a537-61fadef48e1f" />



<img width="1268" height="880" alt="Install of Windows 2 0" src="https://github.com/user-attachments/assets/7683d8d5-1ce7-42f8-9c0d-4f227effad65" />



## ⚙️ Installing Active Directory Domain Services
Open Server Manager

Click on Manage > Add Roles and Features

Select Active Directory Domain Services (AD DS)

Install and Promote to Domain Controller

Set up new forest (e.g., homelab.local)

Set DSRM password

Restart server after installation


✅ Add Roles and Features wizard
<img width="1268" height="890" alt="Add roles and features" src="https://github.com/user-attachments/assets/69481fdf-731c-400d-9ea9-599ca24476ec" />



✅ Choosing AD DS role
<img width="796" height="557" alt="Active  Directory Domain Services" src="https://github.com/user-attachments/assets/a877aabe-7fa3-40a2-b3d9-2c0a8b712b9d" />



✅ Domain configuration
<img width="1043" height="772" alt="image" src="https://github.com/user-attachments/assets/65d43dc4-d412-466f-bba1-1589ddae8ac3" />



✅ Post-installation reboot
<img width="1263" height="876" alt="Prerequisites" src="https://github.com/user-attachments/assets/64219738-4660-4554-9000-050d811e6b87" />


## 🏢 Creating Organizational Units (OUs)
Open Active Directory Users and Computers

Right-click on your domain name > New > Organizational Unit

Create the following:

OU=Computers

OU=Users

OU=Servers  




✅ OUs being created
<img width="753" height="538" alt="Organizational Unit" src="https://github.com/user-attachments/assets/749bb53c-8d44-4a8a-aaea-9f6039876ca6" />


✅ Final structure view
<img width="1045" height="826" alt="final view" src="https://github.com/user-attachments/assets/caefecdb-0973-462a-9d43-c709a7f469c9" />



## 👥 Creating Users and Groups
Right-click on the desired OU > New > User

Create sample users (e.g., jdoe, asmith)

Create Security Groups under IT OU

📸 Screenshots to include:




✅ Creating a new user
<img width="1049" height="815" alt="Create a user" src="https://github.com/user-attachments/assets/f13c53b0-f88a-4717-a9ff-5c70f657ce56" />


✅ Creating a security group
<img width="776" height="543" alt="New ojbect group" src="https://github.com/user-attachments/assets/94ad4eb2-b3be-4e37-b72a-8a966fd9c4d6" />


✅ Final list of users/groups
<img width="1036" height="774" alt="Userr" src="https://github.com/user-attachments/assets/08927829-a318-41e2-a8b3-454a7e10a19c" />



## 🛡️ Applying Group Policies (GPO)
Open Group Policy Management

Create a new GPO (e.g., "Disable Control Panel")

Edit the GPO:

Navigate to: User Configuration > Administrative Templates > Control Panel

Enable Prohibit access to Control Panel

Link GPO to the appropriate OU




✅ Group Policy Management Console
<img width="1043" height="823" alt="Group policy management console" src="https://github.com/user-attachments/assets/429e4f36-afea-46db-b294-d242f576c687" />


✅ GPO settings
<img width="756" height="543" alt="Group policy" src="https://github.com/user-attachments/assets/bb1a4b09-ea88-43f8-9fea-ff3f87fc7f6b" />


✅ GPO linked to OU
<img width="1080" height="866" alt="connected ou" src="https://github.com/user-attachments/assets/f4e3b5a6-9699-441a-a42e-fa0c99839299" />

## 🧪 Testing
Login as a domain user

Confirm policy is applied (Control Panel disabled)

Confirm user is under correct OU



✅ Logged-in user screen
<img width="1273" height="890" alt="login user " src="https://github.com/user-attachments/assets/bcc31d7f-ff3b-471a-94f1-b5f221487bca" />


<img width="1276" height="886" alt="gggg" src="https://github.com/user-attachments/assets/77ee3335-0bd8-4405-b3ff-d812a61fece5" />


✅ Evidence of policy working
<img width="1262" height="859" alt="Dont have access" src="https://github.com/user-attachments/assets/2fba0fbc-2000-4060-a31d-63f886e68b45" />
 

here change it

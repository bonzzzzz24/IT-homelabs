🧠 Active Directory Homelab - Windows Server 2022
💻 Platform: VMware / VirtualBox
🛠️ Tools: Windows Server 2022, Active Directory Domain Services

📌 Objective
Set up and configure Active Directory Domain Services (AD DS) on Windows Server 2022, create Organizational Units (OUs), and apply Group Policies to manage a homelab environment.

🖥️ Environment Setup
Virtual Machine Specs:

OS: Windows Server 2022

RAM: 16GB

Disk: 20GB

Network: Internal

✅ VMware/VirtualBox VM Settings:
<img width="1266" height="872" alt="Install of Windows Server" src="https://github.com/user-attachments/assets/4413627f-f4c9-4622-a537-61fadef48e1f" />

<img width="1268" height="880" alt="Install of Windows 2 0" src="https://github.com/user-attachments/assets/7683d8d5-1ce7-42f8-9c0d-4f227effad65" />
⚙️ Installing Active Directory Domain Services
Open Server Manager

Click Manage > Add Roles and Features

Select Active Directory Domain Services (AD DS)

Install and promote the server to a domain controller

Create a new forest (e.g., homelab.local)

Set the DSRM password

Reboot the server after installation

✅ Add Roles and Features Wizard
<img width="1268" height="890" alt="Add roles and features" src="https://github.com/user-attachments/assets/69481fdf-731c-400d-9ea9-599ca24476ec" />

✅ Choosing AD DS Role
<img width="796" height="557" alt="Active Directory Domain Services" src="https://github.com/user-attachments/assets/a877aabe-7fa3-40a2-b3d9-2c0a8b712b9d" />

✅ Domain Configuration
<img width="1043" height="772" alt="Domain Configuration" src="https://github.com/user-attachments/assets/65d43dc4-d412-466f-bba1-1589ddae8ac3" />

✅ Post-Installation Reboot
<img width="1263" height="876" alt="Prerequisites" src="https://github.com/user-attachments/assets/64219738-4660-4554-9000-050d811e6b87" />

🏢 Creating Organizational Units (OUs)
Open Active Directory Users and Computers

Right-click the domain name > New > Organizational Unit

Create these OUs:

Computers

Users

Servers

✅ OUs Being Created
<img width="753" height="538" alt="Organizational Unit" src="https://github.com/user-attachments/assets/749bb53c-8d44-4a8a-aaea-9f6039876ca6" />

✅ Final OU Structure
<img width="1045" height="826" alt="Final View" src="https://github.com/user-attachments/assets/caefecdb-0973-462a-9d43-c709a7f469c9" />

👥 Creating Users and Groups
Right-click the desired OU > New > User

Create sample users (e.g., jdoe, asmith)

Under the IT OU, create Security Groups as needed

✅ Creating a User
<img width="1049" height="815" alt="Create User" src="https://github.com/user-attachments/assets/f13c53b0-f88a-4717-a9ff-5c70f657ce56" />

✅ Creating a Security Group
<img width="776" height="543" alt="New Object Group" src="https://github.com/user-attachments/assets/94ad4eb2-b3be-4e37-b72a-8a966fd9c4d6" />

✅ Final List of Users/Groups
<img width="1036" height="774" alt="User List" src="https://github.com/user-attachments/assets/08927829-a318-41e2-a8b3-454a7e10a19c" />

🛡️ Applying Group Policies (GPO)
Open Group Policy Management

Create a new GPO (e.g., Disable Control Panel)

Edit the GPO:

Navigate to: User Configuration > Administrative Templates > Control Panel

Enable Prohibit access to Control Panel

Link the GPO to the target OU

✅ Group Policy Management Console
<img width="1043" height="823" alt="Group Policy Management Console" src="https://github.com/user-attachments/assets/429e4f36-afea-46db-b294-d242f576c687" />

✅ GPO Settings
<img width="756" height="543" alt="Group Policy Settings" src="https://github.com/user-attachments/assets/bb1a4b09-ea88-43f8-9fea-ff3f87fc7f6b" />

✅ GPO Linked to OU
<img width="1080" height="866" alt="Connected OU" src="https://github.com/user-attachments/assets/f4e3b5a6-9699-441a-a42e-fa0c99839299" />

🧪 Testing
Log in as a domain user

Confirm the policy is applied (Control Panel disabled)

Confirm user is in the correct OU

✅ Domain User Login
<img width="1273" height="890" alt="Login User" src="https://github.com/user-attachments/assets/bcc31d7f-ff3b-471a-94f1-b5f221487bca" />

<img width="1276" height="886" alt="Logged In" src="https://github.com/user-attachments/assets/77ee3335-0bd8-4405-b3ff-d812a61fece5" />
✅ Policy Successfully Applied
<img width="1262" height="859" alt="Access Denied" src="https://github.com/user-attachments/assets/2fba0fbc-2000-4060-a31d-63f886e68b45" />

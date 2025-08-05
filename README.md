# 🧠 Active Directory Homelab - Windows Server 2022

💻 **Platform**: VMware / VirtualBox  
🛠️ **Tools**: Windows Server 2022, Active Directory Domain Services

---

## 📚 Table of Contents

- [📌 Objective](#-objective)
- [🖥️ Environment Setup](#️-environment-setup)
- [⚙️ Installing Active Directory Domain Services](#️-installing-active-directory-domain-services)
- [🏢 Creating Organizational Units (OUs)](#-creating-organizational-units-ous)
- [👥 Creating Users and Groups](#-creating-users-and-groups)
- [🛡️ Applying Group Policies (GPO)](#️-applying-group-policies-gpo)
- [🧪 Testing](#-testing)

---

## 📌 Objective

To install and configure Active Directory Domain Services on Windows Server 2022, create Organizational Units (OUs), and apply Group Policies.

---

## 🖥️ Environment Setup

**Virtual Machine Setup**

- **OS**: Windows Server 2022  
- **RAM**: 16GB  
- **Disk**: 20GB  
- **Network**: Internal Network  

### ✅ VMware/VirtualBox VM Settings

![Install of Windows Server](https://github.com/user-attachments/assets/4413627f-f4c9-4622-a537-61fadef48e1f)
![Install of Windows Server 2.0](https://github.com/user-attachments/assets/7683d8d5-1ce7-42f8-9c0d-4f227effad65)

---

## ⚙️ Installing Active Directory Domain Services

1. Open **Server Manager**
2. Go to **Manage > Add Roles and Features**
3. Select **Active Directory Domain Services (AD DS)**
4. Install and **promote to Domain Controller**
5. Set up a new forest (e.g., `homelab.local`)
6. Set **DSRM password**
7. Restart server after installation

### ✅ Steps in Screenshots

![Add Roles and Features](https://github.com/user-attachments/assets/69481fdf-731c-400d-9ea9-599ca24476ec)
![Choosing AD DS Role](https://github.com/user-attachments/assets/a877aabe-7fa3-40a2-b3d9-2c0a8b712b9d)
![Domain Configuration](https://github.com/user-attachments/assets/65d43dc4-d412-466f-bba1-1589ddae8ac3)
![Post-Install Reboot](https://github.com/user-attachments/assets/64219738-4660-4554-9000-050d811e6b87)

---

## 🏢 Creating Organizational Units (OUs)

1. Open **Active Directory Users and Computers**
2. Right-click your domain > **New > Organizational Unit**
3. Create the following:
   - OU=Computers
   - OU=Users
   - OU=Servers  

### ✅ Screenshots

![Creating OU](https://github.com/user-attachments/assets/749bb53c-8d44-4a8a-aaea-9f6039876ca6)
![Final Structure View](https://github.com/user-attachments/assets/caefecdb-0973-462a-9d43-c709a7f469c9)

---

## 👥 Creating Users and Groups

1. Right-click an OU > **New > User**
2. Create sample users (e.g., `jdoe`, `asmith`)
3. Under an OU (e.g., IT), create **Security Groups**

### ✅ Screenshots

![Create a User](https://github.com/user-attachments/assets/f13c53b0-f88a-4717-a9ff-5c70f657ce56)
![Create a Security Group](https://github.com/user-attachments/assets/94ad4eb2-b3be-4e37-b72a-8a966fd9c4d6)
![Final List](https://github.com/user-attachments/assets/08927829-a318-41e2-a8b3-454a7e10a19c)

---

## 🛡️ Applying Group Policies (GPO)

1. Open **Group Policy Management**
2. Create new GPO (e.g., “Disable Control Panel”)
3. Edit the GPO:
   - Go to **User Configuration > Administrative Templates > Control Panel**
   - Enable **Prohibit access to Control Panel**
4. Link GPO to the appropriate OU

### ✅ Screenshots

![Group Policy Management](https://github.com/user-attachments/assets/429e4f36-afea-46db-b294-d242f576c687)
![GPO Settings](https://github.com/user-attachments/assets/bb1a4b09-ea88-43f8-9fea-ff3f87fc7f6b)
![GPO Linked to OU](https://github.com/user-attachments/assets/f4e3b5a6-9699-441a-a42e-fa0c99839299)

---

## 🧪 Testing

1. Log in as a **domain user**
2. Confirm:
   - User is in correct OU
   - Group Policy is applied (Control Panel disabled)

### ✅ Screenshots

![Logged-In User](https://github.com/user-attachments/assets/bcc31d7f-ff3b-471a-94f1-b5f221487bca)
![Control Panel Restricted](https://github.com/user-attachments/assets/2fba0fbc-2000-4060-a31d-63f886e68b45)

---

## ✅ Summary

This homelab demonstrates a full setup of Active Directory Domain Services with real-world structure and policies. It’s a great beginner-to-intermediate hands-on lab for learning Windows Server administration and AD basics.

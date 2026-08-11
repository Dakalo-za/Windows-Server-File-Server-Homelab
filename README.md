# Windows-Server-File-Server-Homelab
A windows Server homelab project focused on Active directory, file sharing, NTFS permissions and user/group management

# Windows Server File Server Homelab

## 📌 Overview

A Windows Server homelab project focused on **Active Directory, file sharing, NTFS permissions, and user/group management**.

The goal was to simulate a small company's file server and control access to departmental data.

## 🖥️ Environment

* Windows Server
* Active Directory
* VMware
* File Server
* Active Directory Users and Computers

## 📁 Folder Structure

```text
CompanyData
├── IT
├── HR
├── Finance
└── Public
```

## ⚙️ What I Did

### 1. Created Shared Folders

Created a `CompanyData` folder with separate folders for:

* IT
* HR
* Finance
* Public

### 2. Created Active Directory Groups

Created security groups for each department and organized them within Active Directory.

### 3. Created Test Users

Created test users and assigned them to their corresponding departmental security groups.

### 4. Configured NTFS Permissions

Configured folder permissions so that only authorized department users could access their respective folders.

* Applied **Modify** permissions
* Disabled inheritance
* Removed unauthorized access

### 5. Configured Share Permissions

Configured `CompanyData` as a shared folder using **Advanced Sharing** and configured the share permissions.

## 🐛 Troubleshooting

**Active Directory naming conflict**

* An `HR` OU already existed, preventing the creation of an `HR` group.
* Created a new `Users` OU and added the required groups.

**Password policy issue**

* Test user passwords did not meet the domain password policy.
* Reviewed the password policy and created compliant passwords.

## 🧠 Skills Demonstrated

* Windows Server Administration
* Active Directory
* User & Group Management
* Security Groups
* NTFS Permissions
* File Sharing
* Permission Inheritance
* Basic Troubleshooting

## 📸 Screenshots

Screenshots documenting the implementation are included in this repository.

## 🚀 Future Improvements

* Add a Windows client VM
* Test departmental access using different users
* Configure Group Policy
* Configure mapped network drives
* Test backup and restore

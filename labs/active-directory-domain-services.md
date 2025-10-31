# Lab 004: Active Directory Domain Services Setup

**Date:** 31/10/2025.

**Objective:** Successfully deploy Active Directory Domain Services using Windows Server Manager.

## Lab Overview
Following the client/server OS discovery in Lab 003, this lab implements Active Directory using the Server Manager GUI on Windows Server 2022, building the foundation for enterprise identity management.

## Implementation Steps

### 1. Environment Preparation
- Created new DC03 virtual machine with Windows Server 2022 Evaluation
- Verified clean installation with Server Manager available

### 2. Network Configuration
- Accessed **Server Manager → Local Server → Ethernet** settings
- Configured static IP via Network Connections properties:
  - **IP Address:** 192.168.1.10
  - **Subnet Mask:** 255.255.255.0
  - **Default Gateway:** 192.168.1.1
  - **Preferred DNS:** 192.168.1.10 (self-referencing)

### 3. Active Directory Installation 
- Used **Server Manager → Manage → Add Roles and Features**
- Selected **Active Directory Domain Services** role
- Added required features through the pop-up prompt
- Completed installation through the wizard interface

### 4. Domain Controller Promotion (GUI Method)
- Clicked **notification flag → "Promote this server to a domain controller"**
- Selected **"Add a new forest"** deployment configuration
- Set **Root domain name:** winfredlab.local
- Configured **Directory Services Restore Mode (DSRM)** password
- Accepted default options for DNS, Paths, and Review
- Passed prerequisites check and initiated installation
- Server automatically rebooted after promotion

## Configuration Details
- **Domain Name:** winfredlab.local
- **Server Role:** Domain Controller
- **Forest Functional Level:** Windows Server 2022
- **DNS Server:** Integrated with AD DS
- **IP Configuration:** 192.168.1.10/24
- **Installation Method:** Server Manager GUI

## Verification Tests
- ✅ Active Directory Users and Computers console accessible
- ✅ DNS Manager shows integrated _msdcs.winfredlab.local zone
- ✅ Server appears as Domain Controller in Server Manager
- ✅ Can resolve mylab.local domain internally
- ✅ AD DS role shown as installed in Server Manager

## Evidence
- 

## Skills Demonstrated
- Windows Server GUI navigation and management
- Network configuration through graphical interface
- Role-based installation via Server Manager
- Domain controller deployment wizard
- Integrated DNS configuration understanding

## Key Achievements
- Established first domain controller using GUI method
- Successfully configured integrated DNS services
- Built foundation for user/group management labs
- Applied lessons from Lab 003 to ensure correct platform
- Gained experience with Windows Server administrative tools

---

**Status:** ✅ Complete  
**Environment:** Windows Server 2022 | Oracle VirtualBox  
**Method:** Server Manager GUI  
**Follow-up:** User and group management operations

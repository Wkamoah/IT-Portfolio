# Lab 003: Client vs Server Operating System Discovery

**Date:** 31/10/2025
**Objective:** Identify and resolve fundamental environment configuration error - attempting to install server roles on client OS

## Problem Identification
**Initial Issue:** Active Directory Domain Services installation failing repeatedly on DC01 and DC02

**Symptoms Observed:**
- Server Manager application missing from Windows installation
- `Install-WindowsFeature` command not recognized
- No option to promote server to domain controller
- System identified as Windows 10 Pro instead of Windows Server

## Root Cause Analysis
**Discovery:** Both DC01 and DC02 virtual machines were created with **Windows 10 Pro** (client operating system) instead of **Windows Server 2022** (server operating system).

**Key Learning Point:** 
- **Client OS** (Windows 10/11): Designed for end-user workstations, cannot run enterprise server roles
- **Server OS** (Windows Server 2022): Specifically designed to host network services like Active Directory, DNS, DHCP

## Technical Understanding
### Windows 10 Pro Limitations:
- Cannot install Active Directory Domain Services role
- Missing server management tools (Server Manager, AD Admin Center)
- Limited to 2TB RAM vs Windows Server's 24TB
- No built-in Hyper-V role for additional virtualization

### Windows Server 2022 Requirements:
- Required for domain controller promotion
- Includes Server Manager and administrative tools
- Supports enterprise roles and features
- Designed for 24/7 operation and multiple concurrent users

## Resolution Steps
1. **Document the learning experience** in portfolio
2. **Download Windows Server 2022 Evaluation ISO** from Microsoft
3. **Create new DC03 virtual machine** with proper server OS
4. **Proceed with original AD DS lab objectives** on correct platform

## Evidence
- https://github.com/Wkamoah/IT-Portfolio/tree/main/evidence/lab%20003

## Lessons Learned
1. **Environment verification** is crucial before beginning complex configurations
2. **Understanding OS capabilities** prevents wasted troubleshooting time
3. **Documenting mistakes** is as valuable as documenting successes
4. **Recovery planning** is an essential IT skill

## Next Steps
- Proceed with Lab 004: Active Directory Domain Services Setup on DC03
- Apply lessons learned to future environment planning

---

**Status:** ✅ Complete (Learning Objective Achieved)  
**Follow-up Lab:** Lab 004 - Active Directory Domain Services Setup (DC03)

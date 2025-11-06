# 🖥️ IT Support & Systems Administration Portfolio

**Welcome to my hands-on IT learning journey!** This repository documents my progress through a structured 10-month IT Career Launch Plan, from IT Support fundamentals to Systems Administration.

---

## 🚀 About Me

I'm **Winfred Kofi Amoah**, a Ghanaian IT student based in Moscow, transitioning into IT Support and Systems Administration. Currently enrolled in a self-directed 10-month accelerator program, building practical skills through home labs and certification prep.

**Career Goal:** Secure entry-level IT Support role by January 2026, progressing to Junior Systems Administrator by August 2026.

---

## 📚 Learning Journey & Problem-Solving

### 1. Virtualization Boot Challenge (23.10.2025)
**Challenge:** Initial DC01 VM failed to boot during Windows Server deployment  
**Discovery:** VirtualBox requires explicit boot configuration from ISO files  
**Solution:** 
- Diagnosed boot order settings in VM configuration
- Created DC02 VM with corrected boot priority → successful installation
- Applied solution to original DC01 VM
**Outcome:** Both domain controllers now operational, deeper understanding of virtualization platform

### Client vs Server OS Discovery (31.10.2025)
**Challenge:** Attempted to install Active Directory on Windows 10 VMs (DC01/DC02)  
**Discovery:** Windows 10 is a client OS and cannot run server roles like Active Directory Domain Services  
**Solution:** 
- Researched differences between client and server operating systems
- Identified the need for Windows Server 2022 for domain controller functionality
- Documented the learning process and created recovery plan
**Outcome:** Deeper understanding of OS fundamentals and proper lab environment planning

### 2. Freshdesk Workflow Optimization (01.11.2025)
**Challenge:** 
- Ticket documentation for LAB# 001,002,003 and 004 lacked professional structure.
- No Freshdesk Tutorial for in-depth knowledge of the features of Freshdesk
  
**Discovery:** Professional IT support requires systematic ticket management for tracking and accountability.  

**Solution:** 
- Watched a Freshdesk tutorial video on youtube, took notes and tried some features.
- Video link =  https://www.youtube.com/watch?v=5MUFKgNuN84
  
**Key Learnings:** 
- Freshdesk can do automatic ticket assignment using a "Round Robin" system to evenly distribute work among agents.
- I can add automatic escalation rules to alert managers if a ticket remains unassigned for a set time, ensuring nothing gets forgotten.
- Freshdesk can track team performance metrics on its dashboard, like unresolved tickets per group and average response times.
- I can set different agent access levels (Global, Group, Restricted) and track their availability status (e.g., Working, Away).
- I can use private internal notes on tickets for team communication that the customer cannot see.
- Freshdesk allows you to use a custom professional email domain (e.g., support@winfredlab.com) instead of a generic address.
- I can customize ticket fields and dropdowns (like Type, Priority, Source) to fit my lab's specific workflow.

### 3. Real-World Hardware & Boot Troubleshooting (04.11.2025)
**Challenge:** Colleague's Dell laptop had dual issues: boot failures and automatic power-on  
**Discovery:** 
- **Boot Issue:** GPT disk partition required UEFI mode, but BIOS was set to Legacy/CSM
- **Power Issue:** Physical power button was mechanically stuck, sending constant "on" signal
**Solution:**
- Systematically eliminated software causes using `powercfg -lastwake` and BIOS settings
- Identified hardware fault via sleep mode test (unresponsive power button)
- Configured UEFI-only boot mode and advised on hardware repair
**Outcome:** Successfully diagnosed complex multi-layer issue combining firmware configuration and physical hardware failure
---

## 🛠️ Active Home Lab Environment

### Current Setup
- **Virtualization:** Oracle VirtualBox
- **Domain Controller:** Windows Server 2022 (DC01)
- **Client Machine:** Windows 10
- **Ticketing System:** Freshdesk for lab documentation
- **Version Control:** GitHub for evidence tracking

---



## 🎯 Current Focus (Phase 1: 90-Day)

### Active Certifications in Progress
- **Google IT Support Certificate**
- **CompTIA A+** (Core 1 & 2)


---

## 📈 Technical Skills Progress

### 🖥️ Systems Administration
![Active Directory](https://img.shields.io/badge/Active_Directory-Learning-yellow?style=flat)
![PowerShell](https://img.shields.io/badge/PowerShell-Learning-yellow?style=flat)
![Windows Server](https://img.shields.io/badge/Windows_Server-Intermediate-green?style=flat)

### 🌐 Networking Fundamentals
![TCP/IP](https://img.shields.io/badge/TCP/IP-Learning-yellow?style=flat)
![DNS](https://img.shields.io/badge/DNS-Learning-yellow?style=flat)
![DHCP](https://img.shields.io/badge/DHCP-Learning-yellow?style=flat)

### 🔧 IT Tools & Platforms
![VirtualBox](https://img.shields.io/badge/VirtualBox-Intermediate-green?style=flat)
![Freshdesk](https://img.shields.io/badge/Freshdesk-Intermediate-green?style=flat)
![Git](https://img.shields.io/badge/Git-Intermediate-green?style=flat)

---

## 📊 Lab Completion Progress

| Lab # | Topic | Status | Evidence |
|-------|-------|--------|----------|
| 001 | Virtual Hardware Diagnostic | ✅ Complete | [View Lab](https://github.com/Wkamoah/IT-Portfolio/blob/main/labs/pc-hardware%20diagnostics.md) |
| 002 | VM Boot Configuration Troubleshooting| ✅ Complete | [View Lab](https://github.com/Wkamoah/IT-Portfolio/blob/main/labs/vm-boot-configuration-troubleshooting.md) |
| 003 | Client vs Server OS Discovery | ✅ Complete |  [View Lab](https://github.com/Wkamoah/IT-Portfolio/blob/main/labs/client-vs-server-os-discovery.md) |
| 004 | Active Directory Setup | ✅ Complete | [View Lab](https://github.com/Wkamoah/IT-Portfolio/blob/main/labs/active-directory-domain-services.md) | 
| Rea 001 | Dell Laptop Boot and Hardware Troubleshooting | ✅ Complete | [View Lab](https://github.com/Wkamoah/IT-Portfolio/blob/main/realworld/laptop-boot-power-issue-troubleshooting.md) | 

---

## 🎓 Certification Roadmap

1. **Google IT Support Certificate** (Nov 2025)
2. **CompTIA A+** (Q1 2026)
3. **CompTIA Network+** (2026)
4. **CompTIA Security+** (2026)
5. **Microsoft AZ-900** (2026)

---

## 📫 Connect With Me

- **Email:** wcannerro@gmail.com | winfredkofiamoah@mail.com
- **GitHub:** [@Wkamoah](https://github.com/Wkamoah)
- **Location:** Moscow, Russia (Peoples' Friendship Univerity of Russia)

---

## 🔄 Update Log

- **2025-10-22:** Repository created with initial lab structure
- **2025-10-23:** Completed Lab 001 - Virtual Hardware Diagnostic
- **2025-10-31:** Windows Server 2022 deployment (Lesson Learned)
- **2025-11-01:** Freshdesk Optimization



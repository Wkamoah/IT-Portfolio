# Lab 002: VM Boot Configuration Troubleshooting

**Date:** 20/10/2025
**Objective:** Diagnose and resolve virtual machine boot media and configuration issues

## Problem Report
**Initial Issue:** DC01 VM failed during Windows Server setup with error:  
*"Windows cannot find the Microsoft Software License Terms. Make sure the installation sources are valid and restart the installation."*

**User Complaint:** "Windows Server installation fails with license terms error during setup phase"

## Troubleshooting Process

### Step 1: Problem Identification
- VM boots successfully from ISO
- Windows Setup starts loading
- Fails with specific error about missing license terms
- Installation cannot proceed beyond initial phase

### Step 2: Root Cause Analysis
- **Verified ISO file:** Downloaded from official Microsoft Evaluation Center
- **Checked VM configuration:** Resources adequate, ISO properly attached
- **Identified Issue:** Corrupted or incomplete ISO mount in virtual optical drive

### Step 3: Solution Implementation
1. **Changed Mount Method:** Switched from virtual DVD drive to direct file attachment
2. **Manual Boot Selection:** Used F12 boot menu during VM startup
3. **Selected Correct Boot Device:** Chose hard disk/file boot option instead of optical drive
4. **Successful Boot:** VM properly recognized installation media and proceeded with setup

### Step 4: Validation
- DC01 VM successfully completed Windows Server installation
- No further license or media errors encountered
- System now boots reliably without manual intervention

## Technical Resolution
**Problem:** Virtual optical drive mounting issue with ISO file  
**Solution:** 
- Bypassed virtual DVD emulation
- Used direct file boot method
- Manual boot device selection via F12 menu

## Lessons Learned
- Virtualization media mounting can introduce unexpected issues
- Boot menu (F12) provides manual override for boot device selection
- Multiple boot methods available when primary method fails
- Systematic troubleshooting resolves media recognition problems

## Evidence


**Status:** ✅ Complete

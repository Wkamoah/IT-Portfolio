# Real 001: Laptop Troubleshooting - Boot & Automatic Power-On

**Date:** 04.11.2025
**Objective:** Diagnose and resolve a complex issue involving boot failures and spontaneous power-on events on a colleague's Dell latititude E7450 laptop.

## Problem Description
A colleague reported two distinct but potentially related issues with their Dell laptop:
1.  The laptop would not boot successfully.
2.  The laptop would automatically turn on by itself moments after being shut down.

## Troubleshooting Process

### Phase 1: Diagnosing the Boot Issue
*   **Step 1:** Verified the laptop could boot successfully when manually selected to boot in **UEFI mode** from the one-time boot menu (F12).
*   **Step 2:** Confirmed the boot failure occurred when the system attempted to use the default **Legacy boot mode**.
*   **Step 3:** Identified the root cause: the hard disk was partitioned using the **GPT scheme**, which is only compatible with UEFI firmware. The BIOS was set to Legacy/CSM mode, which requires an MBR-partitioned disk.

### Phase 2: Diagnosing the Automatic Power-On Issue
*   **Step 1:** Checked all common software and BIOS wake triggers:
    *   Verified **Wake-on-LAN** was disabled in BIOS.
    *   Confirmed no **RTC (Real-Time Clock) alarms** were set.
    *   Ran `powercfg -lastwake` in Command Prompt, which reported **0 wake events**, ruling out a software-based wake signal from the OS.
*   **Step 2:** Performed a physical hardware test:
    *   Put the laptop into Sleep mode.
    *   Observed that the power button was unresponsive and did not wake the system, indicating it was stuck in a depressed state, constantly sending an "on" signal.

## Root Cause Analysis
1.  **Boot Failure:** A configuration conflict where the BIOS was set to **Legacy/CSM** boot mode, but the hard drive used a **GPT partition scheme**, which is incompatible.
2.  **Automatic Power-On:** A **mechanical failure of the physical power button**, which was stuck in a pressed position, causing the system to receive a constant "power on" signal.

## Resolution
1.  **For the Boot Issue:** Accessed the BIOS and reconfigured the boot settings:
    *   Changed the **Boot List Option** from `Legacy` to `UEFI`.
    *   **Disabled the Compatibility Support Module (CSM)** to enforce UEFI-only booting.
2.  **For the Power Issue:** As it was a hardware fault, a software/BIOS fix was impossible. The colleague was advised to take the laptop to a repair shop for a **front panel assembly replacement**.

## Verification
*   **Boot:** After BIOS reconfiguration, the laptop booted successfully on the first attempt without needing the boot menu.
*   **Power:** The root cause was conclusively demonstrated to the colleague, who accepted the recommended repair solution.

## Key Learnings
*   The critical relationship between disk partition schemes (GPT/MBR) and firmware boot modes (UEFI/Legacy).
*   A systematic approach to diagnosing power issues, moving from software/BIOS settings to physical hardware testing.
*   How to use `powercfg -lastwake` to rule out operating system wake triggers.

---
**Status:** ✅ Complete

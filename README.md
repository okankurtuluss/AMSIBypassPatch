# AMSIBypassPatch.ps1

## Description

**AMSIBypassPatch.ps1** is a PowerShell script designed to bypass the Antimalware Scan Interface (AMSI) by applying a memory patch to the AmsiScanBuffer function. This script disables AMSI's ability to scan and detect potentially malicious scripts, allowing for uninterrupted execution of PowerShell commands. The script checks the success of the patching process and provides appropriate feedback.

## Usage

### Running the Script

To run the script, open a PowerShell window with administrative privileges and execute the following command:

.\AMSIBypassPatch.ps1

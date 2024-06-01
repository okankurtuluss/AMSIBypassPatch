# AMSIBypassPatch.ps1

## Description

**AMSIBypassPatch.ps1** is a PowerShell script designed to bypass the Antimalware Scan Interface (AMSI) by applying a memory patch to the AmsiScanBuffer function. This script disables AMSI's ability to scan and detect potentially malicious scripts, allowing for uninterrupted execution of PowerShell commands. The script checks the success of the patching process and provides appropriate feedback.

## Usage

### Running the Script

To run the script, open a PowerShell window with administrative privileges and execute the following command:

.\AMSIBypassPatch.ps1

### Script Output
The script will output one of the following messages to indicate the result of the AMSI bypass attempt:

Protection Disabled: Indicates that AMSI has been successfully bypassed.

Failed to Disable Protection: Indicates that the AMSI bypass attempt was unsuccessful.

### Script Details
Function: Disable-Protection

The core functionality of the script is encapsulated in the Disable-Protection function. This function contains embedded C# code that interacts with Windows API functions to apply the memory patch.

### C# Code
The embedded C# code is responsible for:

Obtaining the handle to the amsi.dll module.

Getting the address of the AmsiScanBuffer function within the amsi.dll module.

Changing the memory protection of the AmsiScanBuffer function to allow writing.

Applying a patch to the AmsiScanBuffer function that effectively disables it.

Restoring the original memory protection settings.

### Error Handling
The function checks for errors at each critical step and returns false if any step fails. If all steps are successful, it returns true.

### Disclaimer
This script is intended for educational and authorized testing purposes only. Misuse of this script can result in legal consequences. Ensure you have proper authorization before using this script on any system.

### License
This project is licensed under the MIT License. See the LICENSE file for details.

### Acknowledgments
This script was inspired by various AMSI bypass techniques shared by the security community. Special thanks to all contributors who have shared their knowledge and expertise.

### PoC
test

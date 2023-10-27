## Setting Up NVM on Windows
NVM (Node Version Manager) for Windows is a tool that allows you to easily install, manage, and work with multiple versions of Node.js on Windows.

# Prerequisites
* Ensure you have administrative rights on your computer.
* Uninstall any existing versions of Node.js and npm before installing nvm-windows.

# Installation Steps
1. Uninstall Existing Node.js and npm:
Before installing nvm-windows, it's essential to remove any existing installations to prevent conflicts.
* Open the Control Panel.
* Navigate to Programs and Features.
* Find Node.js in the list, select it, and click Uninstall.

2. Download nvm-windows:
* Visit the GitHub releases page of nvm-windows.
 * Download the latest version of the installer, typically named nvm-setup.zip.
 
3. Install nvm-windows:
* Extract the nvm-setup.zip file.
* Run the extracted nvm-setup.exe to start the installation.
* Follow the on-screen instructions to complete the installation.

4. Verify Installation:
* Open a new Command Prompt or PowerShell window.
* Type:
    ```bash
    nvm version

This should display the version of nvm, confirming the correct installation.

5. Install Node.js using nvm:
    To install a specific version of Node.js:
    ```bash
    nvm install <version>

* To install the latest version of Node.js:
    ```bash
    nvm version latest

6. Set a Default Node.js Version:
   ```bash
    nvm version

7. Verify Node.js and npm Installation:
After setting the Node.js version, you can verify the installation with:
    ```bash
   node -v
   npm -v

8. Switching Between Versions:
To switch between different versions of Node.js, use:
    ```bash
   nvm use <version>

## Troubleshooting
If you encounter the "command not found" error:

1. **Restart Your Terminal or Computer:** Sometimes, a simple restart of the terminal or computer can resolve PATH issues.
2. **Check in a Different Terminal:** Try running the nvm version command in the Command Prompt or PowerShell to see if the issue is terminal-specific.
3. **Ensure nvm is in your PATH:** Ensure that the nvm-windows installation path is added to the system's PATH environment variable.
4. **Reinstall nvm-windows:** If all else fails, consider uninstalling and then reinstalling nvm-windows.

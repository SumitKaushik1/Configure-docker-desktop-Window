# Configure-docker-desktop
## Update Windows 10:

- First, visit the website Windows 10 Download Page.
  - Download the "Windows Update Assistant".
  - Run the downloaded file to update your Windows operating system.
  - Restart your PC after the update completes.
- Enable Windows Subsystem for Linux (WSL):
   - To enable WSL from Command Prompt as Administrator:
      - Press Win + X and choose "Command Prompt (Admin)" or "Windows PowerShell (Admin)".
      - Alternatively, search for "cmd" in the Start menu, right-click on "Command Prompt", and select "Run as administrator".
      - Execute the following command:
      `````sh 
      dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
      `````

      - Restart your computer to apply the changes.
      - Additional Steps for WSL 2:

   - If you want to use WSL 2 for improved performance:
       - Enable the Virtual Machine Platform feature with this command:
       `````sh 
       dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
      ````````
      - Restart your computer again.
      - Set WSL 2 as your default version by running:
      `````sh
        wsl --set-default-version 2
      `````
      - Install a Linux distribution:
      - Search for your desired Linux distribution (e.g., Ubuntu, Debian) in the Microsoft Store and install it.
      - Alternatively, install a distribution from Command Prompt with:

     ````sh
        wsl --install -d Ubuntu
     `````
      - Replace Ubuntu with the name of your preferred Linux distribution.
      -  Username and Password for Ubuntu WSL:

      - After installation, launch your installed Linux distribution (e.g., Ubuntu) from the Start menu.
      - Follow the setup instructions to create a new user account and password for your Linux environment.
   
 ## Download Docker Desktop:

  - Download Docker Desktop from the official Docker website.
   
   - Install Docker Desktop:

      - Open PowerShell as Administrator.
      - Navigate to the directory where Docker Desktop Installer.exe is downloaded.
      - Execute the following command to install Docker Desktop:
 
     `````sh 
     Start-Process 'Docker Desktop Installer.exe' -Wait -Verb RunAs
     ```````
     - Follow any prompts to complete the installation process.
     - These steps should help you set up WSL with Ubuntu, install Docker Desktop, and run it on your Windows machine smoothly. Remember to follow administrative prompts and restart your system as necessary during the process.



## To resolve the issues with Docker Desktop on Windows, follow these steps:

  - Issue 1: An unexpected error was encountered while executing a WSL command
  - Issue 2: Updating WSL: update failed: wsl.exe –update n–web-download not supported
    Uninstall Docker Desktop:

  - If you encounter either of the above errors, start by uninstalling Docker Desktop from your system.
  Free Up Space on C: Drive:

  - Ensure that you have at least 20 GB of free space on your C: drive. You can free up space by moving files from your C: drive to another drive, such as the E: drive, using File Explorer.
  Download Docker Desktop Version 4.31.1:

  - After freeing up space, download Docker Desktop version 4.31.1 (build 153621).
  - Install Docker Desktop:

  - Once downloaded, proceed with the installation of Docker Desktop. This version should run properly after installation.
  - By following these steps, you should be able to resolve the errors and get Docker Desktop running smoothly on your system.

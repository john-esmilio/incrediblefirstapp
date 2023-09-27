Setting Up a React Native Development Environment

System Requirements
Specifications of the system used for this setup:
• CPU: Intel i5-12600KF Processor
• RAM: 32GB DDR4 Memory
• Storage: Minimum 500GB SSD
• Windows Operating System: Windows 11 Home, Version 22H2
• Target OS: Android
Installation Instructions
Install Visual Studio Code

1. Open your web browser and head over to the official Visual Studio Code website.
2. Download Visual Studio Code by clicking on the “Download for Windows” button.
3. After the executable file is downloaded, click on it to start the installation.
4. Agree with the License Agreement and hit Next.
5. Choose the destination location. In this setup, we will leave it at the default location. However, you are welcome to choose where to install Visual Studio Code. Hit Next when you are finished.
6. Select where to select the Start Menu Folder. It is recommended to leave it at the default value. Hit Next when finished.
7. Select additional tasks to be performed. It is recommended to create a desktop icon for easy access to Visual Studio Code. Select the checkbox and leave the default checkbox settings as they are. Hit Next to continue with the installation.
8. Install Visual Studio Code by clicking on the Install button.
9. Wait for the installation to be completed and finish the installation. You may choose to launch the installation or not by selecting the checkbox.
   Install Node.js
   React Native requires the installation of Node.js
10. Head to the official Node.js download page.
11. Click on the latest LTS version of your operating system (18.18.0). This download also includes npm 9.8.1.
12. Download the installer package onto your desktop.
13. Run the installer by double-clicking on the installer and follow the setup wizard with the default values.
14. When the prompt for “Tools for Native Modules” pops up, select the checkbox to install the necessary tools to continue with the installation.

Install the Java SE Development Kit (JDK)
As per stated under the React Native webpage, a JDK is needed to run React Native. It is recommended to use JDK 11, as newer JDK versions may result in problems in React.

1. From the start menu, type “Command Prompt”.
2. Right click on “Command Prompt” and select “Run as Administrator”.
3. Run the following command: choco install -y nodejs-lts Microsoft-openjdk11

Install Android Studio

1. Navigate to the Android Studio website.
2. Click on the “Download Android Studio Giraffe” button to download Android Studio.
3. Accept the Terms and Conditions and download Android Studio.
4. Run the installer and use the default values.
5. While on the installation wizard, make sure the boxes next to all the following items are checked.
   a. Android SDK
   b. Android SDK Platform
   c. Android Virtual Device
   d. If you are not already using Hyper-V: Performance (Intel ® HAXM) (See here for AMD or Hyper-V)
6. Agree with the License Agreement and finish the installation.

Install the Android SDK

1. Open Android Studio, click on “More Actions” and select "SDK Manager”.
2. Select the “SDK Platforms” tab and in the bottom right corner, select the “Show Package Details” checkbox.
3. Under the Android 13 (Tiramisu) entry, ensure the following are selected:
   a. Android SDK Platform 33
   b. Intel x86 System Image or Google APIs Intel x86 Atom System Image
4. Select the “SDK Tools” tab and again, select the “Show Package Details” checkbox in the bottom right corner.
5. Expand the Android SDK Build-Tools menu and ensure that 33.0.0 is selected.
6. Click “Apply” in the bottom right corner to download and install the Android SDK.
7. While still in Android Studio, you can move on to the installation of the android device.
   Install the Android Device
8. If you are still in the Android Studio application, select More Actions, and select Virtual Device Manager.
9. Select Create Device on the top left corner of the window.
10. Select any phone you wish to develop on (we will use the Pixel 3a for this demonstration). Hit Next.
11. Select the Tiramisu API Level 33 system image and click on the download symbol.
12. Click Next and Finish to create your AVD.
    Configuration Steps
    Configure the ANDROID_HOME Environment Variable
13. Open the Windows Control Panel.
14. Click on User Accounts, then click User Accounts again.
15. Click on “Change my environment variables” on the left side of the window.
16. Click “New” and input “ANDROID_HOME” into the Variable name and this value into Variable value: %LOCALAPPDATA%\Android\Sdk
17. Open PowerShell
18. Paste this into PowerShell: Get-ChildItem -Path Env:\
19. Near the top, confirm that ANDROID_HOME is seen at the top.

Add platform-tools to Path

1. Open the Windows Control Panel
2. Click on User Accounts, then click User Accounts again.
3. Click on “Change my environment variables” on the left side of the window.
4. Select the “Path” variable under User variables
5. Select “Edit”
6. Select the “New” button and add this path to the list: %LOCALAPPDATA%\Android\Sdk\platform-tools
   Project Creation
   The steps outlined below will allow you to create a new project using the framework.
7. Open Visual Studio Code.
8. In the top left corner, Click on File, then Open Folder.
9. Create a folder for your new project to be created in. For this demo, we can name the folder “NewProject”.
10. Open the terminal by holding “Ctrl + Shift + `” or on the top left, Terminal -> New Terminal.
11. The terminal will pop up at the bottom of the window.
12. Enter this prompt into the terminal: npx react-native init incrediblefirstapp
    a. Incrediblefirstapp will be the project name you will create for your first project.
13. The terminal will ask to install the following packages. Hit Y and press enter to continue.
14. When the packages and dependencies are finished installing, enter cd incrediblefirstapp into the terminal.
15. Keep Visual Studio Code open and you can move onto running the project on Android Studio.
    Running the Project
16. Open Android Studio to run your React Native Android App.
17. Select More Actions and select the play button on the Pixel 3a device you created.
18. Go back to Visual Studio Code and enter this into the terminal: npx react-native run-android. This will launch the emulator on the virtual Android device.
19. Command prompt will launch the emulator automatically. Hit the “a” key to run the emulator on android.
20. Once you see “Welcome to React Native” on your virtual device, you did it!
    Troubleshooting
    • Read the error messages carefully. Error messages often contain details to address the problem.
    • Ensure your virtual Android Device is running.
    • React Native has a built-in tool to debug. Press Ctrl + M on the device to open the React Native debug menu.
    • Check if your version of Node.js is up to date.
    Resources
    • React Native Documentation
    • Setting up the Development Environment
    • React Native Troubleshooting
    • Android Studio Documentation
    • Android Studio Troubleshooting

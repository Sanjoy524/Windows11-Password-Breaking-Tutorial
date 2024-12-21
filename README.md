# Unlock Your Windows 11 PC and Recover Your Account Tutorial

Welcome to the comprehensive guide on unlocking your Windows 11 PC and recovering your account if you have forgotten your password or PIN. This repository is designed to help users who are locked out of their devices and need to regain access quickly and efficiently. Whether you are a tech novice or a seasoned user, this guide provides clear, step-by-step instructions, resources, and troubleshooting tips to assist you through the process.

## Step 1: Boot into Advanced Boot Options
- Restart your computer.
- While the Windows logo appears, press and hold the power button to force a shutdown.
- Repeat this process twice.
- On the third start, Windows should enter the Automatic Repair environment.

## Step 2: Access Command Prompt
- From the Automatic Repair environment, navigate to **Troubleshoot** > **Advanced options** > **Command Prompt**.

## Step 3: Create a New Administrator Account
- At the Command Prompt, type the following commands and press Enter after each one:
  ```plaintext
  c:
  cd windows\system32
  ren utilman.exe utilman.exe.bak
  copy cmd.exe utilman.exe
  wpeutil reboot
## Step: If utilman.exe is missing, try these commands instead:
- At the Command Prompt, type the following commands and press Enter after each one:
  ```plaintext
  c:
  cd windows\system32
  ren sethc.exe sethc.exe.bak
  copy cmd.exe sethc.exe
  wpeutil reboot

```markdown
# Unlock Your Windows 11 PC and Recover Your Account Tutorial

Welcome to the comprehensive guide on unlocking your Windows 11 PC and recovering your account if you have forgotten your password or PIN. This repository is designed to help users who are locked out of their devices and need to regain access quickly and efficiently. Whether you are a tech novice or a seasoned user, this guide provides clear, step-by-step instructions, resources, and troubleshooting tips to assist you through the process.

## Table of Contents
- [Disclaimer](#disclaimer)
- [Prerequisites](#prerequisites)
- [Step 1: Boot into Advanced Boot Options](#step-1-boot-into-advanced-boot-options)
- [Step 2: Access Command Prompt](#step-2-access-command-prompt)
- [Step 3: Create a New Administrator Account](#step-3-create-a-new-administrator-account)
- [Step 4: Access Command Prompt on Login Screen](#step-4-access-command-prompt-on-login-screen)
- [Step 5: Create a New User](#step-5-create-a-new-user)
- [Step 6: Regain Access to Previous Account](#step-6-regain-access-to-previous-account)
- [Step 7: Reset Password via Command Prompt](#step-7-reset-password-via-command-prompt)

## Disclaimer
This tutorial is intended for educational purposes only. Use it responsibly and only on computers you own or have permission to access.

## Prerequisites
- A Windows 11 PC that you are locked out of.
- Basic knowledge of using the Command Prompt.

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
  ```
- If `utilman.exe` is missing, try these commands instead:
  ```plaintext
  c:
  cd windows\system32
  ren sethc.exe sethc.exe.bak
  copy cmd.exe sethc.exe
  wpeutil reboot
  ```

## Step 4: Access Command Prompt on Login Screen
- On the login screen, click the Utility Manager icon, or press the Shift key five times quickly to open Command Prompt with administrative privileges.

## Step 5: Create a New User
- Type these commands:
  ```plaintext
  net user username password /add
  net localgroup administrators username /add
  ```
  Replace 'username' and 'password' with your desired username and password.
- Then, restart your computer and log in with the new account.

## Step 6: Regain Access to Previous Account
- Open User Accounts by pressing `Win + R`, type `control userpasswords2` or `netplwiz`, and press Enter.
- Select your previous account, click on Reset Password, and enter a new password.
- Log out of the current account and sign in with your previous account using the new password.

## Step 7: Reset Password via Command Prompt
- Open Command Prompt (Admin) by right-clicking the Start button and selecting "Command Prompt (Admin)" or "Windows PowerShell (Admin)".
- Type:
  ```plaintext
  net user username newpassword
  ```
  Replace 'username' with your previous account's username and 'newpassword' with the new password you want to set.


---
title : Set Kali root password and enable root login
date : 2024-06-25 1:00:00 +07:00
tags : [ "Kali", "Linux", "Root", "Password"]
categories : [ "Linux" ]

---

# Set Kali root password and enable root login

![kali-root-login](assets/root-login.png){: width="600" height="400" }

To enable root login for Kali Linux, we must manually set the root password. In past versions of Kali Linux, users could log in directly to the root account by default. On more recent versions, this has been disabled. The developers of Kali have made it incredibly easy to re-enable the root login. Follow the steps below to enable root login and log in to the GUI as root.

## Step-by-Step Process to Enable Root Login

### Step 1: Install kali-root-login Package

First, use the apt package manager to install the `kali-root-login` package.

    sudo apt update
    sudo apt install kali-root-login

![kali-root-login](assets/kali-root-login 1.png)

### Step 2: Set the Root Password
Next, you need to set the root password using the `passwd` command. Setting it to the current password of your user account is fine, but this command must be run.
    
    sudo passwd 
    [Enter password twice]

![kali-root-login](assets/kali-root-login 2.png)

### Step 3: Return to the Login Screen
You can return to the login screen by switching users, logging out, or restarting the system.

![kali-root-login](assets/kali-root-login 3.png)

### Step 4: Log in as Root Account
Login with the root user account and the password you set in the previous steps.

![kali-root-login](assets/kali-root-login 4.png)
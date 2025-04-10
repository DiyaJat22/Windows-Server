# 🛠️ How to Install Active Directory Domain Services (AD DS) on Windows Server 2022

This guide outlines the step-by-step process to install and configure **Active Directory Domain Services (AD DS)** on **Windows Server 2022**.

---

## ✅ Step 1: Prepare Windows Server 2022

- **Install Windows Server 2022**: Ensure Windows Server 2022 is properly installed on your machine.
- **Configure Network Settings**: Set up a static IP address and confirm the server is properly connected to the network.

---

## 🔧 Step 2: Open Server Manager

- **Launch Server Manager**: Open **Server Manager** from the Start Menu. It is the main tool for managing roles and features in Windows Server.

---

## ➕ Step 3: Add AD DS Role

- Click **"Manage"** in Server Manager.
- Select **"Add Roles and Features"**.

- In the **Installation Type** section, choose:
  - `Role-based or feature-based installation`, then click **Next**.

- In the **Server Selection** step:
  - Select the local server from the list and click **Next**.

---

## 🧱 Step 4: Select AD DS Role

- Under **Server Roles**, check the box for **Active Directory Domain Services**.
- A dialog box will prompt to add required features.
  - Click **Add Features**, then **Next**.

---

## 📦 Step 5: Add Features

- On the **Features** page, leave default options unless specific features are needed.
- Click **Next**.

---

## ℹ️ Step 6: AD DS Role Overview

- Read the brief about AD DS.
- Click **Next** to continue.

---

## ✅ Step 7: Confirm Installation

- Review your selections.
- Click **Install** to begin installing AD DS.

---

## 🧭 Step 8: Post-Installation Configuration

- Once installation is complete, click **"Promote this server to a domain controller"** (a yellow warning will appear in Server Manager).

- In **Deployment Configuration**:
  - Select **"Add a new forest"** (if you're creating a new domain).
  - Enter your **Root domain name** (e.g., `example.local`).
  - Click **Next**.

---

## 🔐 Step 9: Configure Domain Controller Options

- Set the **Directory Services Restore Mode (DSRM) password**.
- Choose the required options (typically leave default selected).
- Click **Next**.

---

## 🌐 Step 10: Configure DNS

- DNS options will appear (you can leave them as is unless customization is needed).
- Click **Next**.

---

## 📋 Step 11: Review Settings

- Review all configuration settings.
- Click **Next** to proceed.

---

## 🖥️ Step 12: Complete Installation

- Click **Install** to finalize the configuration.
- Once completed, the server may prompt for a **restart** — allow it to reboot.

---

## 🎉 Summary

By following these steps, you will have successfully installed and configured **Active Directory Domain Services (AD DS)** on **Windows Server 2022**.

For visual learners, you can refer to detailed **YouTube tutorials** in **Hindi** for a clearer understanding of the process.

---

Let me know if you want a diagram or lab setup to go with this `.md` file!

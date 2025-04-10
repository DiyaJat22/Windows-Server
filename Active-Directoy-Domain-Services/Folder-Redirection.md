# 📁 What is Folder Redirection?

**Folder Redirection** is a technique used in Microsoft Windows operating systems to redirect user folders to a network location.  
It is especially useful in office network environments to centralize and protect user data.

---

# ⚙️ How is Folder Redirection Used?

## 1. Through Group Policy:
- Folder Redirection is typically implemented using **Group Policy** in Active Directory.
- Administrators create a policy that specifies which folders (like Documents, Desktop) should be redirected and where.

## 2. On User Interface:
- When users log in to their computers, the specified folders are automatically redirected to the network location.
- Users can interact with the files just like they would on their local drive, even though the data resides on a server.

---

# ✅ Benefits of Folder Redirection

- **Data Security**: Data is stored on the server, making it more secure compared to local storage.
- **Shared Data**: If the same redirection policy applies to multiple users, their data is stored in a centralized location, making sharing easier.
- **Backup Support**: Since the data is stored on a server, it can be backed up regularly, minimizing the risk of data loss.
- **Faster Login Times**: Redirected folders reduce the need to load large local profiles, speeding up the login process.

---

# 🏢 Example: Using Folder Redirection in ABC Technologies

## Scenario:
- ABC Technologies is a large organization with multiple employees.
- The company wants all employees’ **Documents** and **Desktop** folders to be stored on a centralized server for better security and easier backups.

---

# 🛠️ Steps to Configure Folder Redirection using Group Policy

This guide explains the step-by-step process to set up **Folder Redirection** in a Windows domain environment using **Group Policy Management Console (GPMC)**.

---

## 🥇 Step 1: Open Group Policy Management Console (GPMC)
- Press `Windows + R`, type `gpmc.msc`, and hit **Enter**.
- GPMC will open where you can manage Group Policy Objects (GPOs).

---

## 🥈 Step 2: Create a New Group Policy Object (GPO)
- Right-click on the **Organizational Unit (OU)** or domain where you want to apply the policy.
- Select **"Create a GPO in this domain, and Link it here…"**.
- Name the GPO (e.g., `"Folder Redirection Policy"`).

---

## 🥉 Step 3: Edit the GPO
- Right-click the newly created GPO and choose **"Edit"**.
- Navigate to:

User Configuration → Policies → Windows Settings → Folder Redirection


---

## 🏗️ Step 4: Choose the Folder to Redirect
- Right-click on a folder like **Documents**, **Desktop**, etc.
- Select **"Properties"**.

---

## ⚙️ Step 5: Configure Redirection Settings
- In the **Target tab**:
- Set **Setting** to: `Basic – Redirect everyone’s folder to the same location`.
- Under **Target folder location**, choose: `Redirect to the following location`.
- In **Root Path**, enter a shared network path, e.g.:
  ```
  \\ServerName\Users\%USERNAME%\Documents
  ```

---

## 🔐 Step 6: Set Permissions (Optional but Recommended)
- Ensure the destination shared folder on the server has appropriate **NTFS and Share permissions**.
- Example: `Everyone: Read`, `Authenticated Users: Modify`, `Administrators: Full Control`.

---

## 💾 Step 7: Apply and Close
- Click **Apply** and **OK**.
- Close the Group Policy Editor.

---

## 🖥️ Step 8: Test the Policy
- On a client computer, run:

gpupdate /force

- Log off and log back in to see if folder redirection is applied.
- Check if files saved in the folder (e.g., Documents) are now stored on the server path.

---

## ✅ Folder Redirection is Now Configured!
- Users' selected folders will now automatically redirect to the designated network path.
- Data is safer, centrally managed, and easier to back up.



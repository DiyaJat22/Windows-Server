# Add Group Policy to Sales OU in Windows Server

This guide explains how to create and apply a Group Policy Object (GPO) to the Sales OU using Group Policy Management Console (GPMC) on Windows Server.

---

## 🚀 Steps to Add GPO to Sales OU

1. **Open GPMC**  
   - Press `Windows + R`, type `gpmc.msc`, and hit Enter.

2. **Navigate to Sales OU**  
   - In the GPMC console, expand your domain (e.g., `example.local`).  
   - Locate and select the **Sales** Organizational Unit.

3. **Create a New GPO**  
   - Right-click on the Sales OU and select  
     `"Create a GPO in this domain, and Link it here..."`  
   - Name the GPO, e.g., `Sales Policy`.

4. **Edit the GPO**  
   - Right-click the newly created GPO → Click **Edit**.  
   - In **Group Policy Management Editor**, set your desired policy.  
     (e.g., configure desktop wallpaper, folder redirection, or disable control panel access.)

5. **Apply the Policy**  
   - Close the editor to save changes.  
   - The GPO is now linked to the Sales OU.

6. **Force Update on Client (Optional)**  
   - On a client machine in the Sales OU, run:  
     `gpupdate /force` in Command Prompt.

7. **Verify Application**  
   - Use `gpresult /r` to confirm that the GPO is applied.

---

✅ Now your GPO is successfully applied to all users and computers in the Sales OU.

# 🛡️ Top 10 Group Policies in Windows Server (Described)

Group Policy is a powerful feature in Windows Server that allows administrators to control user and computer configurations in an Active Directory environment. Below are the top 10 essential policies, explained in detail.

---

## 1. Password Policy
**Path**: `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy`  
**Description**:  
- Enforces strong password requirements.
- Parameters include:
  - Minimum password length.
  - Complexity requirements (uppercase, numbers, symbols).
  - Password history and expiration duration.
**Purpose**: Enhances security by enforcing strong authentication practices.

---

## 2. Account Lockout Policy
**Path**: `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy`  
**Description**:  
- Locks a user account after a set number of failed login attempts.
- Includes settings for lockout duration and reset time.
**Purpose**: Prevents brute-force attacks and unauthorized access.

---

## 3. Folder Redirection
**Path**: `User Configuration > Policies > Windows Settings > Folder Redirection`  
**Description**:  
- Redirects user folders like Documents, Desktop to a network location.
- Ensures data is stored on a central server rather than on local machines.
**Purpose**: Simplifies backups, improves data security, and enhances roaming profile performance.

---

## 4. Disable USB Storage Access
**Path**: `Computer Configuration > Administrative Templates > System > Removable Storage Access`  
**Description**:  
- Disables use of USB drives and storage devices.
- Can block read/write or completely deny access.
**Purpose**: Prevents data leakage and insertion of malware through USB.

---

## 5. Windows Firewall Configuration
**Path**: `Computer Configuration > Policies > Windows Settings > Security Settings > Windows Firewall`  
**Description**:  
- Sets default behavior for Windows Firewall.
- Allows or blocks specific applications or ports.
**Purpose**: Helps manage network traffic and improve system security.

---

## 6. Audit Logon Events
**Path**: `Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Audit Policy`  
**Description**:  
- Logs successful and failed login attempts.
- Helps track user behavior and identify security incidents.
**Purpose**: Crucial for security auditing and forensics.

---

## 7. Set Desktop Wallpaper
**Path**: `User Configuration > Administrative Templates > Desktop > Desktop`  
**Description**:  
- Forces a standard desktop wallpaper for all users.
- Often used for branding or compliance notices.
**Purpose**: Provides visual consistency and discourages personalization in professional settings.

---

## 8. Disable Control Panel and Settings Access
**Path**: `User Configuration > Administrative Templates > Control Panel`  
**Description**:  
- Restricts users from accessing or changing system settings via the Control Panel.
**Purpose**: Prevents users from making unauthorized or risky configuration changes.

---

## 9. Time Synchronization Policy
**Path**: `Computer Configuration > Administrative Templates > System > Windows Time Service > Time Providers`  
**Description**:  
- Ensures all systems sync with the same time server.
**Purpose**: Maintains consistency in event logs and authentication protocols.

---

## 10. BitLocker Drive Encryption
**Path**: `Computer Configuration > Administrative Templates > Windows Components > BitLocker Drive Encryption`  
**Description**:  
- Enforces encryption of system and data drives using BitLocker.
**Purpose**: Protects data in case of device theft or unauthorized access.

---

🧠 **Note**: These Group Policies should be deployed based on the needs of the organization and tested in a controlled environment before full deployment.


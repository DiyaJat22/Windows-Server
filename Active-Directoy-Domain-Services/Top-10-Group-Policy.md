# Top 10 Group Policies in Windows Server

This document outlines the top 10 essential Group Policies used in a Windows Server environment, especially within enterprise networks to manage and secure computers and users.

---

## 1. **Account Lockout Policy**
- **Purpose**: Prevent brute-force attacks by locking out user accounts after a certain number of failed login attempts.
- **Settings**:
  - Account lockout threshold
  - Account lockout duration
  - Reset account lockout counter

---

## 2. **Password Policy**
- **Purpose**: Enforce secure password practices among users.
- **Settings**:
  - Minimum password length
  - Password complexity requirements
  - Maximum and minimum password age

---

## 3. **Audit Policy**
- **Purpose**: Keep track of security-related events such as logon attempts, object access, and system changes.
- **Settings**:
  - Audit logon events
  - Audit account management
  - Audit policy change

---

## 4. **Software Restriction Policy**
- **Purpose**: Prevent the execution of unauthorized applications.
- **Use Cases**:
  - Define trusted locations for executable files
  - Block execution of applications from unknown paths

---

## 5. **User Rights Assignment**
- **Purpose**: Assign specific privileges to users or groups.
- **Examples**:
  - Log on locally
  - Shut down the system
  - Access this computer from the network

---

## 6. **Windows Firewall Settings**
- **Purpose**: Configure firewall rules for inbound and outbound connections.
- **Settings**:
  - Enable/Disable firewall
  - Define inbound/outbound rules
  - Allow apps through firewall

---

## 7. **BitLocker Drive Encryption**
- **Purpose**: Protect sensitive data by encrypting drives.
- **Settings**:
  - Require additional authentication at startup
  - Choose drive encryption method

---

## 8. **Disable Removable Storage Access**
- **Purpose**: Prevent data leakage through USB drives and other removable devices.
- **Settings**:
  - Deny read/write access to removable storage
  - Disable autorun on removable media

---

## 9. **Security Options**
- **Purpose**: Fine-tune system-level security configurations.
- **Examples**:
  - Admin approval mode for UAC
  - Do not store LAN Manager hash value
  - Network security: LAN Manager authentication level

---

## 10. **Folder Redirection**
- **Purpose**: Redirect user folders (Documents, Desktop) to a network location.
- **Benefits**:
  - Centralized data management
  - Easier backups
  - Access data from any domain-connected device

---

## Conclusion

These group policies play a crucial role in enhancing security, compliance, and manageability of systems in a Windows domain environment. Proper planning and implementation of these policies are essential for a robust IT infrastructure.

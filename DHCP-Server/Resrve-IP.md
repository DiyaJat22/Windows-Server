# DHCP Reserved IP Address Configuration

A **reserved IP address** ensures that a specific device always receives the same IP address from the DHCP server based on its **MAC address**. This is useful for printers, servers, or other critical devices that need a consistent IP.

---

## 🛠️ When to Use IP Reservation?

- When a device (e.g., printer, server, CCTV, etc.) should **always have the same IP address**
- Ensures **consistent connectivity**
- Useful for **port forwarding**, **remote access**, or **network monitoring**

---

## 🔧 Steps to Configure DHCP IP Reservation (Windows Server)

### Step 1: Open DHCP Management Console

1. Go to:  
   `Start` → `Administrative Tools` → `DHCP`

2. Expand your DHCP server node:  
   `DHCP` → `IPv4` → your scope (e.g., `LAN Scope`)

---

### Step 2: Add Reservation

1. Right-click on `Reservations` under the desired scope  
2. Click **New Reservation**

---

### Step 3: Fill in Reservation Details

In the **New Reservation** window:

- **Reservation Name:**  
  Give it a meaningful name (e.g., `Printer-Office`, `Server-01`)

- **IP Address:**  
  Choose the IP address you want to reserve (must be within the scope's range but not currently leased to another device)

- **MAC Address:**  
  Enter the client device’s **physical address (MAC)** without dashes or colons  
  _(e.g., 00A1B2C3D4E5)_

- **Description (optional):**  
  Add any relevant notes

- **Supported Types:**  
  Choose `Both` for DHCP and BOOTP unless you have a specific use case

3. Click **Add** to save the reservation

---

### Step 4: Verify & Reconnect Client

1. Make sure the client device is **disconnected and reconnected** to the network  
2. On the client, run:  
   `ipconfig /release`  
   then  
   `ipconfig /renew`  
   or simply restart the network interface

3. Use `ipconfig` to confirm the **reserved IP address** is assigned

---

## 📌 Note

- The reservation only works if the **MAC address is correct**
- Ensure the IP address is **not part of the active lease pool**, or it may cause conflicts
- Reserved IPs still go through the **DORA process**, but always receive the same address

---

## ✅ Benefits of IP Reservation

- **Consistent IP address** for critical devices
- Avoids **manual static IP configuration**
- Simplifies **network management and troubleshooting**
- Essential for **network printers**, **servers**, **VoIP phones**, etc.

---

## 🧠 Example Use Case

| Device         | IP Address   | MAC Address        | Purpose              |
|----------------|--------------|---------------------|----------------------|
| Printer-HP1010 | 192.168.1.50 | 00A1B2C3D4E5        | Office printer       |
| CCTV-FrontGate | 192.168.1.60 | 00B3C4D5E6F7        | Security camera      |
| NAS-Storage    | 192.168.1.100| 00C5D6E7F8G9        | File storage server  |

---

## 🔚 Conclusion

**DHCP reservations** allow for centralized control of IP address assignments while maintaining the flexibility of DHCP. This ensures that important devices always get the same IP without the hassle of configuring static addresses manually.


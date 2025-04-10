# DHCP Scope Creation – Windows Server

A **DHCP Scope** is a range of IP addresses that the DHCP server can assign to clients on a specific subnet. Setting up a scope is essential for enabling automatic IP configuration in a network.

---

## 🛠️ Steps to Create a DHCP Scope

### ✅ Step 1: Open the DHCP Management Console

1. Go to:  
   `Start` → `Administrative Tools` → `DHCP`
2. Expand the server node under `IPv4`

---

### ✅ Step 2: Start New Scope Wizard

1. Right-click on `IPv4`
2. Select **"New Scope"**
3. The **New Scope Wizard** will open  
4. Click **Next** to continue

---

### ✅ Step 3: Scope Name and Description

- **Name:** e.g., `Office LAN`
- **Description (optional):** e.g., `Main Office DHCP Scope`

Click **Next**

---

### ✅ Step 4: Define IP Address Range

- **Start IP Address:** `192.168.1.10`
- **End IP Address:** `192.168.1.200`
- **Subnet Mask:** Enter automatically or specify (e.g., `255.255.255.0`)

Click **Next**

---

### ✅ Step 5: Add Exclusions (Optional)

- Add any **IP addresses to exclude** from the scope  
  (e.g., `192.168.1.1 to 192.168.1.5` for routers or printers)

Click **Next**

---

### ✅ Step 6: Lease Duration

- Set the **duration of the IP lease** (default: 8 days)
- You can adjust this based on your network's needs

Click **Next**

---

### ✅ Step 7: Configure DHCP Options

Choose:
- **Yes, I want to configure these options now** → Click **Next**

Enter:
- **Router (Default Gateway):** e.g., `192.168.1.1`
- **DNS Servers:** e.g., `8.8.8.8`, `8.8.4.4`
- **WINS Server** (if used)

Click **Next** through each option and finish

---

### ✅ Step 8: Activate the Scope

- Select **"Yes, I want to activate this scope now"**
- Click **Next** and then **Finish**

---

## 📌 Example Configuration

| Setting             | Value                    |
|---------------------|--------------------------|
| Scope Name          | Office LAN               |
| IP Range            | 192.168.1.10 – 192.168.1.200 |
| Subnet Mask         | 255.255.255.0            |
| Exclusions          | 192.168.1.1 – 192.168.1.5 |
| Lease Duration      | 8 days                   |
| Gateway             | 192.168.1.1              |
| DNS Servers         | 8.8.8.8, 8.8.4.4         |

---

## ✅ Scope Successfully Created!

Once activated, the DHCP server will begin assigning IP addresses from the defined scope to DHCP clients on the network.

---

## 📎 Notes

- You can create **multiple scopes** for different subnets
- Always **exclude** IPs reserved for static assignments
- Monitor scope usage to avoid IP shortages


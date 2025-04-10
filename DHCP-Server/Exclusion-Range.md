# DHCP Exclusion Range Configuration

In DHCP, an **exclusion range** is a set of IP addresses within the defined DHCP scope that the server is instructed **not to assign** to clients. These addresses are excluded from the dynamic pool and are often used for static IP devices or special purposes.

---

## 🧠 Why Use Exclusion Ranges?

- To **reserve IP addresses** for servers, printers, routers, or other critical devices
- To **prevent conflicts** between statically assigned and dynamically assigned IPs
- To organize IP address usage efficiently within the network

---

## 🛠️ Steps to Configure DHCP Exclusion Range (Windows Server)

### Step 1: Open DHCP Management Console

1. Go to:  
   `Start` → `Administrative Tools` → `DHCP`

2. Expand your DHCP server node:  
   `DHCP` → `IPv4` → your scope (e.g., `LAN Scope`)

---

### Step 2: Add an Exclusion Range

1. Right-click on your **DHCP Scope**
2. Click **New Exclusion Range**

---

### Step 3: Define the Range

- **Start IP Address:**  
  Enter the first IP address you want to exclude (e.g., `192.168.1.1`)

- **End IP Address:**  
  Enter the last IP address in the exclusion range (e.g., `192.168.1.10`)

> ✅ If you only want to exclude a single IP, set the start and end IP to the same address.

3. Click **Add** to apply the exclusion range

---

## 📌 Example

| DHCP Scope Range     | 192.168.1.1 – 192.168.1.200 |
|----------------------|-----------------------------|
| Exclusion Range      | 192.168.1.1 – 192.168.1.20  |
| Usable by DHCP       | 192.168.1.21 – 192.168.1.200|

- In this example, DHCP will **not assign IPs from 1 to 20**, which can be used for static devices

---

## 🔧 Modify or Remove Exclusion

- To modify an exclusion range:  
  Delete the existing range and create a new one

- To remove an exclusion range:  
  Right-click the range under `Address Pool` → `Delete`

---

## ✅ Best Practices

- Exclude IPs for **default gateways, printers, and servers**
- Plan your IP ranges in a **logical and documented** way
- Keep dynamic and static addresses **clearly separated**

---

## 🧠 Tip

Use IP addresses **outside of the exclusion range** for DHCP reservations, unless you're manually managing static IPs on those devices.

---

## 🔚 Conclusion

Exclusion ranges in DHCP ensure that specific IP addresses are not dynamically assigned. This provides **greater control**, avoids IP conflicts, and supports **organized network infrastructure**.




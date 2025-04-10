# DHCP Server Configuration on Windows Server

Follow the steps below to install and configure a DHCP (Dynamic Host Configuration Protocol) server on a Windows Server machine.

---

## Step 1: Install the DHCP Server Role

1. **Open Server Manager**:  
   Navigate to:  
   `Start -> Administrative Tools -> Server Manager`

2. **Click on "Add Roles and Features"**

3. Select **"Role-based or feature-based installation"**, then click **Next**.

4. **Select the server** on which you want to install the DHCP role.

5. In the **"Server Roles"** section, check **"DHCP Server"**, then click **Next**.

6. A prompt will appear to add required features. Click **"Add Features"**.

7. Review your selections and click **"Install"** to begin the installation.

> 💡 **Explanation**: The DHCP Server role is necessary to assign IP addresses dynamically to client machines in your network.

---

## Step 2: Configure the DHCP Server

1. **Open the DHCP Management Console**:  
   Navigate to:  
   `Start -> Administrative Tools -> DHCP`

2. **Create a New DHCP Scope**:
   - Right-click on **"DHCP"** and choose **"New Scope"**
   - Enter a **name** (e.g., `LAN Scope`)
   - Define an **IP address range** (e.g., `192.168.1.10` to `192.168.1.200`)
   - Enter the **Subnet Mask** (e.g., `255.255.255.0`)
   - Set the **Lease Duration** (default is 8 days)
   - Click **Next**, and configure any additional options if needed

> 💡 **Explanation**: A *scope* defines the range of IP addresses the DHCP server can assign to clients on a specific subnet.

3. **Configure DHCP Options**:
   - Navigate to `DHCP -> IPv4 -> Server Options`
   - Right-click and select **"Configure Options"**
     - **Option 3 (Router)**: Enter the default gateway IP (e.g., `192.168.1.1`)
     - **Option 6 (DNS Server)**: Enter the IP of your DNS server (e.g., `8.8.8.8`)
     - Configure any other necessary options
     - Click **OK**

> 💡 **Explanation**: DHCP Options help configure network settings like Gateway, DNS, etc., automatically for clients.

4. **Activate the DHCP Scope**:
   - Right-click on the newly created **Scope** under `DHCP -> IPv4 -> Scopes`
   - Select **"Activate"**

> ✅ This enables the DHCP server to start leasing IP addresses within the defined range.

---

## Step 3: Configure the DHCP Client

1. **Open Network Adapter Properties**:
   - Right-click on the **Network Connection** icon → **Properties**
   - Select **"Internet Protocol Version 4 (TCP/IPv4)"** → Click **Properties**

2. **Set to Use DHCP**:
   - Select:
     - `Obtain an IP address automatically`
     - `Obtain DNS server address automatically`
   - Click **OK** to apply the settings

3. **Renew the IP Address** (optional):
   - Open **Command Prompt**
   - Run:
     ```bash
     ipconfig /renew
     ```

> 💡 **Explanation**: These settings allow the client device to request and receive an IP address from the DHCP server dynamically.

---

## Additional Features

- ### **DHCP Server Logs**
  You can enable and review logs that track all DHCP-related activities, such as assigned IPs and request logs.

- ### **DHCP Filters**
  Configure filters to allow or deny DHCP access based on **MAC addresses** or **Client IDs** for security and control.

- ### **DHCP Classes**
  DHCP Classes allow you to assign different configurations (e.g., different IP ranges) based on the type or group of client devices.

---

## Conclusion

Configuring a DHCP server on Windows Server is a straightforward and essential task for efficient network management. By automating IP address assignment and providing centralized configuration, DHCP significantly reduces administrative overhead and minimizes errors in network configuration.

It also enhances scalability and control, especially in enterprise networks where hundreds of devices may need IP addresses dynamically.

---

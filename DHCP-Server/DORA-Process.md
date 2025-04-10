# DORA Process in DHCP

The **DORA process** is the sequence of steps used by the **Dynamic Host Configuration Protocol (DHCP)** to assign an **IP address** to a client device on a network. It consists of four key steps:

---

## 1️⃣ Discover (D) – DHCP Discover

When a client (such as a computer, phone, or printer) connects to a network and needs an IP address, it sends a **DHCP Discover** message.

- This is a **broadcast message** because the client doesn’t yet have an IP address.
- The message is sent to **255.255.255.255** or the subnet’s broadcast address.
- It is looking for any available **DHCP server** to respond.

💡 **Example:** When you connect your laptop to Wi-Fi, it automatically sends a request to obtain an IP address.

---

## 2️⃣ Offer (O) – DHCP Offer

When a **DHCP server** receives the Discover message, it checks its pool of available IP addresses and sends a **DHCP Offer** message back to the client.

This message contains:
- An **available IP address**
- **Subnet mask**
- **Default gateway**
- **DNS server address**
- **Lease time** (how long the IP address will remain valid)

- This message is usually sent as **unicast** or **broadcast**, depending on the network setup.

💡 **Example:** When you join your office network, the DHCP server offers you a suitable IP address.

---

## 3️⃣ Request (R) – DHCP Request

The client receives **one or more** DHCP Offers (if multiple DHCP servers respond) and selects one. It then sends a **DHCP Request** message back to the selected server.

- The message tells the server that the client **accepts** the offered IP address.
- It also notifies other DHCP servers that their offers are declined.

💡 **Example:** If multiple DHCP servers exist on a network, the client picks one offer and sends a request for that IP address, rejecting the rest.

---

## 4️⃣ Acknowledge (A) – DHCP Acknowledgment (ACK)

The DHCP server responds with a **DHCP ACK** message, confirming the lease of the IP address to the client.

- The client is now assigned an IP address and can communicate on the network.
- The **lease timer** starts from this point.
- If the server cannot assign the requested IP (e.g., it was already leased), it sends a **DHCP NAK (Negative Acknowledgment)** instead, forcing the client to restart the DORA process.

💡 **Example:** When your smartphone connects to Wi-Fi, it receives a valid IP address and can now browse the internet.

---

## ✅ Summary of the DORA Process

| Step        | Message Type | Sender     | Purpose                                       |
|-------------|---------------|------------|-----------------------------------------------|
| Discover    | Broadcast      | Client     | To locate available DHCP servers              |
| Offer       | Unicast/Broadcast | Server     | To offer an available IP address               |
| Request     | Broadcast      | Client     | To request the offered IP and confirm choice  |
| Acknowledge | Unicast        | Server     | To confirm assignment and provide configuration |

---

## 🧠 Conclusion

The **DORA process** is an efficient and structured method used in networking to **automatically assign IP addresses** using DHCP. It simplifies network administration and ensures devices receive valid configurations without manual setup.


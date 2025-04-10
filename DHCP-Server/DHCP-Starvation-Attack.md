## What is DHCP?

**DHCP** (Dynamic Host Configuration Protocol) is a protocol that automatically assigns IP addresses to devices (like computers, printers) on a network. When you connect your computer to a network, the DHCP server provides an IP address so the device can communicate with the internet or other devices on the network.

## What is a DHCP Starvation Attack?

A **DHCP Starvation Attack** is a type of cyberattack. In this attack, an attacker tricks the DHCP server and exhausts all the available IP addresses. When all IP addresses are consumed, new devices cannot connect to the network.

## How does this attack work?

1. **What the attacker does**:
   - The attacker uses a program to send a large number of DHCP Discover messages to the DHCP server. These messages appear normal, but the attacker uses different MAC addresses.
   - For example, the attacker may send 1000 bogus messages, making the DHCP server believe that 1000 different devices are requesting IP addresses.

2. **What the DHCP server does**:
   - The DHCP server responds to each of these messages and assigns all the available IP addresses.
   - Suppose the DHCP server has 254 IP addresses. Once all are assigned, no IP addresses remain.

3. **What happens next**:
   - When a new user (e.g., a new computer) tries to connect to the network, it doesn't receive an IP address because none are available on the DHCP server.
   - This results in the user being unable to connect to the network. This situation is known as a **Denial of Service (DoS)** — meaning the service becomes unavailable.

## Simple Example

- **Your office**: Imagine your office has a DHCP server operating on the 192.168.1.0 network with 254 IP addresses.
- **The attacker**: A person (attacker) uses a program to send thousands of DHCP Discover messages.
- **DHCP server**: The server assigns all the IP addresses.
- **New computer**: When a new computer tries to connect to the network, there are no IP addresses left, so it can't connect.

## How to prevent this attack

1. **Port Security**: Apply port security on switches so that only a limited number of MAC addresses are allowed per port.

2. **DHCP Snooping**: A security feature that allows messages only from trusted DHCP servers.

3. **Network Monitoring**: Regularly monitor the network to detect suspicious activity.

## Conclusion

A DHCP Starvation Attack is a serious issue that can disrupt network services. Implementing proper security measures is essential to prevent this kind of attack. If you need further clarification on any specific point, feel free to ask!

---

To understand the different types of DHCP Starvation Attacks, let's focus on the impacts and potential outcomes. DHCP Starvation Attack can lead to two main types of attacks:

## 1. Denial of Service (DoS) Attack
- **What it is**: The primary goal of a DHCP Starvation Attack is to exhaust the DHCP server’s pool of IP addresses. Once all IP addresses are assigned, new devices can't receive an IP address from the server.
- **Impact**: This disrupts network services for legitimate users. Any new device trying to connect to the network won’t be able to do so.
- **Example**: In an office, an attacker sends bogus DHCP Discover messages to the server. All IP addresses are consumed, and new devices like computers or mobile phones can't connect to the network.

## 2. Man-in-the-Middle (MITM) Attack
- **What it is**: After a DHCP Starvation Attack, the attacker may set up their own rogue DHCP server. This server assigns IP addresses to users.
- **Impact**: When legitimate users connect through this rogue DHCP server, the attacker can intercept their network traffic. This may lead to data theft or manipulation.
- **Example**: After launching a DHCP Starvation Attack, an attacker sets up their own DHCP server. When users receive IP addresses from this server, the attacker can eavesdrop or mislead them.

## Other Related Attacks

- **DHCP Spoofing Attack**: In this attack, the attacker sets up a fake DHCP server. It tricks users into connecting to the fake server instead of the legitimate one.

- **DHCP Relay Attack**: Here, the attacker forwards DHCP packets from one network to another, exploiting the DHCP server’s resources.

## Conclusion

DHCP Starvation Attack mainly leads to two types of attacks: Denial of Service (DoS) and Man-in-the-Middle (MITM) Attacks. To protect against such attacks, network security measures like **Port Security** and **DHCP Snooping** must be implemented.


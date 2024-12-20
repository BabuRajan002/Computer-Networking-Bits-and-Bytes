# DNS (Domain Name System)

* A global and highly distributed network service that resolves strings of letters into IP addresses for you. 

## There are five primary types of DNS servers:

1. Caching Name servers
2. Recursive name servers
3. Root name servers
4. TLD name servers
5. Authoritative name servers

**Caching and recursive name servers** 

- Purpose is store known domain name lookups for a certain amount of time
- These DNS servers are generally provided by the ISPs or local network

## TTL (Time To Live)

* A value, in seconds, that can be configured by the owner of a domain name for how long a name server is allowed to cache an entry before it should discard it and perform a full resolution again. 

## Anycast

* A technique that's used to route traffic to different destinations depending on factors like location, congestion, or link health

# Anatomy of Domain name

* Administration of TLD's is managed by non-profit organisation called ICANN(Internet Corporation of Assigned Names and Numbers)

# DNS Zones:

* DNS Zones have hierarchial concepts

# DHCP

* An application layer protocol that automates the configuration process of hosts on a network

## Dynamic Allocation

* A range of addresses is set aside for client devices and one of the these IPs is issued to these devices when they request one.

***Summary of DHCP***

This content explains how DHCP (Dynamic Host Configuration Protocol) automates network configuration for devices, making network management more efficient. 

**Why DHCP is Important**
- Manually configuring network settings for each device is time-consuming, especially in large networks.
- DHCP allows devices to automatically obtain necessary network settings, simplifying administration.

**How DHCP Works**
- A DHCP server maintains a pool of IP addresses and other network settings.
- When a device connects to the network, it sends a request to the DHCP server.
- The DHCP server assigns an available IP address and other settings to the device.

**DHCP Allocation Types**
- **Dynamic Allocation:**  Assigns IP addresses to clients from a pool on a first-come, first-served basis. The IP address may change each time the device connects.
- **Automatic Allocation:** Similar to dynamic, but the DHCP server tries to assign the same IP address to a device whenever possible.
- **Fixed Allocation:**  A specific IP address is manually assigned to a device based on its MAC address, providing greater control and security. 

Let me know if you'd like more details on any specific aspect of DHCP! 

# Generic Questions about DHCP

Let's go over each of your answers and see how they align with the course material. 

**1. What is the purpose of DHCP?**

You're on the right track! You correctly identified that devices need IP addresses, subnet masks, and gateways to communicate on a network. 

**DHCP automates the process of assigning these network configurations to devices, simplifying network management and ensuring devices can connect seamlessly.**  Instead of manually configuring each device, DHCP allows for a centralized way to manage IP addresses.

**2. What does DHCP stand for, and at what layer of the networking model does it operate?**

You are correct! DHCP stands for **Dynamic Host Configuration Protocol**. 

You mentioned that it operates at the Application layer. While DHCP helps configure the network layer, it actually operates at the **Application Layer** of the TCP/IP model. Remember, even though it's configuring network-level settings, the protocol itself functions at the application layer.

**3. Can you explain the four steps of the DHCP discovery process?**

Your explanation of the DHCP discovery process is mostly accurate! Here's a slightly more detailed breakdown:

*   **DHCP Discover:** The client, with no IP address yet, sends out a broadcast message (DHCP Discover) to find a DHCP server on the network. You correctly identified the source and destination IPs and ports used.
*   **DHCP Offer:** DHCP servers on the network receive the DHCP Discover message.  The server offering an IP address sends a DHCP Offer message to the client. This message includes the offered IP address and other network configuration parameters.
*   **DHCP Request:** If the client accepts the DHCP Offer, it responds with a DHCP Request message, essentially saying, "Yes, I want that IP address."
*   **DHCP Acknowledgment:** The DHCP server receives the DHCP Request and sends back a DHCP Acknowledgment (DHCPACK) message, confirming the IP address assignment and lease duration.

**4. What is a DHCP lease, and what is its significance?**

You've got the right idea! 

A **DHCP lease** is like a temporary contract between a DHCP server and a client. The lease specifies the duration for which the client can use the assigned IP address. 

The significance of a DHCP lease is that it allows for efficient IP address management. When a lease expires, the IP address is returned to the pool and can be assigned to other devices. This prevents IP address conflicts and ensures that addresses are available for devices that need them.

**5. What UDP ports are used by DHCP for client and server communication?**

You are absolutely correct! 

*   **DHCP Client:** Uses UDP port **68**.
*   **DHCP Server:** Uses UDP port **67**.



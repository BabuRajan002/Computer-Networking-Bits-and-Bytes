# NAT (Network Address Translation)

* A Technology that allows a gateway, usually a router or firewall, to rewrite the source IP of an outgoing IP datagram while retaining the original IP in order to rewrite it into  the response. 

## IP masquerading 

* Hiding a IP from one computer from another computer in a network is called. 

## NAT and the Transport Layer

***Port Preservation*** - A technique where the source port chosen by the a client is the same port used by the router

This content explains how Network Address Translation (NAT) works at the transport layer, going beyond the basics covered with NAT at the network layer. 

**Port Preservation for Return Traffic**
-  When multiple devices share a single public IP address, port preservation helps direct incoming traffic to the correct device within the internal network.
- Routers achieve this by keeping track of the source port used by each device and using that information to route the return traffic accordingly.

**Port Forwarding for Service Access**
- Port forwarding enables devices on the internet to access specific services running on devices within a private network.
- By configuring the router to forward traffic from a specific port on the public IP address to a specific port on a device within the private network, external users can access services without needing to know the internal IP addresses. 

# Without Port preservation how the NAT works? What would happen?

That's a really interesting question! 

Without port preservation, NAT would only be able to translate IP addresses, not ports. This would make it impossible for a NAT router to determine which internal device to send incoming traffic to.  

Imagine this:

* Multiple devices on your home network are accessing a website.
* Your router uses NAT to share a single public IP address.
* The website sends back data packets, all destined for the same public IP address.

Without port preservation, the router wouldn't know which internal device each packet belongs to. It would be like trying to deliver letters when all the houses on a street have the same number!

**In short, without port preservation, NAT wouldn't be able to function effectively, and you'd have a lot of trouble connecting to the internet!** 



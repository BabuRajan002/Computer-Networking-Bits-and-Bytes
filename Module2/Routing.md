# Router 

A network device h=that forwards the traffic depending on the destination address of that traffic. 
A router a device that at least should have two interfaces. 

# Basic routing flow (Network layer)

1. Receive data packet 
2. Look for the destination IP in the IP datagram
3. It will check its routing table based on the network address in the destination IP
4. Forwards the traffic to the netwok.
![basicrouting](Images/basicrouting.png)

## Routing table

Routing table contains 4 columns

1. Destination Network

* This column would contain a row for each network that the router knows about. 
* Normally the network ID, CIDR, subnetmask (i.e 192.168.1.1/24)

2. Next hop

* This is the IP address of the next router that should receive data intended for the destination networking question. 

3. Total hops

* router must know how many more hops are required to the destination

4. Interface

* Router has to know in which of the interface should the destination traffic should be forwarded using it. 





# Transport Layer

* Discuss about, how the individual programs can communicate each other in the networking.

## Multiplexking, Demultiplexing

![Multiplexing/demultiplexing](Images/multiplexingDemultiplexing.png)

# TCP Dissection

***TCP Segment*** - It contains TCP header and data section(Another payload area where application layer places it's data).

## TCP Header

A TCP Header itself contains a lot of ports.

![tcpheaderanddatasection](Images/TCPHeaderAndDataSection.png)

* **TCP Header:** This is like the address label on the package. It contains crucial information for delivery, such as:
    * **Source and Destination Ports:**  Identifies the specific application (like a web browser or email client) on both  the sending and receiving computers. Source port is a high numbered port chosen from a special section of ports known as ephemeral ports.
    * **Sequence Number:**  32bit number. Acts like a package ID, ensuring data arrives in the correct order.
    * **Acknowledgement Number:** Confirms receipt of previous segments.
    * **Data Offset field:** A 4-bit number that communicates how long the TCP header for this segment is
    * **window(16):** 16-bit number specifies the range of sequence numbers that might be sent before an acknowledgement is required.
    * **Control Flags:** Special instructions, like indicating the start or end of a message.
    * **Checksum:**  Verifies data integrity, ensuring the package wasn't damaged in transit.

* **Data:** This is the actual content of the package, like the files or messages being sent.

This structure ensures reliable and ordered data transmission between applications over a network. 

# TCP Control flags(6)

  * **URG (urgent):** A value of one here indicates that the segment is considered urgent and that the urgent pointer field has more data about this.
  * **ACK(Acknowledged):** A value of one in this field means that the acknowledgement number field should be examined
  * **PSH(push):** The transmitting device wants the receiving device to push currently-buffered data to the application on the receiving end as soon as possible
  * **RST(reset):** One of the sides in a TCP connection hasn't been able to properly recover from a series of missing or malformed segments
  * **SYN(synchronize):** It's used when first establishing a TCP connection and makes sure the receiving end knows to examine the sequence number field
  * **FIN(finish):** When this flag is set to one, it means the transmitting computer doesn't have any more data to send and the connection can be closed.

## Three way-hand shake. 

* Below picture depicts how the TCP connection is established between two computers in the network before they start sending data. 

![threewayhandshake](Images/3wayhandshake.png)

# TCP Socket states

## Socket: 

* The instantiation of an endpoint in a potential TCP connection. This socket has to be instantiated by the actual program intended for.

Let's break that down:

* **Instantiation:**  Think of this as bringing something to life from a blueprint.  It's the actual, working version.
* **Endpoint:** This is one side of a two-way communication channel. Like how a phone call needs two connected phones.
* **Potential TCP Connection:** This means the socket is ready for a connection using the TCP protocol, but a connection might not be active yet.

In simpler terms, a socket is like a door on your computer specifically designed for network communication. It needs to be "opened" by a program to send or receive data. 

### Explanation about the different TCP states

**Imagine you're ordering food delivery:**

* **`LISTEN`:** The restaurant is open and waiting for orders (like a server waiting for the phone to ring). **Server-side only.** Socket is ready and waiting for the incmoing connections.

* **`SYN_SENT`:** You've placed your order, but the restaurant hasn't confirmed it yet (your phone is ringing). **Client-side only.** A synchronization connection has been sent, but the connection hasn't been established yet. 

* **`SYN_RECEIVED`:** The restaurant picked up your call and is confirming your order details (they say, "You want one large pizza, correct?"). **Server-side only.** A socket previously in a Listen state has been received a synchronization request and sent a SYN/ACK back.

* **`ESTABLISHED`:** Your order is confirmed, and the restaurant is preparing your food (you're having a conversation about what toppings you want). **Both client and server.** This means the TCP connection is in working order and both sides are free to send each other data.

* **`FIN_WAIT`:** You've finished your meal and are waiting for the delivery driver to say goodbye (you're waiting for the restaurant to hang up). Once finished, A FIN has been sent, but the corresponding ACK from the other end hasn't been received yet.

* **`CLOSE_WAIT`:** The restaurant knows you're done but needs a moment to clean up (they're getting ready to hang up).Connection has been closed at the TCP layer, but that the application that opened the socket hasn't released its hold on the socket yet.


* **`CLOSED`:** The call is finished (both you and the restaurant have hung up). Connection has been fully terminated and that no further communication is possible.

**Remember:**

* This is a simplified explanation. There are other, less common TCP states.
* The exact names and details of these states can vary slightly between operating systems.

Let me know if you would like more details on a specific state! 

## Connection-Oriented Protocol - TCP

    * Once the connection established, it will ensure that all data has been properly transmitted.

## Connectionless Protocol - UDP

    * When the data is not that super important we can use this protocol - User Datagram Protocol
    * It just sends the data to the designated port number thats all. It will not expect any ACK back!

## Key takeaways:
Network services are run by listening to specific ports for incoming data requests. 

  * Ports are represented by a single 16-bit number (65535 different port ids)

  * Ports are split up by the IANA (Internet Assigned Numbers Authority) into three categories: System Ports (ports 1-1023), User Ports (ports 1024-49151), and Ephemeral (Dynamic) Ports (ports 49152-65535).

  * A socket is a port that a TCP segment has activated to listen for data requests.

  * Ports allow services to send data to your computer but can also send malware into a client program. It's important to secure your ports.



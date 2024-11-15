Cables:
-> Conect different devices together allows data transmitted over them.
Two Types of cables:
1. Copper.
   -> Mostly we know that computer send the data using binaries (0 and 1). Receiver in the another differentiates the voltage difference with binaries 0 and 1 which can be translated into different forms of data.multiple ways.
   -> Most common forms of copper twisted-pair cables used in networking is cat(egory)5, cat5e, and cat6 cables.
   -> cat3, cat5, cat 5e, cat 6, cat 6a, cat 7.The twisted pairs inside the cable can drastically alter how quickly the data can be sent across them. How resistent the signals.

   Cross talk:
   -> When the electrical pulses are in one cable accidently detected in another cable causing the network error in the receiving end. Higher level protocols has a method for detecting the missing data and asking again
   the missed data.

   -> Copper cables uses electrical voltages to transmit the data between the network devices or computers. 
   
2. Fibre optics:
   -> Contain individual optical fibers, which are tiny tubes made our of glass about the width of a human hair.
   -> This tubes can transmit the pulses light to represent the 0's and 1's.
============================================================================
Hubs and Switches:
-> Hub is a physical layer device that allows for connections from many computers at once.

Some realtime scenario example why Hub is not useful for the modern networks:

That's a great question!  Let's dive into a real-world scenario that illustrates how hubs and switches work, relating it back to what we're learning about collision domains.

Imagine an office setting:

Scenario:  A Small Office with a Hub 

Think of a small office with several computers all connected to a central hub.
Everyone's trying to print, send emails, and access files on a shared server at the same time.
Since a hub only understands physical connections, it lets all these data packets flow freely without direction.
This creates a traffic jam of information, like everyone trying to squeeze through a single doorway at once. This is a collision domain in action.
Result: The network slows down, print jobs get stuck, and frustration builds as everyone waits for their turn to use the network.
Solution: Upgrading to a Switch

Now, imagine the same office upgrades to a network switch.
The switch is intelligent. It learns which computer is located at which port.
When a computer wants to print, the switch directs that data packet only to the printer, not to every other device.
It's like having designated pathways for different tasks, ensuring smoother and faster communication.
Let me know if you'd like to explore another example or want to delve deeper into a specific aspect! I'm happy to tailor our discussion to your interests.  And, if you have a particular industry in mind, I can try to make the examples even more relevant to you. Just let me know! 

Collision domain:
-> A network segment where only one device can communicate at a time.
-> If multiple systems try sending data at the same time, the electrical pulses sent across the cable can interfere each other. 

Switches: 
-> Due to above constraints Hub is not useful for high network traffic. 
-> Switch is the best option for it. 
-> Main difference between the Hub and Switch is, hub operates in Physical layer and switch is Data link layer. 


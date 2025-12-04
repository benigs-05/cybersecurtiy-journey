# cybersecurtiy-journey
This repo documents my weekly learning progress as I train my career in Cybersecurity. This will be a half a year journey of trying to grasp the fundamentals and the ins and outs of cybersecurity. 

### CURRENTLY FOCUED ON ###
- CCNA
- Security+ 
- TryHackMe SOC/Blue Team labs
- Linux basics

### WEEKLY LOGS ###
This is where my summaries will be per week on what I've learned. I will add screenshots, notes, and small writeups of the labs I've completed. 

### DAY 1 ###

For the first 30 minutes, I delved into understanding what Cyber security is and the roles within it. With this I was introduced to what offensive security and defensive security are. 

Offensive security was more on thinking like a hacker. This meant that people within this job usually look for bugs, loopholes, and weaknesses of an organization’s systems to break into their system.

Defensive security on the other hand, or what we call “blue teaming”, defends , build architectures, creates systems, analyzes data, monitors data, detects irregularities to stop and prevent hackers from getting into the system. These people are the frontline of an organization’s defense system. 

And the career I am most interested in is a Security Engineer, but before that I want to understand the fundamentals and gain knowledge by being a Security Analyst first. 

Ever since that fateful trip on February this year, the Cyber security seminar has filled my passion and ambition to be on the frontline to defend and be a wall in this digital world. 

After that I moved on to Network Fundamentals. This was quite an easy read for me since my elective this college, which I just finished, was Networking. So, I had a good understanding of what networking is, it’s how computers, devices, and services connect with each other. What the different topologies are like what was discussed here were LAN (Local Area Network), a star topology where there’s a central device for all the devices, a bus topology which travels on something like a “highway”, and there’s the ring where devices form to create a ring, and topologies that were not discussed like mesh, and hybrid, etc. 

This also introduced layer 2 (switches) and layer 3 (routers) devices. Layer 2 switches mainly focused on MAC addresses, are built in numbers that are burnt in a devices chip that makes them unique to every device, since they forwarded the packets which are contained into a frame to their respective devices within their LAN, but if it was outside of the LAN it forwards it to the respective routers which will now handle based on its IP address. 

OSI model was also introduced here where it has 7 different layers, but the focus for networking here is the first four which are the physical layer, data link layer, network layer, and transportation layer. 

The physical layer, by its name itself, is concerned with the physical devices and how they are connected to each other. This can be what type of cable we used like CAT6or CAT5, types of routers, Aps, or switches. This is the lowest layer and the easiest to understand out of them all.

Next is the data link layer. The data link layer contains the packet that the data link layer will frame. The frame concerns itself with the MAC address of a device. This is where switches come into play. 

Then we have the network layer where routers are a part of. This is where routing comes into play, routing talks about the path on which the data are to be sent. This includes protocols like OSPF (Open Shortest Path First) that finds the most optimal path for the data to be sent. Since this is the network layer or layer 3, IP addresses are used here since routers use these to deliver the packets to their respective destination. 

And lastly, we have the transportation layer, this mainly focuses on what type of protocol is going to be used to send the data. We Have the TCP (Transfer Control Protocol) and UDP (User Datagram Protocol). TCP in short need to establish a reliable connection first to its destination so that the data that’s going to be sent has integrity. Examples of its use are for file sharing. For UDP we don’t care that much if data is lost, it’s a continuous stream of data sent. Examples of this is a video call. Where even though it might be blurry sometimes the call continues. 

The remaining is mostly what we call the data, layer 5 or the session layer (maintaining the connection), layer 6 or the presentation layer (this is where translation of data occurs so that the receiving device can understand it), and last is the application layer or the layer 7 (where everyone is familiar with, this is where we see and interact with data. Like how we used Facebook, YouTube, Gmail, etc.)

All these layers work together to create a process called encapsulation (Layer 7 to Layer 1) and decapsulation (Layer 1 to Layer 7). 

There’s also what we call the TCP/IP which is kind of like the OSI model but is reduced to only 4 layers. Application, Transport, Internet, and the Network Interface Layer. Again, the TCP/IP requires an established connection first before data is sent. This makes the data of this protocol much more reliable compared to its counterpart. For it to establish a connection we have a process called the Three-way Handshake. First it (SYN)synchronizes with the receiver, the receiver then acknowledges it and then synchronizes with the sender (SYN/ACK), and the sender finally acknowledges it to establish a connection. Once the connection is finished, we then proceed to something similar. The sender sends (FIN) for closing the connections, receiver sends (FIN/ACK), and the sender acknowledges it (ACK) and the connection is closed. 

Then we have the UDP/IP, again UDP doesn’t require a constant connection between two devices to be sent. This makes it much faster but less reliable. If the receiver requests, the sender will continue to respond until it finishes, disregarding the quality of the connection. So, some data may be lost in this process. 

There are also ports, a numbering system from 0-65535 that are usually where we connect to based on the protocol being used. For example, HTTP uses port 80, HTTPS uses port 8080, FTP uses port 21, etc. 

And lastly for networking fundamentals is port forwarding. Port forwarding is necessary since without it only devices within the LAN can access the things inside it. Port forwarding makes it so that external devices that aren’t in our network can access the internal services inside our network. Things like firewalls are added here because they allow or deny traffic to enter or go out of a network. Another one is a VPN (Virtual Private Network), it acts like a private tunnel that makes it for 2 devices withing different networks can communicate privately with each other. 

### DAY 2 ###

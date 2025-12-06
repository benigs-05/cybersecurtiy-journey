### cybersecurity-journey ###
This repo documents my weekly learning progress as I train my career in Cybersecurity. This will be a half a year journey of trying to grasp the fundamentals and the ins and outs of cybersecurity. 

### CURRENTLY FOCUSED ON ###
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
For day 2, I learned the basics of how the web works and Linux. 

Although I have a background in networking, we never really delved deeper into how the web works, specifically how the different protocols work. We just knew what they were and what they did. That’s why this module made me understand the different protocols that take place whenever we browse the web. 

Let’s start with the DNS or the Domain Name System, basically without the DNS when searching the web, we would have to enter the IP address of the website. Let’s say if we want to look up Facebook, without DNS in place, just searching up Facebook wouldn’t get you anywhere because it wouldn’t know what to do with it. We would have to type in one of its IP addresses like 152.240.241.35. Having DNS would mean that we can mask this IP with Facebook.com. Making it available for us to look it up by just typing the name of the website and not the IP address. 

We also have part of the DNS, the top-level domain (.com, .edu, .ph, .gov, etc.), second-level domain (Facebook, Gmail, YouTube, etc.), and  the subdomain (admin.tryhackme.com, they are seated in the left side of the second-level domain and has the same restrictions like the second-level domain. In this case it’s admin.)

In DNS there are also record types, A record (holds IPv4 addresses), AAAA (holds IPv6 addresses), CNAME (this resolves to another domain and that domain is responsible to where to go), MX Record (This is responsible for the transport of emails, like redirecting it to where it should go first, and the backups that it should go to.), and TXT Record (This is responsible for creating rules of entry for emails, and it also can prove that your ownership of a domain, and storing any extra information a service needs). 

There’s also how the DNS handles requests. 
1. First it checks if the DNS you are trying to look up is in your computer’s local cache, if not it goes to a Recursive DNS Server. 
2. The Recursive DNS Server (this is provided by your ISP) also has a cache. If it can find it locally it will proceed with getting it. If not, it now goes to the Root DNS Server. 
3. Root Servers act as the DNS backbone of the internet. This is for redirection. Let’s say you look up Facebook.com, it will redirect you to the correct TLD Server. So, TLD Server will be responsible for forwarding where to go for the .com part. 
4. Then, the TLD Server will forward it to the respective Authoritative server that will handle your response. 
5. Lastly, the Authoritative Server is responsible for storing DNS records for a particular domain name. Once it finds it, it sends it back to the Recursive DNS server, and caches it locally and then proceeds to move forward with the request. 

Next, is the HTTP(s) or the HyperText Transfer Protocol (Secure). This protocol is responsible on how we communicate with the web servers that we interact with, this will decide how the webpage data is transmitted, regardless of the formats it may use (images, videos, html, etc.).
Inside this is the URL (Uniform Resource Locator), this is an instruction on how to access the information on the internet. We also have methods like GET (getting information), POST (posting new information), PUT (updating information), and DELETE (deleting information) requests.  

We also have status codes that tell us what went wrong when we tried to access a HTTP server. One example would be 200 (OK) or 403 (Forbidden) that we might encounter on some websites. 

And the inside are also the different headers, one common header that we are all familiar with are cookies. Cookies make it so that whenever we visit a website once and we enable cookies. Whatever we do with the website, if we come back to it, it will remember us because of the cookie. 

 Of course, the structure of how websites are created is also in this. The two main languages are HTML, which adds static configurations for the website and JavaScript which adds the functionality for the website. Both of this work hand in hand to create a functioning website. And when bad programming occurs within this, data can be exposed to hackers specially when it's poorly made. One practice is HTML injection, this is where unfiltered user input is displayed on the page. 

So, by putting all of these together I learned the process whenever I request a website. To sum it up it goes like this, Request a website – Find the IP using DNS – Connect to the server – View the website. 

 
Last is the introduction of Linux and how it works. For day 2, I only went through 2 rooms since how the web works took so much of my time. 

For this, I was introduced to Linux (Linux is an operating system like Windows) and it is lightweight compared to Windows OS. Some of its purpose are it allows us to create websites, for control panels in cars, Point of Sale, and infrastructures like traffic light controllers or industrial sensors. And we used a Ubuntu Linux machine that is built in TryHackMe. The one downside that people can find daunting with Linux is that it doesn’t exactly have a GUI, we only interact with the machine =using the terminal. So, really understanding and learning the commands here are helpful. 

With this room, I learned my first command which is echo, this outputs text. After echo, it started to be more fun. I learned about ls, which lists the directories that you have within that location. There’s also cd where it changes the directory you are in. There’s cat for outputting the contents of a file, and there’s pwd for determining where you are in the directory.

Here's a list of codes/flags/operators that I also learned:
-	find [-name hello.txt] or find [-name *.txt if you want the list of all the files that have this type of extension.] (for finding a specific file)
-	grep, one of its uses is for finding a specific text in a file. grep “error” this.text
-	&, usage is it enables the code to do its job in the background while you do other stuff. 
-	&& allows y ou to combine multiple codes in one line
-	>, this operator let’s you take the output and send it to where you want to. For example echo hello > message. This puts the txt hello file to the message file.
-	>>, this operator does the same but instead sending it and changing the values within it, this appends it. Meaning if we use echo hi >> message. We are creating a file that has two texts in it hello, and hi. 

For room 2, or the Linux Fundamentals 2. We used ssh to remotely execute commands on another device. 

With ssh I could login and use accounts that were provided by tryhackme using the command
ssh tryhackme@givenipaddress. Along with its password, tryhackme.
This allowed me to access a remote machine that I can execute commands on.

These are the commands I’ve learned in room 2: 
-	-a, this comes along with ls and lists all files including those that are hidden. -a isa flag and with man (manual) command. man ls, we can view all the flags that we can use within linux. 
-	touch, for creating a file
-	mkdir, making a folder, which then creates a new directory.
-	cp, copy a file or folder
-	mv, move a file or folder
-	rm, remove a filer or folder
-	file, determine the type of file.
-	-l, enables us to see the details about a file such as its permissions, who created it and when. Paired like this, ls -l 
-	su, for switching users. We can either use su user2 which switches to user2 but variables stay the same, but we keep our environment or use su -l user2 that loads user2’s environment variables. 
And lastly some of the directories like, /etc (files here are used by your operating system), /var (this is where frequently accessed or written by services applications running ong the system, like log files), /root(the home directory), and /tmp (stores data that are only accessed once or twice.)
That’s all for day 2!!


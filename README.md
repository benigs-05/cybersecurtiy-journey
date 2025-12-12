### cybersecurity-journey ###
This repo documents my weekly learning progress as I train my career in Cybersecurity. This will be a half a year journey of trying to grasp the fundamentals and the ins and outs of cybersecurity. 

### CURRENTLY FOCUSED ON ###
- CCNA
- Network+
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

### DAY 3 ###
For Day 3 I finished 2 modules. Linux Fundamentals 3 and Windows Fundamentals 1. 
For Linux Fundamentals 3, Terminal Text Editors were taught. Although we have echo and > to output to a given file, it’s only limited. That’s why [nano] is preferred when it comes to editing files. We use nano [name of file], if the file you input doesn’t exist, yet it will create that file. If it does exist it will just proceed to access the contents of that file and continue on editing it. 
VIM was also introduced but since it’s a much more advanced editor, it was only brought up. But I do plan on learning VIM since it’s also a part of Linux. 
Some utilities were also taught, like copying a file from your machine to a remote system if we know the username and the IP address and the directories of that machine. 
scp was used, it goes like this: 
scp [file name in your system to be copied] [username of where you’ll copy it]@[its ip address]:[port number if available]/[directory]. 
And if we want to copy something from that machine the code is as follows:
scp [name of the machine that you’ll copy the contents]@[ip address]:[port number]/[directory] [filename in your system]. 
If for example you copy a file named hello.txt to a remote machine with a directory like home/downloads/hi.txt, it will replace the hi.txt with hello.txt. But if you just input the directory home/downloads/. The file hello.txt will be copied in that directory along with hi.txt

Python3’s “HTTPServer” was also introduced here, this module turns your computer into a quick and easy web server that you can use to server you own files where it can be downloaded using curl and wget. 
To access and download we need to have 2 instances of the terminal opened. 
The first terminal will be used to access web server with the command: 
python3 -m http.server, while this is open, we can open another terminal where we can use that to download files. The code to use is: wget http://[MACHINE_IP]:8000/[filename].
Once we are done, we can use ctrl+c to stop the instance of the web server. 
I also learned about the processes that run in Linux, how to view them and how to manage them. ps, give a list of all the running processes in your system. ps aux, gives the processes that are also run by other users. 
These processes are tagged with their ID called the PID (Process ID), this is used to determine the order of which the process runs, or the total number of processes currently running. 
top command was also introduced, this also gives the processes that are running but instead of a one-time view like the ps, this command refreshes every 10 seconds and when you move down the list using the arrow keys. 
kill, is another command used to terminate a process, when it is killed, we can also do 3 other commands to follow up. We can use SIGTERM (kills the process and allows it to do cleanup), SIGKILL (kills the process and doesn’t do any cleanup), SIGSTOP (suspend a process). 
There are also processes that we manage, we can do this by using the command: systemctl [option] [service] wherein option can be: START, STOP, ENABLE, DISABLE.
We also have background and foreground processes. Things ran in the terminal will run in the foreground since if we use like cat to see the contents of the file it is shown through the terminal which is a foreground process. A background process is usually paired with an * operator. This is great for downloading or copying large files that can take a lot of time. With this, we can do other tasks rather than just waiting for it to finish. We can also use ctrl + z to background a process. And to foreground it again, we can just use fg.
And then we have cron, it is a process that let’s us manage our crontabs where we can automate certain processes by putting in: 
0 */12 * * * cp -R /home/cmnatic/Documents /var/backups/
[min][hour][day of the month][month][day of the week][the actual command that will be executed], we can also put in asterisk * to leave some of it blank. So the code above will run every 12 hours every day.  [*/] means that is should “run every x units”, so in this case 12 units. 

There are also packages and software repos within Linux. When users or developers want to submit software to the community, they do so by submitting it to an “apt (advanced persistent threat)” repository. This needs to be approved and once approved it will be okay for release.

We can locate the repositories in our system using the ls command in the /etc/apt directory. Locate sources.list and use nano. So, nano sources.list, with this command we can see all the repositories that we have access to. We can also remove and add repositories inside. Or we can also use the command sudo add-apt-repository [Type of repository]:[username]/[name of the specific repository]. After this it will automatically add it to the sources.list 
And lastly, we can easily maintain our logs via the directory /var/log 
Next we move on to Window’s Fundamentals 1. This was very easy since, almost everyone uses windows as their operating system. The basics were introduced like the GUI (Graphical User Interface), the file system (from FAT16/32 – HPFS (High Performance File System) – and what Windows use now is the NTFS (New Technology File System)). Basically, NFTS is above these 2 since it addresses limitations such as. Supporting files larger than 4gb, setting specific permissions on folders and files, folder and file compression, and encryption. 
NTFS has 6 permissions per folder or file: Full control, Modify, Read & Execute, List Folder Contents, Read, Write. 
NTFS also has a feature called ADS(Alternate Data Streams), it is a file attribute to NTFS. It allows files to have more than one stream of data. 
The Windows\System32 Folders, in default this is where the OS is located. But it can actually be anywhere in the different directories. This is also where Environment Variables are, these are the variables that store information about the operating system environment. 

Users were also introduced, how there’s a standard and administrator type of users. And to view these users, we can use the command lusrmgr.msc in run to view the users and groups. These groups has permissions set to it, and users are assigned to this group by the administrator. The user inherits the permissions of the group they are part in, but users can also be assigned to multiple groups. 
The UAC (User Account Control), this helps prevent malware from damaging a PC and helps organizations deploy a better-managed desktop. We may have seen UAC do its job sometimes when it asks us for permission before allowing apps or users to make system-level changes. Without UAC, malware can be installed silently when we are browsing or doing stuff on the internet. 
Settings and Control Panel was also introduced. Settings has become more advanced in comparison to other versions of settings in lower versions of windows. Settings is more used now even in changing things that, back then, would require the control panel to do so. 
Lastly, the Task Manager, this informs us the apps and processes that are running in our system. This gives the CPU usage, GPU, Memory, and RAM. 

### DAY 4 ### 
This day covered the last 2 modules within the Pre security path, the Window’s Fundamentals 2 and 3. This delved deeper into system configuration, and advanced system settings. This talked about how we can access the system configuration via settings or just the msconfig. System configuration typically helps with diagnosing startup issues. It covers General (this is where how we want to handle startup), Boot (We can configure boot options), Services (This lists the configured services in your system), Startup (this is used to manage startup apps, but windows currently suggest to use the task manager instead when configuring the startup apps.), and Tools (this is where you can find various tools that we can run to configure the operating system further) tab. 

In Advanced System settings, we can locate the system properties, inside this we can configure the performance and behavior of our system. 

We can also change UAC settings about when to notify us. It can be put to always notify, notify for apps, notify without dimming, and never notify. It is not advisable to change this though as it can pose security threats since UAC is responsible for making sure that our privileges cannot damage the system. 
We also have Computer Management where we can find System Tools, Storage, and Services Application. 
Under System Tools, we have Task Scheduler, this is where we can manage tasks that we can set up if we want to automate it, permit it to run, or even create new tasks. Event Viewer, everything that we do on our computer will be registered here. This can serve as trails that can be used when it comes to troubleshooting our system. Shared Folders, this is where Users and Groups are found. Performance is used to view performance data which can be in real-time or log files, and lastly is the Device Manager, where we can manage and see all the devices that are running in our system. 

We also have Storage which is responsible for Windows Server Backup and Disk Management. Within Disk management, we can set up new drives, extend a partition, shrink a partition, and assign or change drive letters. 

We also have Services and Applications, you can see here a more in-depth structure of how services run in your system, and you can also decide if you want it to start automatically or manually. 
System Summary was also discussed, here we can see our hardware resources, the components of our systems, and the software environment in which our systems run. Things like devise that are connected, the specs of our system, adapters, IP address, MAC address can be located here. 
We also have the Resource Monitor, this displays the processes that run in our system and the state they are in, the threads , and CPU they use. You can see the CPU, Disk, Network, and Memory resources here. 
Just like how Linux has a terminal, Windows also has one that we call the command prompt. This is how we can interact with our operating system without the use of GUI that was presented beforehand. GUI is much easier to use than the command prompt, but the command prompt is still a part of the Windows OS. Things like ipconfig (which can view the network address of the computer we are using.). And just like Linux, this of course comes with its own manual or help. We can either use help, or [command] /?
Lastly, for this module is the Windows Registry, this registry contains the profiles for each user, applications installed, property sheet settings, the hardware that exists on the system, and the ports being used. We can view and edit the registers, but it isn’t advisable since it’s complicated and dabbling in it can affect normal computer operations if you don’t know what you are doing. 
For the last room (Windows Fundamentals 3), I was introduced into several built in Windows security tools that come in with the OS. These security features protect our devices from getting harmed. 

First, is the Windows update. Typically, the windows update rolls every 2nd of Tuesday but sometimes Windows pushes updates ahead of schedule if it’s something that is really needed for the system. Windows update can be ignored but it will always auto update itself after a set number of times you ignore it. 
Second, is the Windows security having four protection areas in it that are Virus & Threat protection, Firewall & Network Protection, App & Browser Control, and Device Security. These 4 are marked with colored circles. There’s Green, Yellow, and Red. Green mean everything is okay, yellow means you need to review it, and red means you need immediate action. 
These 4 can also be configured. In Virus & Threat protection, you can manage how you would like your device protected. You can even turn off protection if you want to or configure it to exclude certain files or folders from these settings. 
Next, is the Firewall & Network Protection. Firewall controls what goes in and out of our devices via our ports. Under this setting we have, Domain Network {host system can authenticate to a domain controller like a company where there is a Domain Controller),  Private Network (private and home networks, or our trusted networks), and Public Network (Public networks that include hotels, cafes, and other locations, or the untrusted networks). You can configure the apps here and where it might belong to the three. 
Another one, is the App & Browser control. This is responsible for showing you a notification when a service, a file, or an app can make changes, can harm your device, or when it’s going to be installed. This can check it and protect your device. 
We also have Device Security, although this setting isn’t usually changed. We have core isolations here that protect core parts of our devices. Settings here should be defaulted and shouldn’t be configured. 
Next, is Security Processor, or also called the TPM (Trusted Platform Module). This provides additional security to our device. We can also view our Security Processor details here. 
BitLocker was also briefly introduced as a feature of Windows, but it wasn’t talked about and had only a paragraph of it. It stated that it is a data protection feature that integrates with the operating system and addresses the threats of data theft or exposure. TPM and BitLocker goes hand-in-hand. 
Last is the Volume Shadow Copy Service (VSS)m this creates a snapshot of the data that can be used for backup whenever needed. VSS enabled will allow us to create restore points, perform system restore, configure restore settings, and delete restore points. This can be configured via right clicking a our C drive and picking the “Configure Shadow Copies”. 
That’s it for the 4 modules that I went through for the past 4 days. I learned about the intro to cyber security, networking, Linux, and Windows fundamentals. I never had any trouble, and enjoyed Linux more compared to Windows. Theses series of module motivated me that there’s still so much new things to learn within cyber security and I am excited for it! 

### DAY 5 ### 
This started the Cybersecurity 101 course, sine I had finish Pre Security. This opened with how I can use the web and utilize the search engines within it. We start by how we can use google better, or any search engine. We can specify what type we are searching for like filtype:, we can exclude words using -, we can look for specific words in a website by typing in “site:facebook.com ai”.
We also have search engines that have specific functions. One example is Shodan, you can look up devices here that are connected to the internet. Whatever it is as long as it is connected to the internet. 
Censys is like Shodan but this search engine is more specific as it focuses on certificates, websites, protocols, and other internet assets. To set them apart is, Shodan can examine the service banners of TCP, while Censys can analyze it by going bit-by-bit.
VirusTotal is another website that we can use to examine files via uploading them or the url of the file. 
HaveIBeenPawned takes your email address and scans if it has appeared in a leaked data breach. 
The CVE (Common Vulnerabilities Exposures) program, is a dictionary of vulnerabilities. 
Exploit Database, is also a dictionary of approved exploits. These codes are well tested and marked as verified. Uses of these codes aren’t ethical if no permission from the company or organization was given. 
GitHub, this is also a large database wherein we can find codes, CVEs can also be linked here, exploit codes. Just about anything that a software might upload to. 	
We also have social medias that we can use when it comes to looking for information about someone.  
This concluded with a very short study session for the day. Learning how to navigate the web in a much more efficient way. 

### DAY 6 – THE CHALLENGE OF LEARNING ## 
As I get more into learning about what cybersecurity is, it dawned me that my current learning method wasn’t yielding the results I had hoped for. I often just jump into a topic, read it and understand it, move one and whatever topics I have learned that day will be summarized the next day before I start studying. 

I did understand it, but only on a shallow level, I didn’t know how to correlate it to other concepts, and it was difficult for me to explain it in a comprehensive way. The retention and the mastery weren’t there. That’s why I needed change, and I reserved 1 day of looking up the web on how to study. 

And that’s when I stumble upon Justin Sung, he’s a YouTuber that has dedicated his life on researching what is learning, how does it happen, and not just what are the best methods to learn. 

The concept of putting high enough load and effort for the brain to change in a way that it’s easy to learn to understand concepts, correlate them, master them, and retain them. Applying this method took me double the time to finish a subject but I am happy that I get to learn hard, and not just the easy way. I am enjoying learning cyber security and have found great joy in the way I currently learn. There still needs to be improvement, and I am glad I am aware of it and am here for it. 

### DAY 7 ###

Day 7 was SUCH a fun experience since I really understood what Windows Domain is. 

Windows Domain is a centralized network that contains servers, users, machines, and policies within it.

The Windows Domain is managed by a server called Domain Controller. This Domain Controller is where all those devices and users are managed by. The Domain Controller holds information about security groups, Group Policies, Organizational Units, Authentication, and necessary data from users like login, ip address, ports, etc. 

Data are handled by the Active Directory, specifically the Active Directory Domain Service. 

There are 2 “Security Principals” living inside the Windows Domain. They are the Users, and the Machines. 
Users can be authenticated and can be granted permissions on the resources that they can access. There are 2 different type of users, people (actual users that are signing in and using the devices) and services (services are granted accounts that are specifically used to run a certain service.) 
Machines can also be authenticated via a random key that the domain controller will give them for future access and authentication. They are also permitted to use resources within the domain. 

These 2 can be classified into different Security Groups. Security Groups are groups that have certain permissions on what resources they can use. Can they use the database server? The file server? The printer? 

Users and Machine can also be put into Organizational Units. Organizational Units are used to categorize and organize the different entities living in the domain. Within OU’s there are also what we call Group Polices that can be applied to them, that’s why a user or machine can only be a part of one OU. This is because policies are applied to them. But if we want special privileges for a user, we can use delegation. Delegation is the use of assigning special privileges to a person over a certain OU. 

Let’s move on to Authentication, the service used here are Kerberos, and NetNTLM. 
Kerberos uses ticket-based authentication, the process is as follows: 
1.	The user is authenticated via his login information. Since his login information is already hashed in the Domain Controller. When getting tickets from the Key Distribution Center, the password is hashed and encrypted and that is what’s sent to the server. 
2.	The encrypted key is then forwarded to the KDC to give the Ticket-Getting-Ticket, once it calculates the necessary information and is correct the user is authenticated and given a TGT, that can be used to access different tickets like the TGServices, and is also given a Session key. 
3.	To access a service, the user sends a request for a Ticket-Getting-Service to the KDC
4.	The KDC then uses the users session key, TGT, and SPN (Service Principal Name – this specifies the service and the server name).
5.	Once the calculation is complete and verified, KDC sends a TGS along with a service session key.
6.	The user then sends these things to the server that’s going to be used. Once verified by the server, the user is now authenticated to use that server.

NetNTLM on the other hand uses challenge-based methods for authentication, the process is as follows: 
1.	The user requests to get authenticated to the server they want to access. 
2.	The server generates a challenge response to be sent to the client
3.	The client adds information (NTLM password hash) along with the challenge that is sent back to the server. 
4.	The server forwards it to the domain controller
5.	The domain controller verifies this by computing the data. If it matches the expected data, it verifies. If not, user can’t use the server.
6.	And status is sent to the client whether he can access it or not
Although both are used by DC, Kerberos is the default authentication service, and NetNTLM is used for backward compatibility. 
And whenever a Windows domain gets larger, we manage it not by adding more devices, groups, policies to one domain but by adding a subdomain. This creates a tree, wherein we can have multiple domains, with multiple Domain controllers, and on different networks. A new security group is added her called Enterprise Admin that has access to all the domains.

Once this expands, and let’s say we have another company that is different from our domain that we are managing. That is called a forest, where there’s a collection of trees. 

We also have trusts, this can be one way or two way. One way trust relationships allow for one domain to have access to another. Two-way means they can access specific things from each other with the permissions they are given. 







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

### DAY 1 - INTRO TO CYBER ###

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

### DAY 2 - HOW THE WE WORKS, LINUX ###
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

### DAY 3 - WINDOWS FUNDAMENTALS ###
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

### DAY 4 - WINDOWS FUNDAMENTALS ### 
This day covered the last 2 modules within the Pre security path, the Windows Fundamentals 2 and 3. This delved deeper into system configuration, and advanced system settings. This talked about how we can access the system configuration via settings or just the msconfig. System configuration typically helps with diagnosing startup issues. It covers General (this is where how we want to handle startup), Boot (We can configure boot options), Services (This lists the configured services in your system), Startup (this is used to manage startup apps, but windows currently suggest to use the task manager instead when configuring the startup apps.), and Tools (this is where you can find various tools that we can run to configure the operating system further) tab. 

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

### DAY 5 - SEARCH ENGINES ### 
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

### DAY 7 - WINDOWS DOMAIN AND ACTIVE DIRECTORY ###

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

### DAY 8 COMMAND LINE, POWERSHELL, LINUX ### 
For day 8, I learned about the Command Line, Powershell, and Linux’s shell, Bash. 
Command Line, unlike using the GUI is a text-based interface wherein we can use fewer resources, for automation, and for faster interaction with your system. This module introduced the different commands to navigate through your system in a easy level. Here are the commands: 
Commands are usually in PATH directories, so whenever we use a command it searches PATH directories for the executable 
-	set (This lists all the variables within your system) 
-	ver (This gives the Windows version)
-	systeminfo (gives an in-depth information about your system’s hardware and software)
-	cls (clears the command line)
-	more (pipelined to commands that have a long output)
-	help (used after a command to get more information on how to use it)
-	 ipconfig (Information about your network’s IP, like subnet mask, gateway, and address)
-	ping (for testing connectivity by sending an icmp request)
-	 tracert – (checks all the router path you went through before reaching the address) 
-	netstat – (shows established connections [TCP/UDP])
-	cd (changing directories/current directory)
-	dir (viewing child items)
-	mkdir (make folders/directories)
-	rmdir (remove folders/directories)
-	type (prints output of a file)
-	copy (copying files)
-	move (moving files)
-	erase/del (deleting files)
-	tasklist (view all processes that are running)
-	taskkill (stops a process)
-	chkdsk (checks the file system and disk for errors)
-	driverquery (installed device drivers)
-	sfc /scannow (scans and repairs files)
Next, is the Powershell. The powershell was created for the purpose of automation and configuration management. This is more powerful compared to Windows’ CLI as this is object-oriented. That means that output will always have property and a function. These make it much more powerful since it can identify what the output is and not just a string of letters and numbers. 
To enter powershell, we just type “powershell” in the Command Prompt. 
Commands are structured as verb-noun, here are the commands I’ve learned:
-	Get-Content (outputs the content of a file) 
-	Set-Location (changes directories)
-	Get-Command (all the commands we can use), we can filter it via -CommanType “type”
-	Get-Help (used to view a command and how it is used)
-	Get-Alias (get the popular commands of linux and cmd and its equivalent to powershell)
-	New-Item (creates files or directories)
-	Remove-Item (deletes files or directories)
-	Copy-Item (copy files or directories)
Along with these commands, I was also introduced to what piping is. Piping is the method of using 2 or more commands. It uses the output of the previous command as an input to further filter your commands. 
Examples:
-	Get-Command | Sort-Object Length (sort them based on their length)
-	Get-Command | Where-Object -Property “Extension” -eq “.txt” (finds all objects that are .txt) (pick what it shows)
-	Get-Command | Where-Object -Property “Name” -like “ship*” looks for objects that starts with the name ship
-	Get-Command | Select-Object -First 5, picks which to show (first 5 files)
-	Get-Command | Select-String functions like grep to check files and it’s content that will have the string specified.

System Information 
-	Get-ComputerInfo (functions like system info)
-	Get-LocalUser (users/status/description)
-	Get-NetIPConfiguration (network info)
-	Get-NetIPAddress – (ip addresses of the interfaces used)
Real-Time System Analysis 
-	Get-Process (shows the processes that are running)
-	Get-Service (services in the system)
-	Get-NetTCPConnection – established TCP connections, address, port, state. 
-	Get-FileHash (generates a hash, used for mionitoring, for footprint of the object)
Scripting 
-	Invoke-Command, these run scripts and can be sued to run remotely to another machine. 

Lastly, I was introduced to what the shells are in Linux and scripting. Scripting is basically a line of commands, like a to do list, that when executed will run based on you commands. 
But before that, we have shells. Echo $SHELL to know what shell you are using, and echo /etc/shells for the different shells you can use. 
We have BASH (Bourne Again Shell), this is the default in Linux. Is more on the mid tier, it can be customized, but it is limited. Can be used for automation, and configurations. Has tab feature, and history.
Next is Fish (Friendly Interactive Shell) – beginner-friendly, customization is good, it comes with highlighting, simple syntaxes, and even auto correct. 
Then, ZSH (ZShell) – modern shell, tab completion, also has customization, and has great scripting capabilities. 
For scripting: 
To first create a script, we first create a file that has the type .sh. example: Nano script.sh
Every script will start with a shebang, #!, this tells your system what shell you are using. 
example: #!/bin/bash, this uses bash.
Example code: 
Nano simple_script.sh 

Inside simple_script.sh:
#!/bin/bash
#declares variables, these are comments. They do not alter your script. Used to make understanding what script and line does. 
username=””
university=””
password=””

#below uses the for function for iteration from 1-3
for i in {1..3}; 
do
echo “University”
#read is used to input our answer to the variable. username in this case
read username
echo “University:”
read university
echo “Password:”
if [ “$username” = “Benigno” ] && [ “$university” = “PRMSU” ] && [ “$password” = “102603” ]; then
echo “Hello, Benigno! Access Authorized”
#this makes it so that it goes out of the loop when credentials are correct 
break
else
echo “You only have 3 tries, this is try number $i”
fi
done
if [ “$i” -eq 3 ]; then
echo “You have been denied access”
fi

To run this we first change the mode for the script since executable isn’t added in yet. We use the command chmod +x simple_script.sh
To run it, we just specify the directory it is in like ./simple_script.sh
Above shows loops like For that iterates the given numbers, and If else, for the condition that the names should match, and if not output this. Conceptually, it works like other languages so it’s very easy to learn, and I enjoyed this part the most. 

That’s a wrap for Day 8, and I’m always eager to learn more! 

### DAY 9 – SOLIDIFICATION OF NETWORK FUNDAMENTALS ###
Day 9, was an easy read, this just gave additional information about the things I learned in network fundamentals. 
The OSI Model, 7 layers that describes how data is encapsulated and decapsulated. The layers are as follows: 
1.	Physical Layer – this talks about the medium of data, like is it a fiber optic? A CAT6? This also talks about the transmission of data, is it using electricity? Light? 
2.	Data Link – this is where packets are encapsulated with their frames. Their destination and source mac address. 
3.	Network Layer – this is where the data inputs a header of source and IP destination. 
4.	Transport Layer – implements the connection that it will establish. TCP/UDP
5.	Session Layer – this layer focuses on establishing and maintaining a connection between the client and the host. 
6.	Presentation Layer – this layer focuses on encryption of our data, compression, and translation.  
7.	Application Layer – this is where the protocols that we mostly use happen, such as the HTTP, DNS, Mail, etc. 

TCP/IP Model was also discussed. Basically, it’s like The OSI Model, but it only has four layers.
1.	Application Layer – Functions like layers 5, 6, and 7 of the OSI model.
2.	Transport – implements the type of connection that is going to be established, TCP/UDP
3.	Internet – IP address source and destination, logical
4.	Link – MAC address source and destination and also the Physical layer

TCP/ IP model is a practical solution of its predecessor, the OSI model. This explains what happens. While the OSI model is used for understanding how data moves and how it is encapsulated. 
Encapsulated data looks like this 
[Ethernet/Wifi Header][IP][TCP/UDP][DATA][Ethernet/Wifi Trailer]
IPs and Subnets were also discussed. 
IP addresses, have two types. IPv4, which has 4 octets (32 bits). xxxx.xxxx.xxxx.xxxx (in binary)
IPv6 has 128 bit since it uses hexadecimal values xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx. 
Subnetting is the process of assigning what are the network values, and what are the host values. The most common are /24, /16, /8. We can also borrow if host bits aren’t enough or we want to conserve IP addresses by only taking in what we need. 
IP addresses also fall into two classifications. Private and public.
Private is used in our LAN, while Public is used to connect outside our network, like the internet. 
Routing was also discussed, this is the logical process of sending data into the proper network. How data travels from one network to another, and what path it chooses.

We also have UDP and TCP. Again, these are the protocols established regarding what service we are trying to access. UDP, are connectionless, so if the protocol requires speed over reliability we choose UDP. If reliability, TCP. 

TELNET (Teletype network), nowadays this is used for analyzing TCP connections and Network information since using this for commands and configurations isn’t secure like the SSH.
The module also introduced DHCP (Dynamic Host Configuration Protocol), this is usually what current routers do in our homes or almost everywhere, like public WiFis. What this does is it assigns our device an IP and the proper configuration of its subnet mask, gateway, network address, broadcast address, and its dns server. 
It has 4 steps, 

D – our device broadcasts in the 255.255.255.255 address for an IP address via UDP packetport 67. 

O – host offers an IP

R – client requests and clarifies

A –host acknowledges

And since we don’t have an IP yet, this happens in Layer 2 or the MAC address layer. It communicates via the link layer. 
We also have ARP (Address Resolution Protocol) – this is used for connecting to an unknown IP within our network. It uses MAC address. For example 192.168.1.1 is requesting a connection to 192.168.1.2, but it doesn’t know where it is. ARP handles this by using the sender’s MAC address along with its requested IP to the broadcast address of the mac which is FF:FF:FF:FF:FF:FF, and then it’ll flood all the devices and the destination’s MAC address will reply that it has it. 

Next is the ICMP (Internet Control Message Protocol) these is used for network diagnostics, ICMP requests are usually sent via the ping command. Ping tests the connectivity with a given address. It sends ICMP request 8, and the destination will send back type 0 if it is reached. Another one is the tracert, this traces the route that the data will take via TTL, so it knows how many hops it’ll take before it reaches the destination. Once it reaches it, the receiver will send ICMP type 0 again. 

When it comes to routing we also have different protocols that take place in different networks. We have OSPF (Open Shortest Path First), used in medium to large networks and route is mostly based on bandwidth.

EIGRP (Enhanced Interior Routing Gateway Protocol) – route is passed on bandwidth, delay, reliability and load. This is used on CISCO networks. 
BGP (Border Gateway Protocol) – route is based on policies, used on the internet by ISPs.

RIP (Routing Information Protocol) – route is based on the number of hops, and is used in small networks

And the last topic that was discussed is the NAT (Network Address Translation), this is basically having different private IPs in our LAN with their port pair, and when it comes to connecting outside our LAN every device will use a dedicated public IP along with its port so the host knows the destination, and the device that will receive it inside the network. 


### DAY 10 – CORE AND SECURE PROTOCOLS ### 

For Day 10, I learned more about the main protocols that usually take place when browsing the web. I learned about the secured and not secured version of these protocols, and how they differ from each other. 

DNS, or the Domain Name System is used to map keywords, or the name of the website to their corresponding IP address. This makes it so the IP address can be mapped and we can have an easy time remembering the websites that we want to visit. There are different types of DNS records, we have the A (IPv4 address), AAAA (IPv6 address), CNAME (this redirects the domain name to another domain name), and MX (this is used to know what domain will the email be sent to, so what domain is responsible for handling it). 

There’s also what we call the WHOIS records, these records holds the information of the DNSs information like how the owner is, the name of the domain, when was it created, when was it last updated, etc. This gives us a clear insight of the different DNS that exists in the internet. But if you want to be a owner of a DNS not every information can be public, it can also be private. 

Next is the HTTP, or the HyperText Transfer Protocol. This is used for accessing web pages. This is the protocol that takes place. Almost all of these protocols happen in the Layer 7, or the Application Layer. This protocol has commands like GET, for accessing what part of the website we’re looking to go to, and other like PUT, POST, and DEL. This uses port 80.

FTP on port 21, or File Transfer Protocol. As the name says, this is used to transfer files. By logging in, if a server is available to use we can connect to it, view its files, download, upload, or even delete files that are in the server. 

SMTP on port 25, or Simple Mail Transfer Protocol. Again, it is a protocol that handles how mails are SENT. This is mainly for sending mails. 

For receiving files, we have the POP3 :110, and IMAP :143 (Internet Message Access Protocol). The only difference they have is that POP3 is mainly used for single device compared to IMAP, and the email in POP3 protocol, once downloaded to your device are deleted from the server. Making them unavailable if you lose your mail or accidentally delete it. This is where IMAP comes in play, IMAP let’s you synchronize your emails, meaning that these mails are securely stored online and downloading it doesn’t mean that I’s deleted after. It’s stored in the mail server, making it accessible to multiple devices of a user.

These protocols are not secure, making them easily sniffed when an attacker is in your network. The different data like what you’re trying to access, what you’re putting it, the files you are accessing and downloading you user and password, the emails you are receiving and sending, are not secured. This is where TLS comes in.

The Transport Layer Security protocol is an added protocol to the existing protocols mentioned to make them secure. TLS uses TLS certificate for the verification if it’s signed and given by the CA (Certificate Authority). This process of verifying the server happens during the handshake along with the giving of the public key of the server (this comes along with the certificate, if it doesn’t match it’s not authenticated). Client uses all these to match if it’s correct, if it’s authenticated and a shared symmetric session key is given for both the client and server for encryption and decryption of packets. TLS happens after the TCP handshake. TLS is implemented Layer 6, or the Presentation layer. If a security protocol is in place, this is where it is implemented. HTTPS, SMTPS, POP3S, AND IMAPS all use the TLS protocols. These makes it so that the data sent isn’t in plain text and it’s in gibberish form. Only with the key can we decrypt this data. 

We also have SSH or Secure Shell, this was created to make using shells, commands, remote access, and configuration via shell, secure. TELNET, was used for this task but TELNET isn’t secure and data could be sniffed when using TELNET.  

That’s why we have SFTP and FTPS, both are File Transfer Protocol, but SFTP (entire session is encrypted) uses SSH while FTPS (commands and optionally data are encrypted) uses TLS. 

Lastly is VPN, Virtual Private Network – it is a secure, encrypted tunnel that lets us access remote networks as if we are a part of that network, this lets us access the resources within that network. Let’s say for example we want to access a server in Japan. We can use VPN to make it so that our device feels like it is locally connected to that specific part of Japan along with its network configuration. 


### DAY 11 ### 
For Day 11 I learned about what Wireshark and Tcpdump, and how the basics of how they are used. 

Wireshark, it’s a software that allows us to capture and read packets on our interfaces. It is used for troubleshooting problems in our network, detecting anomalies, and learning more about how protocols that we can’t see work. Wireshark only captures and reads data and doesn’t modify it. Its sole purpose is to have a deep understanding, analyzation, and learn of what packets are and their contents, and how they behave. 

I learned how it is used by either exporting already captured packet files, .pcaps our using the capture feature inside Wireshark. There are a few features that enable us to have an easier time navigating through Wireshark. These features are: 
1.	Colouring packets for easier time to identify anomalies or different sets of rules of the color used. 
2.	The capture button for capturing packets. 
3.	We can also merge pcap files
4.	View file details for an in-depth overview of our .pcap files.

For dissecting a packet there are a lot to it. There are the presented columns that we can see when we capture or open a .pcap file. It has the time, the source, destination, the protocol used, and the length info on the column. This column can be modified to add or remove columns. 


A packet might have the following frames when you click on it: 

1.	The frame layer, metadata about the capture (frame number, timestamps, length).
2.	Source [MAC], this is for the data link layer like mac address source and destination. 
3.	Source [IP], this is for the IP, source and destination also 
4.	Protocol, the protocol used either UDP/TCP
5.	Protocol errors, this is where you will see the packets that need to be reassembled. 
6.	Application Layer – the specific protocol used
7.	Application data, the specific data that was generated can be shown here.


We can also Go to a packet, find a packet (this is by using the content inside it), mark packets (highlighting it), packet comments (comments inside a packet that can be used for describing and informing), export packets (export the packets to differentiate them from your actual point of interest ), export file as objects (this comes directly from our network), and then we have expert info to look for warnings that are present like, chat, note, warn, error. They rank from least to most severe.

Lastly, we have packet filtering, this lets us filter different types of rules that we want when capturing or viewing packets so that we can narrow it down to what we’re actually interested in investigating. 
1.	Apply as filter, click on the property and apply that filter. 
2.	Conversation filter, works if we want multiple properties that we want to filter out like the IP destination or source or the protocol that is being used etc. 
3.	Colourise Conversation, this lets us highlight the packets related to the color we’ve chosen for easier identification. 
4.	Prepare as filter, let’s you create a display filter that isn’t applied instantly and will be executed once you tell it so.
5.	Apply as columns, let you add and remove columns. 
6.	Follow stream let’s you see the exchange and the data that is happening between the protocols that take place. 

Next, we have Tcpdump, this works the same, but Tcpdump is used within a terminal, so it is purely text and command-based interaction. It does however capture packets like wireshark but is limited in its deisplay since it is text-based and is much more lightweight and efficient compared to Wireshark. It still helps us analyze packets via a terminal. Tcpdump can also save captures for wireshark if you need an efficient way of capturing packets and then analyzing it in-depth in Wireshark. 
The commands used are: 
1.	Tcpdump -I [name of the interface], the interface we want to capture. We can reveal interfaces by using the command : ip address show. 
2.	Tcpdump -w file, writes the captured packet to a file
3.	Tcpdump -r file, reads a file
4.	Tcpdump -c [count], limit the number of packets you want to capture
5.	Tcpdump -n, makes it so the domain isn’t resolved
6.	Tcpdump -nn, don’t resolve domains and protoclol numbers
7.	Tcpdump -v, or -vv to make the make the packets more detailed as they are captured.

Herea re the filtering expressions that we can use:
1.	Filtering by host: tcpdump host [name of host] or [ip], tcpdump src host [IP], tcpdump dst host [IP]
2.	By port: tcpdump port [number], tcpdump src port [number], tcpdump dst port [number]
3.	By protocol: tcpdump [protocol used]

Logical operators used are: or, and, not
There are also advanced filtering:

1.	Greater [length] or less [length] – talks about the size
2.	Binary operators &, |, and !.
3.	Header bytes can also be examined for specific analyzation of the bits inside a byte. 
4.	proto[expr:size] – proto refers to the protocol used, expr, for what index we start off at first, and the overall bytes we want to capture. 
5.	We can also use flags of the tcp, syn, ack, fin, rst, push. Example, tcpdump "tcp[tcpflags] == tcp-syn" – capture only tcp-syn flags.

And lastly we have how packets are displayed 
1.	-q quick and brief information
2.	-e, include mac address
3.	-A, ASCII encoding
4.	-xx, hexadecimal format
5.	-X, both in ASCII and hexadecimal format

This was the basics of both worlds: Wireshark and tcpdump

### DAY 12 ### - NMAPS, CRYPTOGRAPHY 

For Day 12, I learned about what NMAP is a network scanner for live hosts, services, and the hosts’ ports. We can identify live hosts via nmap -sn [IP/Subnet/Target/Hostname]. This will resolve the output of all its specified targets if it’s up or down. And -sL when it lists the target, no scanning is done and just lists the specified range. It uses ARP protocol when it’s within its local network, and ICMP when it’s outside the network. 
Aside from the host, there’s also port scanning, and example would be -sT. This checks TCP ports via communicating with them with a full TCP handshake. A full TCP handshake will be initiated and when it’s closed, the port will immediately send an RST packet to drop the connection. -sT scans the common 1000 TCP ports before stopping. 
Another version of it is called the -sS, this is stealthy compared to the -sT as this only sends a SYN packet. When the port responds with a SYN-ACK, NMAP doesn’t complete the handshake and responds with a RST packet.

We can also scan UDP ports via -sU. Packets here are often empty but it does send payloads when it knows the protocol being used fro reliability purposes. When it doesn’t respond that it’s unreachable and the connection goes through, it’s open and if it does respond it’s closed. 

Since in default it scans 1000 common ports, we can limit it by the flag -F that only scans 100, and we can also input the range of ports via p[range].

We can also detect the version of the hosts device, and what services the ports are using, and force scan. -O for OS detection, -sV adds the service, and -Pn scan the hosts that are appeared to be down. 

We can also control how fast and how many probes it uses since security protocols might trigger if we go to fast, and we can also use this to manage the resources of our device. 
We can add the -T flag along with its value to set how fast we are to scan it. T0-T5, with T5 being aggressive and takes the fastest. 
--min/max-parallelism <num of probes> and --min/max-rate <number>, and we can specify the waiting time for a target host via –host-timeout.
Lastly, we can change the outputs we are getting by using -v for verbose to -vvvv if we want it very detailed. We can also use -d for debugging. We can also save these files based on the type we want them to be 
-oN (normal output), oX (XML), -oG (grep-able), -oA (all majot formats.)

Next is Cryptography, cryptography in short makes sure that we are safe by ensuring secure communication over a network. It deals with authentication, authenticity, confidentiality, and the integrity of the data that is moving within the network. Cryptography is important as it protects us and our data from sniffers and attackers that may want to steal, alter, or get information from the packets that we receive, it protects sensitive data, and makes sure that who we are talking to is that person and not just someone impersonating him/her. 

The key terms when it comes to cryptography are: 
1.	Plaintext, this is the raw data that we are trying to send to someone. 
2.	Cipher, this is the algorithm that is the foundation of encrypting and decrypting a message. This is made public as we have keys that we used when it comes to encrypting or decrypting or both. 
3.	Ciphertext, this is the secure data that is received or sent once the cipher is applied. 
4.	Keys, we have public and private or shared keys that are used to encrypt and decrypt data. Keys are made private and not sent over the web unless it is asymmetric encryption where the sender needs to have the knowledge of the public key. 
An example of encryption and decryption would be the Caesar Cipher. This basically shifts the keys of a given word with a constant number. This means that if we shift password to 5 keys the resulting answer would be – ufxxbtwi. That is the process of encrypting. And to decrypt it we need to know the value or brute force it by checking every number of key shifts. That is called decrypting. This is the process of cryptography. 

In encryption we have 2 types. We have what we call Symmetric and Asymmetric encryption. 
Symmetric encryption deals with one private key. This private key is a shared session key that is used to decrypt and encrypt messages. Both parties decide on this key and use it together. This is called a shared session key. 
On the other hand, asymmetric encryption deals with two keys. The private and public keys. This is owned by the receiver. The public key is used for encrypting the message (this is accompanied by a certificate along with a signature stating that this host is authenticated an can be trusted) and the private key for decrypting.  Although in practice, asymmetric encryption is used for authentication and symmetric is the one used for encrypting and decrypting of data. 
Basic math also accompanies cryptography, this is used for validating integrity of the data, the authenticity of the message, and is also used for generating keys. Math like XOR (exclusive or). Means that they must be of different value to be 1. And modulo where the answer is the remainder. 

### DAY 13 – PUBLIC KEY CRYPTOGRAPHY BASICS, HASHING, JOHN THE RIPPER ### 
 Asymmetric encryption is generally slower compared to Symmetric, that’s why this is used for the 1st phase of cryptography. This is used to authenticate the hosts that we are trying to connect to. An example of asymmetric encryption is called the RSA. 

The RSA is responsible for generating a key pair for, let’s say a service, even before we connect. The public key created for that server is put into a certificate that is signed by the governing body CA. This certificate from the CA is what allows hosts to be trusted over a network. A simple example math that explains these generation of key is with using two prime numbers (in practice both of these are very large numbers containing 600 digits per number) = n. N is made public. And then we also have the totient of N. This is private. After the computation we can get e and d. (n, e) is public and (n, d) is private. The flow is as follows: 
Alice and Bob (Bob is the Server and Alice is the Client) – Client wants to verify the server. 
Alice sends a challenge to the server 
The server computes It via its private keys (n, d) let’s say we have an output M. 
M is sent back to Alice, and Alice computes it with (n, e) giving the output M’. 
M = M’, it is authenticated. If not, it is dismissed and if we are trying to connect to a http server, the browser will show a warning. 

After the RSA, we have what we call the Diffie-Hellman Key Exchange or DH. This is used to establish a shared secret wherein the symmetric key is derived from. In practice DH generates a secret that is used to generate the shared key that is used for encrypting and decrypting data after the RSA is done with the authentication. The exchange of secrets also happens using modulo and using two integers. This will result in a value k, that will have the same value. 
SSH, when connecting to a secure shell that the SSH client doesn’t recognize, it will prompt the public key that the server we are trying to connect to and if we want to connect to it. This is a precaution for attackers that might use fake servers to connect to us instead. Checking the public key is vital here. In previous discussions, whenever there are exercises that connect to the SSH only a password is required, but that comes with its own risk. That’s why SSH also has public and private key verifications. Ssh-keygen is the command that generates these pairs and we can choose what type of algorithm we want to use. Using “man ssh-keygen”, can list the available key pair algorithm available.
To generate a pair we use the command ssh-keygen -t [key_algo], after this it will be generated. During generation it will prompt us to answer if we want a passphrase or not. Passphrases are used to protect our private key. This is used so that whenever we want to use this private key, it will prompt what the passphrase is. This protects it so even if an attacker knows the value of the private key, an added passphrase can be beneficial. The passphrase is a key to that private key. 
We can also specify what private key we want to use when connecting to a remote connection via ssh -i privateKeyFileName user@host. 
 We can also store keys that we can trust in /.ssh/authorized_keys folder. Key authentication is more secure than using password to authenticate. 
Next, is the PGP software. This is used to generate asymmetric key pairs and used to encrypt files and generate signatures. 
We also have the GPG which is an open-source implementation of the OpenGPG standard. This is mainly used to protect the confidentiality of email transactions and can be used to sign an email message for its integrity. Gpg –full-gen-key is used to generate the key pair, this will prompt us what algorithm we want to use, which elliptic curve (this is used for added layer for computing the value), how long should the key be valid, name, and email address.  

Public keys are used to encrypt the message if someone wants to contact the creator of that public key. 
gpg --import [file_name], is used to import a key 
gpg –decrypt [.gpg file ], to decrypt messages. 
Next is hashing, hashing is the process of creating a one-way irreversible string of your data. That can protect the integrity of the data and provide password confidentiality. This makes it so that passwords are not stored in the servers but the hashed value of that password. Although there might be a possible hash collision, this should be preventable by a good algorithm and good security as to not create duplicate hash for attacking.
That’s why choosing a good password, and a good algorithm can prevent our passwords from being compromised. Salt is a random generated value that is appended  or prepended to our password before hashing to produce a unique hash. This makes the value of our password unique even though we might have the same password as others. That’s why choosing a great password and applying practices that involve generating a good password is required. A weak password can be in the database known as the Rainbow Table, that have precomputed hashes. 
Since there are different type of hashes that are valid in the Unix, Linux environment, they are classified based on their respective algorithms. Hashes may start with these prefixes to identify them: 
$y$ - yescrypt
$gy$ - gost-yescrypt
$7$ - scrypt
$2b$, $2y$, $2a$, $2x$ - bcrypt
$6$ - sha512crypt
$md5 - SunMD5
$1$ - md5crypt.
Next is how we can crack passwords. We can use software like John The Ripper or Hashcat. 
For hashcat we can use the command hashcat -m <hash_type> -a <attack_mode> hashfile wordlist. Specifying what type of hashing algorithm is needed for us to accurately crack the hash. 
As for files, we have what we call the HMAC (Keyed-Hash Message Authentication Code), this uses a cryptographic hash function in combination with a secret key to verify the authenticity and integrity of data. This authenticates that the person who created the message is who they are and that the data hasn’t been modified in any sort of way.  
Then lastly, I learned about John the Ripper and how to use it. John the Ripper is a hash-cracking algorithm that uses a form of attack called a dictionary attack. Dictionary attack, works by providing the list of words that it will try from. Such as the rockyou.txt from the leaked website of rockyou.com. It can crack Window Authentication hashes, unshadow linux hashes, crack password protected zip and rar files, and crack ssh keys. Cracking hashes falls in the NP (Non-Deterministic Polynomial Time) category, as it relies on the computed hash for verification if it’s correct or not. Polynomial time on the other hand talks about problems that are solved by an algorithm in relation to time. Meaning as input increases, the runtime it takes to solve it and the load also increases in number. 

John the Ripper, to work efficiently needs a list of candidates of password to check, and to know what the hashing algorithm is (this isn’t necessary since it has a function that automatically detects hashes, but knowing the hash could provide a way better result.) 
Syntax: 
john [option] [file path]
Examples:
john –format=raw-md5 –wordlist=/desktop/passwords/rockyou.txt hash.txt, this code works by providing the hash you want to crack and the list of candidates that it will use to crack the hash. We can specify the hashing algorithm via the format, but if we don’t know it can automatically detect what hash it is.
We can also unshadow the hashes in etc/shadow in Linux. This contains all the hashed password and the data such as who the user is, and other data related to the password. Accessing etc/shadow requires root admin privileges. To crack this we can use the syntax: 
unshadow [passwd] [shadow] , this generates the unshadowed output that can be used to feed to john the ripper via the john [option] [file path] command. 
Unshadow, merges the data and creates an output that can be fed to John the Ripper. 
Next, we have what we call single crack mode. Single crack mode uses a method called Word Mangling, basically this tries to change or add values based on user information. It also uses the GECOS field that stores user information that can be used to mangle the words. 
--single can be added as a flag to enable this mode. 
We also have Custom Rules that we can create by editing out the conf file of john. The common custom rules that we can add are how we uppercase or lowercase letters, adding numbers, and adding symbols. 
We define the rule by creating a syntax [List.Rules:Name of Syntax]
Below this is the modifiers that we want to add, the most common are: Az(appends the given character/s), A0(prepends the given character/s), c(capitalizes the letter positionally). After that we define the characters that we want to insert. [0-9] for numbers, [0] for isolating just one number to insert, [A-z], will include both upper and lowercase, [A-Z] for only uppercase, [a-z ] for only lowercase. An example rule would be 
cAz”[5][!]” – this creates a rule that capitalizes the first letter and appends 5 or !. 
We can add the flag –rule=[nameofrule] to our syntax to use it.
We can also crack the hashes of password protected files like zip and rar. 
zip2john, and rar2john are used for their respective file extensions. 
zip2john .zip > zip_hash.txt , this creates an output hash of the file and generates a text that we can feed to john. rar2john also works this way.
And lastly, we have ssh2john extracts the hash and is fed to john to crack the passphrase that is used in a private key for authentication. The code is as follows: 
ssh2john [private key file] > passphrase.txt , this is then fed to john to crack it. 


### DAY 14 – Exploitation Basics ### 
For Day 14, I learned the basics of exploitation, and how to use Metasploit. 
As an introduction I was exposed to Moniker Links and the exploit revolving around it back in February 13, 2024. It revolved around Outlook’s vulnerability in relation to moniker links inside emails. 
Moniker Links are COM object references that can be represented using URLs that specify resources that can be a part of an email that was sent. When clicked normally, this prompts a dialog box. This will warn the user and then ask if it wants to open it. But this could be misclassified by using the character “!”. There is a bug that’ll treat the moniker link as an okay url and will continue to access the resource. 
Let’s say we want to attack someone via this method, we will create a hyperlink that will be sent to the victim that will contain a file://IP/test!exploit... 
This will misclassify it and since it is misclassified it won’t trigger the Protected View and will trigger an automatic authentication. This is where the exploit comes in. The attacker has a device, that’s the machine IP that was used in the hyperlink. It also has a fake server set-up. When the victim clinks the link it will try to authenticate itself via the server since it is accessing a resource from the attacker’s machine. The server will send the NTLM challenge and then the user will send its username along with the NetNTLMv2 response. Since we already know all the data except for the password. Cracking the password offline via tools like John The Ripper can be possible. 

Next, we have the introduction for Metasploit.

Metasploit is an exploitation framework that can be used in the cyber security world. Metasploit supports all phases from inputting information to post-exploitation. 

Metasploit is an exploitation framework that supports the exploitation phase and has 3 distinct parts. The command to run the terminal of Metasploit is the msfconsole that uses the Metasploit framework that is not an OS since it is not interacting with the OS but with the framework itself. We also have modules, that are also executed by the Metasploit framework which are predefined software within the framework that are not standalone programs. Tools, such as msfvenom, are standalone programs that are executed by the OS since they are not part of the Metasploit framework. 
The main components of Metasploit are as follows: 
Vulnerability – a weakness in the target’s services that might be misconfigured, low security, or weak protocols in place. 
Exploit – exists in the attacker’s system, specifically the Metasploit framework. Exploits interact with the vulnerable services in a way that can cause an unintended irregularity in the target’s execution state. 
Payload – exists on the Metasploit Framework and is delivered to the target’s system, and executes within the execution context. 

The available msfconsole commands can be viewed via help. This will list the available commands with their description. Aside from the specific commands from Metasploit, it also supports most Linux commands. When using a module, you need to invoke the command “use” followed by its path. Payloads are different as they are set via “set [name of payload]”
Once inside a module, you can invoke the command “show options” and int will show the parameters within that module. These parameters will also show a description of what it is and it will also show what parameters needs to have value. 

We can also use “search [keyword]” if we’re looking for a specific module with that name, the type of us that it will run, what type of exploit it is, etc. There are typically 5 command prompts, we have the regular terminal (this is outside of the Metasploit console. This is our shell). We have the Metasploit console, and then we have The Metasploit console when it has a module selected. We have a Meterpreter session, and we have a shell that is given by the Meterpreter when we invoke the command “shell” 

Talking about Meterpreter, this isn’t a regular command prompt like a shell. As this doesn’t live on the disk but lives in the memory alongside other processes. Meterpreter also communicates over the network and it can be encrypted to avoid detection. Meterperter acts a C2 agent. It has its own set of commands, that have their set of functionalities and these are handled by the modules. A meterpreter session can inlined or staged. When it is inlined, the meterpreter session is active even before the session is established. It sits locally and is just idle when this happens. When it is staged, it usually opens after a connection is established. Meterpreter session let’s us interact with the device and is part of the post exploitation stage. 

Modules have different types, we have Auxiliary, Encoders, Evasion, Exploits, NOPs, and Payload. 
Auxiliary are supporting modules like scanners, crawlers, etc. 
Encoders encode the exploit and payload. 
Evasion helps with evading antivirus to avoid detection. 
Exploits, as we’ve mentioned, capitalizes on the vulnerabilities to alter a system’s behaviors that will create an execution context. 
NOPs, this provides buffers for payload for specific sizes. 
Payloads are the code delivered through the target system and executed within the execution context. Payloads can be categorized into four types. Adapters (these are used to convert to different formats), Singles(Self-contained payloads that are bulk in size, these are used for faster executable payloads), Stagers (These setup the connection and downloads the Stages), Stages (This is the actual full payload.) Both allow the use of larger payloads in comparison to inline. 
Post Exploit, these either gather, escalate, interact with files, etc.

Next is the Exploitation Process. The following are the steps on how I perceived the flow: 
1.	Scanning your target(s). Can be multiple, can be one. But usually it starts with scanning the target through their ports and looking at what services are running their. We can invoke commands that can identify vulnerabilities in the system with nmap. 
2.	After the scan, and we now know the vulnerability. Although there are auxiliary modules that we can use to further refine our exploit. We can look for specific modules that can aid us in exploiting the vulnerability present in the system. 
3.	After choosing an exploit related the vulnerability, we can choose a payload. An example would be a reverse_tcp that will return a meterpreter session. When run, the attacker will listen for incoming connection from the target which has an outbound connection to our IP and specified port. After the connection has been established, a Meterpreter session will be given to you. 
4.	When a meterpreter session has been created, this is now the post-exploitation part where we can gather more information, elevate our privilege, even spy on our subjects, manipulate their system, collect their files, etc. Invoking the command help, let’s you see the possible commands with a meterprer. Things like hashdump is possible. 
There’s also a tool that is called msfvenom and this basically translates modules into a format you want it that’s based on the target’s system or OS.
This was the process that I did with the Blue activity where I had to exploit the system by applying all these things. This was a fun room and I enjoyed it a lot since it helped me build my foundation on how exploitation works. 

### DAY 15 – WEB APPLICATION BASICS ### 
For this room, it gave me a brief rundown on what the Web is and the parts that make it put. 

Frontend – is the appearance that we see whenever we browse. It has three parts, HTML (The structure of the webpage, and content of the webpage), CSS (This is what give customization of how the webpage will appear), and JavaScript (This gives the functionality of the webpage).
Backend – these are the things that we don’t see also gives additional functionality and foundation for our webpage. It has 3 common parts. Database (This is where data is stored, retrieved, changed, and managed), Infrastructure components (These can be made up of servers, physical devices like routers, and software that support the webpage), and WAF (Web Application Firewall, this filters out what goes in and out of our Web Server)
Frontend and Backend coexist with each other to build a working and functional website. 
Going back to webpages, we access them by typing out a URL like facebook.com, youtube.com, or Instagram.com. These are examples of domain and they are a tiny part of the URL or the Uniform Resource Locator. The URL has many parts, below is an example:
http://user:agent@tryhackme.com:80/file?id=1#task3

http is the scheme or the protocol used. 
User:agent is a key value pair of user and password that is used for authentication. Although this practice isn’t used since this exposes sensitive information from the URL. 

Tryhackme.com is the host or domain. This is the website that we are accessing. 
80 is the port that corresponds to the protocol used. 
/file is a specific part of the page that we are trying to access.

?id=1 is called the Query String that is used for user input, usually when searching for something within the domain 

#task3 is a fragment and it points to a specific part within the webpage. With this example it’s In path /file that is pointing to task3, so this is existing somewhere in the path.  

But in order to see the contents of the webpages, there exists a conversation with the client and the server that makes this happen. These are called HTTP messages and is broken down into two. 

HTTP request and HTTP response. 

HTTP request is from the client side and is sent to the server. It contains the Start line which has the HTTP method, the path, and the protocol with its version. 
HTTP method are commands that we are instructing the server to do. The methods are as follows: 
1.	GET – this fetches data from the we server. Like accessing a different part of the webpage. Whenever we use GET URL is reflected. So security is advised here, specially for sensitive data. 
2.	POST – updates or creates data to the server. 
3.	PUT – this replaces or updates, for full updates 
4.	DELETE – removes data
5.	PATCH – updates resources, these are partial updates , modifies 
6.	HEAD – this retrieves headers 
7.	OPTIONS – shows what methods are available. 
8.	TRACE – for debugging, shows methods that are allowed. 
9.	CONNECT – creates a raw TCP tunnel, can be used when there is a proxy. 


Below that is the Header, this contains additional information that is in the form of key value pairs. We have the content-type, or what browser we are using, the domain, or even the cookie (this is a stored information about previous sessions).  
An empty line, which marks the end of the header and the start of the body. 

The body, this usually contains the data that we are trying to send to the server. The body can have different types, the common 4 are: 
URL encoded – key value pairs that are separated by =, per pair is separated by the character “&”. 
Form Data – Per data is separated by a boundary string. This is mainly used for uploading, downloading or sending files. 

JSON – these are also value pairs that is separated by “:”, this is used for structure. 

XML – Data in here is structured within tags similar to HTML formatting.   	

The server then responds to this with a HTTP response. 
This has a Status line, contained here are the HTTP version, Status Code (the value response of the web server), Reason phrase (The explanation for the status code).
Below are the Response and the allocated code for it. 

Informational Response (100-199) – partly receives and still waiting for the rest 
Successful Response (200-299) – received and worked. 
Redirection message (300-399) – means that the website relocated to somewhere different
Client Error Responses (400-499) – missing, problem with request from client. 
Server-Error Response (500-599) – server encountered problems 
Below the status line is the header which consists of key-value pairs too. It can contain the date, content-type, the server handling it, or even cache-control (this is a temporary storage of data. So you don’t need to load it all up again but is stored there until it timeouts.)

But we also have what we call the Security Headers. By the word itself, these are used to improve a secured interaction with the server and client against bad actors. Below are 4 examples: 

Content-Security-Policy – this basically permits where content comes from and which are reliable. 

Strictly-Transport-Security – this is used for ensures that the browser connects to HTTPs
X-Content-Type-Options – this is to combat against guessing what the MIME type is and instead trusts the Content-Type to handle data detection since this can be used to malicious codes.

Referrer-Policy – this controls if the URL is going to be sent or not. This controls the amount of information sent. This can be configured so only the scheme is sent, or only the domain is sent, or the full URL sent. 

Above is a great way to apply security to our web servers so sensitive information can’t be sniffed easily and can protect us from browsing. This is how the client-server communicates whenever we access anything in the internet. 

### DAY 16 – JavaScript Essentials ### 
The JavaScript language. This language, an interpreted language, is used to define the functions and actions of a website. It’s constructed the same as how other programming languages are constructed. It has variables, operators, data types, loops and functions to create the actions that we want. 

JavaScript, in relation to HTML, has two types. It can either be internal or external. 

Internal means it’s basically inside the HTML and is coded in it, external means It’s outside the HTML and is in a file of its own that has an extension of .js that is called in the HTML. 
Internal or external JS can be verified through looking at the page source. 
With JavaScript we can create dialogue boxes that can prompt a user for an input. Here are some examples: 
alert (“YOU ARE HACKED”). This generates a dialogue box with this text along with an ok button. 
prompt (“How old are you?”). This outputs the text and creates a blank form which you can input from. This will return a value or null based on your input.
confirm (“Are you 18?”). This generates a true or false value with an ok and cancel. 
These dialogue boxes or prompts can easily be bypassed if programming is bad and security is weak. A simple inspect in the page source can easily reveal what the logic of the page is. Which can cause the website to be compromised. These are client-side authentication which is not a good practice to implement when building a website.

With that being said, viewers can be slowed down by obfuscation (adds code, shortens, makes it so the logic doesn’t make sense at an instant) and minification (shortens the code) of the source code. This doesn’t mean that an attack can be stopped though, some websites provide de-obfuscation and de-minification.

That’s why the best practices are, we shouldn’t rely on client-side authentication, refrain from adding untrusted libraries, and avoid hardcoding sensitive information, and obfuscate and minify source codes.


### DAY 17 – SQL FUNDAMENTALS ### 

Day 17, was about learning the fundamentals of SQL. SQL is a part of the backend side of a website or just about anything that might store, retrieve, or manage a collection of data. 

SQL or the Structured Query Language is a language that is specifically used for relational databases which can manage the collection of data that we create. 

Relational databases, on the other hand, is a type of database that focuses on data having relationship with other data. This can be distinguished by a primary key(is a unique identifier to the table that will have other data related to it), or a foreign key (a foreign key is a primary key from another table). We can then use THE DBMS (Database Management System) to manage a specific or a collection of databases. 

I learned about the MySQL and these are the commands that I learned with it: 
-	mysql – u name – p used to login to your account with your database 
-	CREATE DATABASE;
-	SHOW DATABASES;
-	USE db_name  switches to a specific database
-	DROP DATABASE db_name  deleted a database
-	CREATE TABLE table_name ( book_id INT PRIMARY KEY, book_name VARCHAR(255), publication_date DATE); an example of creating a table within the database that we’ve chosen. 
-	SHOW TABLES; 
-	DESCRIBE table_name; describes the columns within it
-	ALTER TABLE table_name modify something about the table
-	CRUD OPERATIONS (Create, Read, Update, Delete), these are the basic command when it comes to accessing data. 
-	C – INSERT INTO table_name, creates a new row along with data 
-	R – SELECT * FROM table_name; this shows the table * is used to specify that all columns are chosen
-	U – Update table_name 
SET column_name = “ “
WHERE primary_key = ‘
Updates a table, and always use primary key since it’s unique. 
-	D – DELETE FROM table_name WHERE column_name = value; deletes a record
-	Clauses – this specifies the criteria of data being manipulated. THM focused on 4. 
-	GROUP BY column_name; creates a pile of grouped data based on what we want. 
-	 DISTINCT – used usually with SELECT and outputs values that are unique. 
-	ORDER BY – this is mainly used for how data is presented. Ascending or descending. 
-	HAVING – is a conditional clause, usually used when GROUPED BY is created, although not necessarily explicit to GROUP BY; 
-	I also learned about operators which just returns Boolean values, LIKE, AND, OR, NOT, EQUAL TO, NOT EQUAL TO, LESS THAN, GREATER THAN, LESS THAN OR EQUAL TO, GREATER THAN OR EQUAL TO. These can be used to further filer out data that we want to see. 
-	FUNCTIONS, these are commands that does a specific job and works on each row individually. 
-	CONCAT() – used for merging SELECT CONCAT (name, “string“, category, “string”) AS column_name FROM table_name; or we can use GROUP_CONCAT();
-	SUBSTRING() – shows the given string based from your parameters SELECT SUBSTRING(column_name, 1, 4) AS name FROM table_name; 
-	LENGTH() - returns number of characters
-	COUNT() – returns number of rows. 
-	SUM() – sum of a given data field, MAX() – form ax value, MIN() for minimum value. 
Above are a few examples of the basic syntax of MySQL and is used to manage data. This helped me understand how data is stored and how it can be managed, and how important it is inbeing organized. 

Burp Suite is an exploitation tool used for penetration testing for web applications and mobile applications. Burp Suite is used for intercepting packets, viewing them, modifying them, for testing attacks and for automation of attacks to a server. 

Knowing this, I was introduced to the tools within Burp Suite, these were: 
1.	Burp Proxy – this sits between the client and the web server. This is what makes it possible to intercept HTTP messages and modify them. 
2.	Repeater – messages that are from the proxy are usually sent here, and this is where we manually modify HTTP messages to test our hypothesis and carry out these hypotheses by sending them and checking if an unintended behavior will occur. This helps us understand how the target behaves.
3.	Intruder – this is mainly used after the repeater since this is where our attacks are automated and validated. Information gathered from the repeater is crucial here since knowing how the target responds means a higher chance of our attacks working. 
4.	Comparer – this is used for comparing two outputs and checking the tiniest differences. 
5.	Decoder – this analyzes data mainly asks the questions why is it represented this way, or why was it chosen to be like this. This can help in understanding why the packet is the way it is 
6.	Sequencer – this checks the randomness and predictability of tokens like a session ID. 
The introduction mainly focused on using the Burp proxy, the browser within Burp itself and configuring a proxy via an extension. 
We can capture packets by interacting with a web application we want, and we can intercept them by turning the intercept under the Proxy Tab. Turning the intercept on will delay the packet from reaching the target and we’ll have to modify and analyze the packet. HTTP messages contain data that can be helpful for us when it comes to penetration testing. A simple attack could be an XSS where scripts can’t be loaded into forms via the website but can be edited in the HTTP message. 

This room showed me a glance of how powerful Burp can be when it comes to security assessment of a website application. 

Next is Hydra, although this was such a short room. A new tool has been added to my knowledge. 

Hydra is an online password cracking tool for applications that have a login form like SSH, HTTP, FTP, RDP, and SMB. This can be compared to John the Ripper as it uses a wordlist but the only different thing is John the Ripper is offline and safer compared to Hydra as it is online.

Hydra sends actual login attempts so using it blindly can activate security measures such as locking us out, limiting our responses, blocking us that can compromise our attack. So reconnaissance before using it is a must to achieve better results. 

Tyhackme showed me two examples. SSH and HTTP 
For ssh, the code is as follows: 

Hydra -l <username> -P <path to wordlist> <target_IP> -t 4 ssh 
-t limits the number of threads used so it doesn’t overload and send too many responses that can activate security measures. 

For HTTP, the code is as follows: 
For http, the type of message is used, so in this case it’s a POST message. 
Hydra -l <username> -P <Path to wordlist> <target_ip> http-post-form “/location:username=^USER^&password=^PASS^:Prompt when login fails”  

I was also introduced to a reconnaissance tool called Gobuster, this tool is also used for penetration testing and for security assessment. This is a tool that enumerates possible files, paths, and domains that aren’t linked or advertised within a website. This tool also uses a wordlist to check different responses to see if something exists or not. 

I was introduced to three types of it: 
1.	Web directories/Files – this is a path from a domain that isn’t seen or advertised but exists if manually typed in the URL. These can contain admin pages or secrets that are sensitive and shouldn’t be publicly available. 
The code is as follows gobuster <command> and then followed by flags that can help, in this case the code is gobuster dir –u “URL” -w <path to wordlist>  -x .php, .js  (x just specifies what type are we looking for) 
2.	Subdomains – so these are the child domains that coexists with a main domain that is registered in the DNS server. So when checking for subdomains, we basically interact with the DNS server to check if if a certain subdomain exists or not. 
The code is as follows: gobuster dns -d domain -w <path to wordlist> 

3.	VHosts – or Virtual Hosts, these are subdomains that may or may not be registered in the DNS server and I can be configured within the web config instead. So instead of checking with the DNS server, we now check responses as this sends different host headers checking if a virtual host will respond. 
The code is as follows: gobuster vhost -u “URL” -w <path to wordlist>, but shortening it like this can cause us to miss vhosts since a lot use FQDNS and simple changing the Host to admin is different from admin.thm.com 

so we can use the code gobuster vhost -u “URL or IP” -d example.thm -w <path to wordlist> - - append-domain --exclude-length 250-320 













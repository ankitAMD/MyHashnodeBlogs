---
title: "Day3- Devops"
seoDescription: "Elevate DevOps efficiency with Linux. Unleash seamless integration, automation, and reliability. Optimize your development workflow with Linux's robust foun"
datePublished: Sat Nov 25 2023 15:31:31 GMT+0000 (Coordinated Universal Time)
cuid: clpe7ligj000608labs8y06wk
slug: day3-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/2EJCSULRwC8/upload/4241c996a4b8ca28c3a7aba7128a5662.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700920041802/b991df2c-80e9-4801-8ad4-0beb4132b6d4.png
tags: cloud, linux, aws, automation, devops

---

In general, Linux offers four installation methods:

1. Dual Boot Setup
    
2. Virtual Box Installation
    
3. Default Installation
    
4. Cloud Deployment (AWS, Azure, GCP)
    
    Distinguishing Terminal, Console, Shell, and Command Line:
    
    Explore this Blog - - [**Terminal, Console, Shell, and Command Line**](https://medium.com/analytics-vidhya/difference-between-terminal-console-shell-and-command-line-2441322b9b90)
    

### What is the Cloud?

Cloud computing is a technology that enables users to access and use computing resources (such as servers, storage, databases, networking, software, analytics, and intelligence) over the internet (the cloud) instead of owning and maintaining physical infrastructure. It provides on-demand access to a scalable and flexible pool of resources, allowing organizations to quickly scale their IT infrastructure based on their needs, pay for what they use, and reduce the complexity of managing hardware and software. Essentially, cloud computing offers a more efficient and cost-effective way to deliver and consume computing services.

For more information visit this Blog -

1. [**CLOUD Computing — Types and its Benefits.**](https://medium.com/analytics-vidhya/why-and-what-is-cloud-computing-474e917ac040)
    
2. [**The Top and Best Cloud Providers in the World.**](https://medium.com/analytics-vidhya/the-top-and-best-cloud-providers-in-the-world-d97fecd06cde)
    

### [**Why AWS? Advantages and Disadvantages.**](https://medium.com/analytics-vidhya/why-aws-advantages-and-disadvantages-f0e666b869b3)

[For More Details visit This Blog- AWS](https://medium.com/analytics-vidhya/why-aws-advantages-and-disadvantages-f0e666b869b3)

[![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700766581911/b98bbd54-1291-4f76-a9e0-8cc62b8fb472.png align="center")](https://aws.amazon.com/about-aws/global-infrastructure/)

In AWS (Amazon Web Services), global infrastructure refers to the vast network of data centers and resources strategically distributed around the world. This infrastructure is designed to provide low-latency, high-performance, and reliable services to users globally. Key components of AWS's global infrastructure include:

1. **Regions:** AWS divides the world into geographical regions, each containing multiple availability zones. A region is a separate geographic area, such as US East (North Virginia) or Asia Pacific (Mumbai).
    
2. **Availability Zones (AZs):** Each region consists of multiple availability zones, which are essentially isolated data centres with redundant power, networking, and cooling. These zones are interconnected to provide high availability and fault tolerance.
    
3. **Edge Locations:** These are additional points of presence worldwide used by AWS CloudFront (content delivery network) to cache and deliver content to end-users with lower latency.
    
4. **Wavelength Zones:** These zones provide ultra-low latency and high-throughput communication between devices at the edge of the network and AWS services.
    

The global infrastructure of AWS allows users to deploy applications and services in multiple geographic locations, ensuring redundancy, fault tolerance, and optimal performance for a diverse range of workloads. It also enables users to comply with data residency requirements and address regulatory concerns by choosing specific regions for their resources.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700766523272/338943c3-c79f-4e2b-96e3-4441d1afe265.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700766539596/64a10e27-e811-4fee-ad94-7bfc89d876a9.png align="center")

As AWS continues to grow over time, the information above may be subject to change.

Start a Linux Server\*\*:\*\* [**How to Create and Launch an AWS EC2 Linux server in 5 minutes**](https://medium.com/aws-in-plain-english/how-to-create-and-launch-an-aws-ec2-linux-server-in-5-minutes-24100a6d56ff)

### **Fundamental Advanced Commands: (Commands used in day-to-day activities).**

1. `date`
    

```bash
date   #date (no option): With no options.
date -u      #Displays the time in GMT(Greenwich Mean Time)/UTC(Coordinated Universal Time )time zone. 
date --date=" string " #Displays the given date string in the format of date (--date or -d).
date --date="2 year ago" #Using –date option for displaying past dates
date --set="Tue Nov 13 15:23:34 PDT 2018" #To set the system date and time -s or –set option is used.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700907926184/93a1c6ed-dc02-44be-90c3-806cc5c51d1d.png align="center")

**List of Format specifiers used with date command:**

```bash
%D: Display date as mm/dd/yy.       
%d: Display the day of the month (01 to 31).       
%a: Displays the abbreviated name for weekdays (Sun to Sat).
%A: Displays full weekdays (Sunday to Saturday).
%h: Displays abbreviated month name (Jan to Dec).
%b: Displays abbreviated month name (Jan to Dec).
%B: Displays full month name(January to December).
%m: Displays the month of year (01 to 12).
%y: Displays last two digits of the year(00 to 99).
%Y: Display four-digit year. 
%T: Display the time in 24 hour format as HH:MM:SS.
%H: Display the hour.
%M: Display the minute.
%S: Display the seconds.
```

```bash
date "+%D"
date "+%D %T"
date "+%Y-%m-%d"
date "+%Y/%m/%d"
date "+%A %B %d %T %y"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700908680885/e4134db9-fc11-4da5-934c-a2cfd3ed5032.png align="center")

1. `cat` - Cat is like a handy tool that helps you look inside files and show their content on the screen. You can also use it to change files.
    

```bash
cat -b : It adds numbers to lines that are not empty.
cat -n : It puts numbers on all lines, making them easy to count.
cat -s : If there are many empty lines, it puts them together, making things neat.
cat -E : It shows a dollar sign at the end of each line, marking where the line ends.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700910360990/a171c92a-6636-40e4-ad65-3359d4efe85a.png align="center")

1. `Sort:` This command is used to sort the results of the search either alphabetically or numerically. It also sorts files and directories.
    
    ```bash
    sort -r: the flag returns the results in reverse order.
    sort -f: the flag does case-insensitive sorting.
    sort -n: the flag returns the results as per numerical order.
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700910766754/2cdbc0fa-2806-48eb-8e07-e51b9c16d5a8.png align="center")

1. `Tail:` This command prints the last N number of data of the given input. By default, it prints 10 lines.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700911023501/ae33ffe1-4242-438c-ac6e-4f54866f2493.png align="center")

1. `Ping:` This command will ping a host and check if it is responding.
    
    1. `-c count: Specifies the number of ping packets to send.`
        
    2. `-i interval: Sets the time interval between successive ping packets.`
        
    3. `-t timeout: Defines the maximum time to wait for a response, in seconds.`
        
    4. `-s packetsize: Specifies the size of the data portion of the ping packet.`
        
    5. `-q: Quiet mode. Displays only summary information at the end.`
        
    6. `-v: Verbose mode. Provides more detailed information during execution.`
        
    7. `-f: Flood mode. Sends a large number of packets quickly for testing.`
        
    
    ```bash
    ping google.com
    ping -c 4 google.com
    ping -i 2 amazon.com
    ping -t 5 yahoo.com
    ping -s 64 microsoft.com
    ping -q openai.org
    ping -v wikipedia.org
    ping -f example.com
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700911615407/1ce2cdee-5e24-45a9-b43f-66e5683b3206.png align="center")
    
2. `Lsof:` It is used to display a list of all the open files on a Linux system.
    

```bash
sudo lsof -u root
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700911832262/cfc6b474-ee72-47fe-bfcd-2633c8aa477d.png align="center")

1. `Ifconfig:` This is used to configure the kernel-resident network interfaces.
    

```bash
ifconfig
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700912087381/c501aa99-d401-4083-b0b1-a77afac275c9.png align="center")

1. `ID:` This is used to find out user and group names and numeric IDs (UID or group ID) of the current user or any other user on the server.
    

```bash
id
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700912181199/14dad24c-eb12-4ba0-a29c-d2b5c86cdf09.png align="center")

1. `Cut:` This command is used to extract specific fields or columns from a file or standard input.
    

It is often combined with other commands, such as sort, uniq, and grep, to perform more complex text-processing tasks.

```bash
cut  -c1-2 fruits.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700912413722/f92bf9d9-b033-4c74-9d5e-83b5a61b303c.png align="center")

1. `Sed:` This is used to perform basic text transformations on an input file. It stands for "stream editor" and is a powerful tool for editing text files or streams in a Linux environment.
    
    ```bash
     sed 's/Plum/Icecream/g' fruits.txt
    ```
    

The `sed` command is used for stream editing and, in this case, is applied to the file `fruits.txt`. The provided expression `'s/Plum/Icecream/g'` is a substitution command that replaces all occurrences of the word "Plum" with "Icecream" in the file.

* `s`: Indicates substitution.
    
* `/Plum/`: Specifies the pattern to be replaced (in this case, "Plum").
    
* `/Icecream/`: Specifies the replacement text (in this case, "Icecream").
    
* `g`: Stands for global, meaning it replaces all occurrences on each line.
    

**Effect:** Any occurrence of the word "Plum" in the `fruits.txt` file will be replaced with "Icecream" after running this `sed` command.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700912869743/741a047e-2eec-450d-a086-4f95ed225a6a.png align="center")

1. `ssh user@host` **–** connect to the host as a user.
    
2. `Ssh-keygen:` This command is used to generate a public/private authentication key pair.
    
3. `nslookup:` The `nslookup` command is a network administration tool used for querying the Domain Name System (DNS) to obtain domain name or IP address information. It stands for "Name Server Lookup."
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700913584669/ca231799-4b71-439c-9991-3fb4a2dd9c2e.png align="center")

14.`Free:` This command displays the total amount of free space available along with the amount of memory used and swap memory in the system, and also the buffers used by the kernel.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700913611604/18d9004c-a876-40f2-9c79-d21ad4ff8ef8.png align="center")

1. `Df, du:`
    
    `df` Command: The `df` command, which stands for "disk free," is used to display information about the available disk space on file systems.
    
    ```bash
    df [options] [filesystem...]
    
    #Options:
    #        -h or --human-readable: Display sizes in a human-readable format.
    #        -T or --print-type: Print file system types.
    
    df -h
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700917623126/215fc66d-7333-4159-8410-38ba2ddca9d5.png align="center")
    
    `du` Command: The `du` command, which stands for "disk usage," is used to estimate the space used by files and directories.
    
    ```bash
    du [options] [directory/file...]
    
    #Options:
    #        -h or --human-readable: Display sizes in a human-readable format.
    #        -s or --summarize: Display only a total for each specified file.
    
    du -h /path/to/directoryorFile
    du -sh
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700917938991/20eecf11-0b36-487a-908a-0b67b767ab96.png align="center")
    
    **Key Differences:**
    
    * `df` provides information about the overall disk space usage and availability on file systems.
        
    * `du` focuses on estimating the space used by specific files and directories.
        
2. `Htop:`This command is used to monitor the system’s resources and processes that are running in real-time.
    

```bash
htop
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700918054738/c52682f0-4e93-49f8-a949-27acb830a9f3.png align="center")

1. `Ps:`
    
    We use the ps command to check the unique ID behind every process.
    
    * **a** = show processes for all users
        
    * **u** = display the process’s user/owner
        
    * **x** = also shows processes not attached to a terminal.
        
        ```bash
        ps aux
        ```
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700918216751/edecc300-102f-4587-ad88-67c609f4eeb5.png align="center")

1. `kill` **Command:**
    
    The `kill` command in Linux is used to terminate processes manually by sending signals to them. The basic syntax is:
    

```bash
kill [options] <pid> 
# Here, <pid> is the process ID of the process you want to terminate.
```

```bash
Options: 

-s or --signal:
# Specifies the signal to be sent. If not provided, the default signal is TERM (terminate).
# Example: kill -KILL <pid>Example: kill -s SIGTERM <pid>

-l or --list:
# Lists all available signals.
# Example: kill -l

-9 or --signal 9 or SIGKILL:
# Forces the process to terminate immediately by sending the SIGKILL signal.
# Example: kill -9 <pid>

-15 or --signal 15 or SIGTERM:
# Sends the default termination signal, asking the process to terminate gracefully.
# Example: kill -15 <pid>

-HUP or --sighup:
# Sends the SIGHUP signal to the process.
# Example: kill -HUP <pid>

-INT or --sigint:
# Sends the SIGINT signal to the process.
# Example: kill -INT <pid>

-KILL or --sigkill:
# Sends the SIGKILL signal, forcefully terminating the process.
# Example: kill -KILL <pid>

-l or --list:
# Lists all available signals that can be used with the -s option.
```

```bash
Terminate a process with a specific PID:
kill 1234

Terminate a process using a specific signal:
kill -s SIGTERM 1234

Forcefully terminate a process:
kill -9 1234

List available signals:
kill -l
```

**Note:**

* The default signal sent by `kill` is `SIGTERM`, which asks the process to terminate gracefully.
    
* Using `SIGKILL` (`kill -9`) should be done cautiously as it forcefully terminates the process without allowing it to perform cleanup actions.
    

1. `traceroute` **Command:**
    
    The `traceroute` command is a network diagnostic tool used to display the route (path) that packets take to reach a destination on a network. It shows the IP addresses of the routers or hops along the way and measures the time it takes for packets to travel from the source to each router and the destination.
    

```bash
traceroute [options] <destination>

#<destination>: The target domain name or IP address.
```

```bash
Options:
-4 or -6:
#Forces the use of IPv4 or IPv6, respectively.
-n:
#Does not resolve IP addresses to hostnames.
-q <queries>:
#Sets the number of queries per hop.
-w <seconds>:
#Sets the maximum amount of time to wait for a response.
-m <max_hops>:
#Sets the maximum number of hops to search for the target.
```

```bash
traceroute -n www.google.com
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700919438657/42fbe4cc-9ff7-4120-aed6-c866f8a074c3.png align="center")

1. `telnet` **Command:**
    

The `telnet` command is a network protocol used for interactive communication with another host over a TCP/IP network. It allows a user to connect to a remote system or device and interact with services running on that system.

```bash
telnet [options] <hostname> [port]

# <hostname>: The host or IP address of the remote system.
# [port]: The port number to connect to (optional, default is 23 for Telnet)
```

```bash
Options:
-l <username>:
# Specifies the username to use when connecting to the remote system.
-t:
# Forces the use of character mode (text mode).
-a:
# Attempts automatic login.
-e <escape_char>:
# Sets the escape character.
-n <net_spec>:
# Specifies the network virtual terminal (NVT) to use.
```

```bash
telnet google.com 80
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700919749077/43beaf4e-0dbd-416c-9eb3-cfefd75a2d14.png align="center")

1. `tee` command:
    

The `tee` command in Unix-like operating systems is used to read from the standard input and write to both the standard output and one or more files simultaneously. It is a simple yet powerful command that finds applications in various scenarios.

```bash
command | tee [OPTION]... [FILE]...

# command: The command whose output you want to redirect to a file.
# [OPTION]: Optional parameters that modify the behavior of tee.
# [FILE]: Optional file(s) to which the output should be written. If not specified, tee writes to the standard output and no files.
```

```bash
Options:
-a or --append:
# Appends the output to the specified files rather than overwriting them.
-i or --ignore-interrupts:
#Ignores interrupt signals, allowing tee to continue writing to files even if interrupted.
```

```bash
echo "hello dosto " | tee -a file10.txt
# Print and Store in a File.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700924021844/036c6b39-abbc-4c4b-9f37-70ff97fb79bf.png align="center")

Store to File:

```bash
echo "hello dosto" > boom.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700924100256/b8bc2889-fa8f-443e-ac29-f52561282113.png align="center")

1. `wc` Command:
    

To count the number of lines, characters, words, and bytes in a file, you can use the `wc` command with the `-l` option. For example:

```bash
wc -l filename #To count the number of lines in a file.
wc -w filename #To count the number of words in a file.
wc -m filename #To count the number of characters in a file.
wc -c filename #To count the number of bytes in a file.
wc filename    #If you want all of these counts together.
```

Replace `filename` with the actual name of the file, you want to count the lines for.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700909951268/43fbf1dc-edd6-4a57-bdcc-56401f11f0ac.png align="center")

1. `useradd command` : To create a user.
    
    ```bash
    sudo useradd [options] username
    
    # sudo: Executes the command with superuser privileges.
    # useradd: Command to add a new user.
    # [options]: Additional options you may want to specify.
    # username: The username you want to create.
    ```
    
    ```bash
    sudo useradd -m devops
    
    Options: 
    -m :
    #when you use -m, the useradd command not only creates the user account 
    # but also sets up the associated home directory, typically located 
    # in the /home directory.
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700924925400/f836b5b9-4274-40f1-940e-cae086650aef.png align="center")
    
2. `passwd` command: To set a password for a user.
    
    ```bash
    sudo passwd username
    
    # Replace username with the actual username for which you want to 
    # set the password.
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700925195041/a40113c8-b762-45ab-baee-8e911358bd35.png align="center")
    
    when you create a new user using the `useradd` command, a corresponding group with the same name as the user is typically created. This group is known as the user's primary group. The `useradd` command automatically handles the creation of the user and the associated group.
    
    `/etc/passwd`**:**
    
    The `/etc/passwd` file is a system file on Unix-like operating systems that stores essential information about user accounts. Each line in this file represents a user account and contains several fields separated by colons (`:`).
    
    ```bash
    john:x:1001:1001::/home/john:/bin/bash
    
    # john: Username
    # x: Placeholder for the encrypted password (actual password stored in /etc/shadow)
    # 1001: User ID (UID)
    # 1001: Group ID (GID) of the primary group
    # /home/john: Home directory
    # /bin/bash: Default login shell
    ```
    
    `/etc/group:`
    
    The `/etc/group` file is another system file that stores information about groups on the system. Each line in this file represents a group and contains several fields separated by colons (`:`).
    
    ```bash
    john:x:1001:
    
    # john: Group name
    # x: Placeholder for the group password (not commonly used)
    # 1001: Group ID (GID)
    ```
    

`/etc/shadow :`

The `/etc/shadow` file is a system file on Unix-like operating systems that stores encrypted user password information. It is a critical component of system security, ensuring that user passwords are stored securely. The `/etc/shadow` file is typically readable only by the root user to prevent unauthorized access to sensitive password information.

```bash
john:$6$RJ1wFtuN$hDmcT.4P97QWdCcoo6jy6Y5fUpvsjTPUaa1SQ7Nmy7JXqNJK6dmfD51jo9F2i2LMnX7AJvs6.1hX/3P8wACoW0:18740:0:99999:7:::
```

**<mark>Note:</mark>**

* The password hash is the critical component that ensures the security of user passwords. It is generated using a one-way cryptographic hash function, making it computationally infeasible to reverse and obtain the original password.
    
* Access to the `/etc/shadow` file is restricted to the root user to prevent unauthorized access to password information.
    

`lsb_release -a :`

The `lsb_release -a` command in Linux is used to display detailed information about the Linux distribution. When you run this command, it provides information such as the distributor ID, description, release number, and codename of the distribution.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700926005748/0a061d02-5069-4634-ada3-fd710802e339.png align="center")

<mark>Note : Please avoid/don't use the below following command:</mark>

```bash
# rm -rf /

" This command can have severe consequences, as it forcefully removes all 
files and directories starting from the root directory, leading to 
data loss and system instability."
```

### **Day 3 Task: Basic Linux Commands**

Task: What is the Linux command to -

1. <mark>To view what's written in a file.</mark>
    
    ```bash
    cat file1.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700856105575/69f6e5ca-f679-450c-b0c5-161e02a097b8.png align="center")
    
2. <mark>To change the access permissions of files.</mark>
    
    ```bash
    chmod 755 file1.txt
    chmod 744 folder1name
    chmod -R 743 Folder2name  # Recursively to all Files and Folders in The Folder2name
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700857790385/010c335b-2986-433c-b510-df2b668ccadd.png align="center")
    
3. <mark>To check which commands you have run till now.</mark>
    
    ```bash
    history
    ```
    
4. <mark>To remove a directory/ Folder.</mark>
    
    ```bash
    rm -r  directoryname
    rm -rf directoryname  # You cannot remove directory using command rm without "-rf" 
    rmdir  directoryname  # You can only remove directoy when its empty using this command 
                          # there is no command rmdir -rf directoryname
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700858657764/c94ced14-7f3e-45f8-b9a9-31ef88a1cb00.png align="center")
    
5. <mark>To create a fruits.txt file and to view the content.</mark>
    
    ```bash
    vi fruits.txt  
    # nano  /path/to/your/filename
    # vim   /path/to/your/filename
    # gedit /path/to/your/filename
    
    cat fruits.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700859626742/caed9f0b-4a89-4de5-aef2-07f809d2d6a2.png align="center")
    
6. <mark>Add content in devops.txt (One in each line) - Apple, Mango, Banana, Cherry, Kiwi, Orange, Guava.</mark>
    
    ```bash
    vi devops.txt 
    #Apple,
    #Mango,
    #Banana,
    #Cherry,
    #Kiwi,
    #Orange,
    #Guava.
    cat devops.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700859823006/4f345b15-6add-4d0d-b4e7-bdfb4939196a.png align="center")
    
7. <mark>To Show only the top three fruits from the file.</mark>
    
    ```bash
    head -3 fruits.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700859969844/7fe61361-b5cd-4fef-8222-1498a3b5eff4.png align="center")
    
8. <mark>To Show only the bottom three fruits from the file.</mark>
    
    ```bash
    tail -3 fruits.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700860040696/3ebc554c-4439-47a1-8d05-be0181dd618e.png align="center")
    
9. <mark>To create another file Colors.txt and to view the content.</mark>
    
    ```bash
    vi Colors.txt  
    # nano  /path/to/your/filename
    # vim   /path/to/your/filename
    # gedit /path/to/your/filename
    
    cat Colors.txt
    ```
    
10. <mark>Add content in Colors.txt (One in each line) - Red, Pink, White, Black, Blue, Orange, Purple, and Grey.</mark>
    
    ```bash
    vi Colors.txt  
    #Add Content in Colors files
    #Red
    #Pink
    #White
    #Black
    #Blue
    #Orange
    #Purple
    #Grey
    cat Colors.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700860367151/f3e25366-3479-41d4-93be-664b86965167.png align="center")
    
11. <mark>To find the difference between fruits.txt and Colors.txt file.</mark>
    
    ```bash
    diff fruits.txt Colors.txt
    
    #or
    
    vim -d fruits.txt Colors.txt  #If you want a more user-friendly side-by-side comparison, you can use a visual diff tool. 
    #For example, you can use vim with the -d option:
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700860535988/4b6ab02e-a72c-46eb-85f2-24a9580d6d89.png align="center")
    

**Note: Day 3 GitHub Task - Completed** (see above response).

**Refer to Task3:**

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day03/solution.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day03/solution.md)

---

🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏

I sincerely hope this blog helps you save valuable time, allowing you to cherish moments with your loved ones. Keep smiling and spread the love!😄😄. Thank you for reading.🤝🤝

Your support means the world to me. If you’ve found this blog enjoyable and informative, Please take a moment to hit that cheerful Like button and share it with others. Thank you for being a part of this journey!🙏🙏.

**Follow/Connect Me:** [**LinkedIn**](https://www.linkedin.com/in/ankit-gupta2/) **|** [**Medium**](https://medium.com/@ankitgupta_974) **|** [**GitHub**](https://github.com/ankitAMD)**|**[**Hashnode**](https://hashnode.com/@NinjaAnkit)**|**[**Linktree**](https://linktr.ee/ninjaankit)**🔔🔔🔔🔔.**

**If you like the above blog Series Please Support Me through “**[**Buymeacoffee**](https://www.buymeacoffee.com/AnkitGupta1) **”.**

**<mark>Below are the Links to a series of Detailed | Step by Step of WordPress Website Hosting on AWS Lightsail :</mark>**

Part 1: [How to host a WordPress website on AWS LightSail.](https://aws.plainenglish.io/how-to-host-a-wordpress-website-on-aws-lightsail-8808b70f7f7c)

Part 2: [Find Login Credentials of the Dashboard of WordPress AWS Lighstail.](https://www.clickaws.com/find-wordpress-password-in-aws-lightsail/)

Part 3: [Setting up a Lightsail Static IP Address from Dynamic IP Address.](https://medium.com/@ankitgupta_974/setting-up-a-lightsail-static-ip-address-from-dynamic-ip-address-4a0628f63c52)

Part 3.1: [Dynamic IP address of Instances in AWS Lightsail.](https://medium.com/nerd-for-tech/the-dynamic-ip-address-of-instances-in-aws-lightsail-b3dfb1562171)

Part 4: [How to Register a Domain Name with Amazon Web Service | Register a Domain Name using AWS Route53.](https://aws.plainenglish.io/how-to-register-a-domain-name-with-amazon-80a1bf809859)

Part 4.1: [Connect a Route53 Registered Domain to AWS Lightsail Instance.](https://aws.plainenglish.io/connect-a-route53-registered-domain-to-aws-lightsail-instance-website-bdd2d57a927c)

Part 5: [Set up a Free SSL Certificate on WordPress AWS Lightsail.](https://www.clickaws.com/how-to-setup-or-enable-free-ssl-certificate-on-your-wordpress-aws-lightsail-instance/)

***Thank you for being a part of our community!***
---
title: "Day2 -DevOps"
seoTitle: "Linux for Devops"
seoDescription: "Elevate DevOps efficiency with Linux. Unleash seamless integration, automation, and reliability. Optimize your development workflow with Linux's robust foun"
datePublished: Thu Nov 23 2023 10:38:45 GMT+0000 (Coordinated Universal Time)
cuid: clpb29b29000009gtb2ck5umf
slug: day2-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/hGV2TfOh0ns/upload/3a2c70b484f43c9c0d2f8863fa3b7fb3.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700312189153/73b1ff31-bcaa-4f47-97ae-e5236c04324f.png
tags: cloud, linux, automation, devops, terraform

---

### **Intro to Linux:**

Linux is an open-source operating system, like Windows or macOS. What makes Linux special is its flexibility and power. It's widely used for servers, smartphones, and even in everyday devices. Linux is known for being secure, efficient, and customizable. Whether you're a tech enthusiast or a developer, Linux provides a playground to explore and tailor your computing environment to suit your needs. It's a key player in the tech world, supporting everything from websites to smart appliances, making it a versatile and robust choice for various applications.

### **History of Linux:**

1. Linux was created by Linus Torvalds in 1991 as an open-source operating system kernel.
    
2. Linus started it as a personal project but shared it freely, encouraging collaboration.
    
3. The kernel, combined with GNU software, formed a complete operating system known as GNU/Linux.
    
4. Linux's collaborative development model attracted a growing community of contributors worldwide.
    
5. Its stability and security features made Linux popular for servers and diverse computing environments.
    
6. Over the years, numerous distributions emerged, each tailored to specific needs.
    
7. Linux gained prominence in server rooms, powering a significant portion of web servers.
    
8. Android, a Linux-based mobile operating system, dominates the smartphone market.
    
9. The open-source nature of Linux promotes customization and adaptation to various devices.
    
10. Today, Linux is a key player in the tech world, running on servers, personal computers, and embedded systems.
    

## **Why Linux is popular?**

Linux stands out as the dominant system for over 90% of the world's top 1000 websites. What sets Linux apart are key characteristics:

1. **Cost-Free:** Linux is free, eliminating the need for any financial investment, unlike Windows.
    
2. **Open Source:** Linux is open source, allowing the public to view, edit, and contribute to its code.
    
3. **Security:** Linux is inherently secure, reducing the need for antivirus software. Regular global upgrades enhance its robust security.
    
4. **Stability and Performance:** Linux boasts high stability, seldom requiring reboots, ensuring uninterrupted performance. It excels in network and workstation scenarios, providing consistent, reliable performance.
    
5. **Community Support:** Active and extensive community support for problem-solving and knowledge sharing.
    
6. **Compatibility:** Compatible with various hardware architectures and devices.
    
7. **Server Dominance:** Dominates the server market due to reliability and scalability.
    
8. **Developer-Friendly:** Preferred by developers for its rich set of development tools and languages.
    
9. **Global Usage:** More than 90% of the top 1000 websites worldwide use Linux.
    

### The disadvantage of Linux:

1. Setting up, installing, and using it can be challenging for users who are new to the system.
    
2. The absence of a centralized organization providing support or updates makes it more challenging to seek assistance during technical issues.
    
3. Certain applications may lack Linux-compatible software, limiting options for specific uses.
    

### **Different Linux distributions**

There are numerous Linux distributions, each tailored to specific needs and preferences. Some popular ones include:

1. **Ubuntu:** Known for its user-friendly interface and extensive community support.
    
2. **Fedora:** Often used for its cutting-edge features and commitment to open source.
    
3. **Debian:** Emphasizes stability and is the foundation for many other distributions.
    
4. **Arch Linux:** A rolling-release system for users who prefer the latest software versions.
    
5. **openSUSE:** Offers a powerful and user-friendly environment, suitable for various purposes.
    
6. **CentOS:** Focuses on stability and is widely used in server environments.
    
7. **Mint:** Designed for ease of use and a comfortable desktop experience.
    
8. **Red Hat Enterprise Linux (RHEL):** A robust and commercially supported distribution suitable for enterprises.
    
9. **Kali Linux:** Specialized in cybersecurity and penetration testing.
    
10. **Manjaro:** Based on Arch Linux, Manjaro aims to make Arch more accessible.
    
11. **Slackware:** One of the oldest distributions, known for simplicity and minimalism.
    
12. **Gentoo:** Allows users to optimize the system for their specific hardware.
    

These are just a few examples, and the Linux ecosystem offers a wide range of distributions catering to different preferences, purposes, and levels of expertise.

## **The architecture of Linux:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700311805214/cefd2c4a-4f19-4e21-907b-10750ebc85e4.png align="center")

🎯At the **Hardware Layer**, we find the physical components like the CPU, memory, and storage—the foundational elements of the computer.

🎯**The Kernel** acts as the vital link between hardware and software, managing system resources, and memory, and facilitating communication among software components.

🎯**The Shell**, a command-line interface, empowers users to interact with the Linux system. It interprets commands, executes them, and presents the outcomes.

🎯Above the Kernel and Shell, **Diverse Applications and software packages** operate, handling tasks from text editing and web browsing to programming and multimedia playback.

### **Is everything in Linux either a file or a directory?**

Yes, in Linux, everything is considered a file or directory. This is a fundamental concept of the Unix/Linux operating system. In the Unix/Linux file system:

1. **Regular Files:** Ordinary files that contain data. This includes text files, documents, images, and executable programs.
    
2. **Directories:** Containers for files and other directories, organizing the file system hierarchy.
    
3. **Special Files:** Devices, sockets, and symbolic links are represented as files in the file system.
    
4. **Devices:** Hardware devices, such as hard drives and USB devices, are represented as files in the `/dev` directory.
    
5. **Sockets:** Used for inter-process communication (IPC), allowing processes to exchange data.
    
6. **Symbolic Links:** Shortcut files that point to another file or directory.
    
7. **Pipes:** Used for communication between processes, allowing the output of one process to serve as the input for another.
    

This "everything is a file" philosophy simplifies the design and interaction within the Linux system, as it allows for a consistent and unified approach to managing and accessing different types of entities.

### **Linux File System Hierarchy:**

1. In Linux everything is represented as a file including a hardware program, the fille are stored in a directory, and every directory contains a file with a tree structure. That is called File System Hierarchy.
    
2. Linux uses single-rotated, inverted tree-like structures.
    
3. Root Directory represents with / (forward slash). It is a top-level directory in Linux where everything begins.
    
    ![Linux File System Hierarchy – nepalisupport](https://nepalisupport.files.wordpress.com/2016/06/linux-filesystem.png align="left")
    
    ![The Linux Directory Structure (File System Hierarchy) Explained with  Examples | 2DayGeek](https://www.2daygeek.com/wp-content/uploads/2016/10/linux-file-system-structure-final-4.png align="left")
    
    ![Linux file system hierarchy v1.0 - blackMORE Ops](https://www.blackmoreops.com/wp-content/uploads/2015/02/Linux-file-system-hierarchy-Linux-file-structure-optimized.jpg align="left")
    
    The Linux File System Hierarchy is like a roadmap for organizing and finding files on a Linux system. Here's a simple breakdown:
    
    1. **/ (Root Directory):** The starting point for the file system. Everything branches from here.
        
    2. **/bin (Binary):** Essential binaries (programs) are needed for system booting and repair.
        
    3. **/boot:** Files for the system's bootloader, are crucial for starting the operating system.
        
    4. **/dev (Device):** Device files represent hardware components like hard drives and printers.
        
    5. **/etc (Etcetera):** Configuration files for system-wide settings and software.
        
    6. **/home:** Home directories for individual users, storing their personal files.
        
    7. **/lib (Library):** Essential system libraries used by programs in /bin and /sbin.
        
    8. **/media:** Mount points for removable media like USB drives.
        
    9. **/mnt (Mount):** Temporary mount points for additional file systems.
        
    10. **/opt (Optional):** Space for additional software packages not included with the operating system.
        
    11. **/proc (Process):** Virtual file system providing information about running processes and system status.
        
    12. **/root:** Home directory for the system administrator.
        
    13. **/sbin (System Binary):** System binaries crucial for system administration.
        
    14. **/srv (Service):** Data for services provided by the system.
        
    15. **/tmp (Temporary):** Temporary files, are often cleared on system reboot.
        
    16. **/usr (User):** Secondary hierarchy with user-related data and programs.
        
    17. **/var (Variable):** Variable data, like logs and spool files, that may change in size.
        
    
    Understanding this hierarchy helps users and system administrators navigate the Linux file system efficiently. Each directory has a specific purpose, making it easier to organize and locate files.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700735708934/a0b320c0-2d54-471a-9d85-6429f509d6a7.png align="center")
    

### **Basic Commands:**

Here are some basic Linux commands that can help you navigate and perform tasks in the terminal:

1. `pwd` (Print Working Directory):
    
    * Displays the current working directory.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700677312651/402a635b-a8e5-4ee2-ad56-48a37fbd3991.png align="center")
        
2. `ls` (List):
    
    * Lists the contents of the current directory.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700677386780/b4a8cc7b-a7f2-48c8-bed7-6b7da0b26834.png align="center")
        
        * `ls -l`\--&gt; List the files and directories in a long list format with extra information
            
        * `ls -a` --&gt; List all including hidden files and directory
            
        * `ls *.sh` --&gt; List all the files having .sh extension.
            
        * `ls -i` --&gt; List the files and directories with index numbers Inodes.
            
        * `ls -d */` --&gt; list only directories.(we can also specify a pattern).
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700734020232/0eb94ba4-a27c-4617-9fc0-0428f1720295.png align="center")
            
3. `cd` (Change Directory):
    
    * Changes the current directory.
        
        Example: `cd Documents`
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700677449175/b6cbc63d-8051-487b-9d9e-0bd1fa37be98.png align="center")
    
    * `cd ~` or just `cd` --&gt; change directory to the home directory
        
    * `cd -` --&gt; Go to the last working directory.
        
    * `cd ..` --&gt; change the directory to one step back.
        
    * `cd ../..` --&gt; Change directory to 2 levels back.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700734493010/9aeed003-2924-47e7-a84d-c4dd4d94b4cf.png align="center")
        
4. `mkdir` (Make Directory):
    
    * Creates a new directory.
        
        Example: `mkdir NewFolder`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700677680767/95f74351-e2b1-4590-847d-3c26ef83b2e1.png align="center")
        
    * mkdir .NewFolder # make a hidden directory (also . before a file to make it hidden)
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700735307552/bc8b7df4-ba47-4bf7-bd9f-9870d791624e.png align="center")
        
    * mkdir A B C D #make multiple directories at the same time
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700735103816/27f29f81-3f26-4596-aebf-6cb362f6f266.png align="center")
        
    * mkdir /home/user/Mydirectory # Make a new folder in a specific location
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700734990063/e7915c2a-270e-484e-9008-5dac6a17faba.png align="center")
        
    * mkdir -p A/B/C/D # make a nested directory
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700735209478/78303ea9-d422-4883-95aa-a4f032d34208.png align="center")
        
5. `touch` :
    
    * Creates an empty file or updates the timestamp of an existing file.
        
        Example: `touch newfile.txt`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700678505129/80ae71a9-b6db-45b6-8c30-b24b304038e5.png align="center")
        
    
    ```bash
    touch file{3..12}.txt
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700921161193/d974b7d6-7e1f-46d7-bdc0-e4964bf1d8f3.png align="center")
    
6. `cp` (Copy):
    
    * Copies files or directories.
        
        Example: `cp file.txt /destination_directory`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700718334668/934dc29a-168a-4fab-a831-79cd2fd70c17.png align="center")
        
    
    ```bash
    cp file* majedaar/
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700921279734/26a7b7f0-7ceb-4f1e-88b6-ee479a1ebe07.png align="center")
    
7. `mv` (Move):
    
    * Moves or renames files or directories.
        
        Example: `mv file.txt new_location/`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700718503365/a8471891-6433-4e2a-89da-3fd7820b81cd.png align="center")
        
8. `rm` (Remove):
    
    * Deletes files or directories.
        
        Example: `rm file.txt`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700718689960/9fb5497c-0cfd-4392-8540-d1e4e43cba70.png align="center")
        
9. `cat` (Concatenate):
    
    * Displays the contents of a file.
        
        Example: `cat file.txt`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700719326522/dcc63dfb-4be6-422f-8194-118fb4d2a4ca.png align="center")
        
10. `echo` :
    
    * Displays a message or value.
        
        Example: `echo "Hello, Linux!"`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700720725709/328ea3a7-4e06-4fe9-9ca0-2b8d7db0900b.png align="center")
        
11. `man` (Manual):
    
    * Displays the manual for a command.
        
        Example: `man ls`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700720758128/279df158-e56c-42e4-9887-b8d98abe7e17.png align="center")
        
12. `grep` :
    
    * Searches for a specific pattern in files.
        
        Example: `grep "pattern" file.txt`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700729091118/6cbb012e-5007-4856-8cc9-06d3192059ce.png align="center")
        
13. `chmod` (Change Mode):
    
    * Changes the permissions of a file or directory.
        
        Example: `chmod +x` [`script.sh`](http://script.sh)
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700729271246/c796366b-e98e-4916-9bff-27f6854c0279.png align="center")
        
14. `chown` (Change Owner):
    
    * Changes the owner of a file or directory.
        
        Example: `chown user:group file.txt`
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700731574998/3ab52bb6-f357-406c-931e-892539f7f702.png align="left")
        
15. `ps` (Process Status):
    
    * Displays information about active processes.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700731849686/3bcfda40-2e77-4a73-8600-13d87c20138e.png align="center")
        
16. `kill` :
    
    * Terminates a process.
        
        Example: `kill PID`
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700732085681/aef77e32-0dff-4049-9a8f-4ccf59c810c4.png align="center")
    
17. `uname`\-
    
    The `uname` command in Unix-like operating systems is used to print system information. It stands for "Unix Name" and provides information about the system name, kernel version, and other system-related details.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700732395529/bdd1c267-bad6-479e-850e-ca3dc47f7cf8.png align="center")
    
18. `clear`\- it is used for a clear screen.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700855543246/d3bed548-2c8e-4602-b1eb-0cf8e7e8a01b.png align="center")
    
19. `whoami` - it shows the current login username.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700855473780/24addb23-57c9-47e6-8506-8daa703ae344.png align="center")
    
20. `date` - it shows the Date and Time.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700855450313/6484a251-5524-4451-ac94-2e3605dd6191.png align="center")
    
21. `history-` it shows the list of previously used commands.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700855384714/bd1c2786-7a81-45e8-b5ee-95bb1ae731b8.png align="center")

**Note: Day 2 GitHub Task - Completed** (see above response).

**Refer to Task2:**

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day02/basic\_linux\_commands.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day02/basic_linux_commands.md)

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
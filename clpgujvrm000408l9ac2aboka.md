---
title: "Day4- Devops"
seoTitle: "Linux Advanced: "Mastering Linux Advanced Commands."
seoDescription: "Elevate your DevOps skills with advanced Linux commands. Explore efficient techniques for effective system management and optimization."
datePublished: Mon Nov 27 2023 11:49:39 GMT+0000 (Coordinated Universal Time)
cuid: clpgujvrm000408l9ac2aboka
slug: day4-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/-ZFvSWK4L28/upload/407d2efb44096ac99eec48791ec841c0.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1701085522916/ba736f65-e418-40da-b998-d7299c1c334c.png
tags: linux, aws, azure, automation, devops

---

Hello everyone, I'm on Day 5 of my DevOps learning journey, starting from Day 0. Today, I'll be discussing advanced Linux commands that are essential for DevOps and Cloud Computing tasks. As an AWS cloud engineer, these commands are crucial for my daily work. Let's explore!

In this blog, I'll cover four crucial concepts:

1. File Permissions
    
2. SSH/SCP
    
3. sudo apt/install
    
4. User Groups
    

### **1\. File Permissions**

<mark>Types of File Permission</mark>:

1. Basic Permission.
    
2. Special Permission.
    
3. Access Control List (ACL) Permission.
    

<mark>Permission Group:</mark>

Permission Descriptions:

1. owner(u)- permission used for the owner of the file.
    
2. group(g)- permission used by members of the group.
    
3. other(o)- permission used by all others.
    
    **<mark>Basic Permissions:</mark>**
    

Basic permissions control the read, write, and execute access for the owner, group, and others.

* **Read (**`r`): Allows reading or viewing the content of a file or listing the contents of a directory.
    
* **Write (**`w`): Permits to modify the content of a file or add, delete, and rename files within a directory.
    
* **Execute (**`x`): Grants the ability to execute a file (for executable files) or traverse a directory (for directories).
    

[![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701031372922/dbe46772-0fad-488d-ad74-884398cf5759.jpeg align="center")](https://twitter.com/alexxubyte/status/1532026886359879681/photo/1)

1. **<mark>Special Permissions:</mark>**
    
    * **Description:** Special permissions provide additional control over file execution and deletion in specific situations.
        
    * **Types:**
        
        * **Set User ID (**`suid`): Executes a file with the permissions of the file owner, regardless of who runs it.
            
        * **Set Group ID (**`sgid`): Executes a file with the permissions of the group owner, regardless of who runs it.
            
        * **Sticky Bit (**`t`): For directories, restrict the deletion of files to the owner of the directory.
            
    * **Representation:** Displayed as additional characters in the permission field (e.g., `rws`, `rwxr-s`, `rwxrwt`).
        
2. **<mark>Access Control Lists (ACLs)</mark>:**
    
    * **Description:** ACLs extend the basic permissions system by allowing more fine-grained control over access to files and directories.
        
    * **Features:**
        
        * **Multiple Entries:** ACLs allow multiple entries for users and groups with specific permissions.
            
        * **Granular Control:** Provides more granular control over access rights, enabling different permissions for different users and groups.
            
    * **Representation:** Displayed using the `getfacl` command to view and set ACLs.
        

**<mark>Summary:</mark>**

* Basic permissions control standard read, write, and execute access for users, groups, and others.
    
* Special permissions offer additional control over file execution and deletion in specific scenarios.
    
* ACLs provide a more flexible and detailed access control mechanism, allowing specific permissions for individual users and groups beyond the basic permissions.
    

### **2\. User Group :**

A group is a valuable tool for administrators as it allows the management and application of permissions to multiple user accounts collectively.

1. `groupadd`: Adds a new group to the system.
    

```bash
groupadd groupname # add group to system

#To check group is available or not
grep Mygroup /etc/group
cat /etc/group | grep Mygroup
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701078918700/547be259-438b-445c-ac1b-a775db090307.png align="center")

**<mark>For check group admin property:</mark>**

```bash
sudo grep Mygroup /etc/gshadow    
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701080325571/9122fd35-f51e-4a74-a163-ed555580facb.png align="center")

The `sudo grep Mygroup /etc/gshadow` a command is used to search for the line containing the group information for "Mygroup" in the `/etc/gshadow` file. If there is a match, it will display the line that contains details about the group, including the encrypted password, group administrators, and group members.

Here's what the output might look like:

```bash
Mygroup:!:::
```

Breaking down the output:

* `Mygroup`: The name of the group.
    
* `!`: The encrypted password field (indicating no password is set).
    
* `::`: Empty fields for group administrators and group members.
    

This output indicates that "Mygroup" has no password set, no designated group administrators, and no group members at the moment.

Please note that the actual output may vary based on the content of your `/etc/gshadow` file.

**<mark>For delete group Account:</mark>**

```bash
groupdel Mygroup
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701080417786/7440181a-90d9-4536-91ab-f353228a9b0a.png align="center")

To add single member to Group:

```bash
gpasswd -a ajay Mygroup
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701080736132/4ce5da54-699b-46c3-9147-6293ccbc67aa.png align="center")

To add multiple members in Group:

```bash
sudo gpasswd -M user_list group_name
```

The `gpasswd` a command is used for administering the `/etc/group` file and allows for various group-related operations on Linux systems. The `-M` option specifically is used to set or change the list of group members.

* `-M`: This option is followed by a comma-separated list of users (`user_list`) that you want to set as the members of the specified group.
    
* `group_name`: The name of the group for which you want to set or change the members.
    

```bash
sudo gpasswd -M user1,user2 examplegroup
```

This command will update the group membership of "examplegroup" to include only "user1" and "user2," removing any previous members.

Remember to replace "user1," "user2," and "examplegroup" with your actual usernames and group name.

For removing group member

```bash
gpasswd -d ajay Mygroup
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701081506075/3e319d1d-282d-44eb-b0fe-279fc5e2b88e.png align="center")

To make group Admin

```bash
gpasswd -A ajay Mygroup
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701081463377/101536c7-a2fa-4221-b8cd-033a3e071e3e.png align="center")

**<mark>Note: </mark>** when you create a user on many Linux systems, a corresponding group with the same name as the user is often created by default. This is a common convention and helps in managing user accounts and their associated groups efficiently.

**<mark>For change ownership :</mark>**

```bash
 sudo chown Ankit wordcountfile.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701084996000/7dd4ce21-5a03-4cb5-9a41-3adbed19645b.png align="center")

**<mark>For change Group ownership :</mark>**

Change group to another group.

```bash
sudo chgrp Mygroup wordcountfile.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701084698295/b75c66d7-b321-4a13-b059-00e550f5eff4.png align="center")

To check how many users are in a particular group on Linux:

```bash
getent group group_name | cut -d: -f4
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701084863106/da93a036-6d4d-4541-999a-71ac06423ebf.png align="center")

### **3\. SSH/SCP :**

1. **<mark>If you don't attach a private key are you able to do ssh in that instance?</mark>**
    
    No, Without a key pair, you can't connect to the instance through SSH.
    
    In the context of cloud computing services like Amazon Web Services (AWS) or other similar platforms, a key pair consists of a public key and a private key. When you create a new virtual machine instance (such as an Amazon EC2 instance on AWS), you have the option to associate a key pair with that instance. Here's why a key pair is necessary for SSH access and why you can't connect to the instance without it:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701000322779/f248c88b-4202-458f-8143-be05fca2f5e9.jpeg align="center")
    
    **<mark>Authentication and Security:</mark>**
    
    **Public Key (**`id_`[`rsa.pub`](http://rsa.pub)**):** The public key is placed on the virtual machine during its creation. It's used to encrypt data that can only be decrypted with the corresponding private key. It is placed in the `~/.ssh/` directory by default.
    
    **Private Key(**`id_rsa`)**:** The private key is kept secure on your local machine. It's used to decrypt the data encrypted by the public key.
    
    **<mark>SSH (Secure Shell) Protocol:</mark>**
    
    SSH is a cryptographic network protocol that allows secure communication between two computers over an insecure network. It is widely used for accessing and managing remote servers securely.
    
    When you try to connect to an instance using SSH, the server requests your public key for authentication.
    
2. **<mark>Why Key Pair is Essential:</mark>**
    
    **Authentication:** The SSH server on your virtual machine authenticates you by checking whether your public key matches any of the authorized keys in the `~/.ssh/authorized_keys` file of the user you are trying to log in as.
    
    **Encryption:** Additionally, the SSH communication between your local machine and the server is encrypted using the public-private key pair, ensuring the security of data transmission.
    
3. **<mark>What Happens Without a Key Pair:</mark>**
    
    If you create an instance without associating a key pair, there is no way for the SSH server on the instance to authenticate you securely. It won't have your public key to compare against, and as a result, SSH login attempts will fail.
    
    You won't be able to establish a secure connection to the instance, leaving it inaccessible for remote administration.
    
    <mark>In summary,</mark> the key pair ensures secure communication between your local machine and the virtual machine, allowing for authentication and encryption of data. Without a key pair, the SSH server on the instance has no means to securely authenticate and establish a connection, making SSH access impossible.
    
4. **<mark>SSH - Secure Shell:</mark>**
    
    When you create a server using a console command, it typically triggers a process called `ssh-keygen` that generates a pair of keys. These keys, known as a <mark>public key</mark> and a <mark>private key</mark>, are essential for secure communication when using the SSH protocol to connect to and manage the server. The public key is placed on the server, and the private key is kept secure on your local machine. This key pair allows for secure and authenticated access to the server.
    
5. **<mark>PPK/PEM Key :</mark>**
    
    <mark>PPK</mark> is specific to <mark>PuTTY</mark>, while <mark>PEM</mark> is a more generic and widely supported format used by many <mark>SSH and cryptographic tools.</mark> If you are using PuTTY, you might need a PPK key, and if you are using other tools, a PEM-encoded key is often more versatile.
    
6. To check if the **<mark>SSH client is available on your computer</mark>**, you can open the command prompt (on Windows) or terminal (on macOS or Linux) and simply type:
    
    ```bash
    ssh
    ```
    
    If the SSH client is installed, you should see information about the available options and usage of the `ssh` command. If it's not installed, you might get a message indicating that the command is not recognized or suggesting that you install an SSH client.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700815221646/cdebda4a-88b9-40e6-912e-fb060903dfb9.png align="left")
    
7. <mark>Steps to log into the Server using SSH Client:</mark>
    
    1. Open an SSH client.
        
    2. Locate your private key file. The key used to launch this instance is Ubuntu\_Key.pem
        
    3. Run this command, if necessary, to ensure your key is not publicly viewable.
        
        ```bash
        chmod 400 Ubuntu_Key.pem
        ```
        
    4. Connect to your instance using its Public DNS:
        
        ```bash
        ssh -i "Ubuntu_Key.pem" ubuntu@ec2-16-170-221-173.eu-north-1.compute.amazonaws.com
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700816125651/fc8fb0dc-d2eb-48e8-acc8-a3318944bb94.png align="left")
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700816148900/0f4a635b-9491-4a34-8a83-f840cad00985.png align="center")
        
8. **<mark>SCP Command:</mark>**
    
    1. To copy a file from your local computer to a remote AWS EC2 instance using SCP (Secure Copy Protocol), you can use the following command:
        
        ```bash
        scp -i  path/to/your/private-key.pem  /path/to/local/file.txt  ec2-user@your-aws-instance-ip:/path/on/remote/server
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700820278911/3275b138-947e-4884-a7fb-d74fa31f8c91.png align="left")
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700820293951/c5a2f465-eeae-4c98-931e-01512286d9ec.png align="left")
        
        ```bash
        scp -i "/Users/Ankit Gupta/Desktop/Ubuntu_Key.pem" "/Users/Ankit Gupta/Desktop/Hardening.txt" ubuntu@ec2-16-170-221-173.eu-north-1.compute.amazonaws.com:/home/ubuntu/
        ```
        
    2. To copy a file from a remote AWS EC2 instance to your local computer using SCP, you can use the following command:
        
        ```bash
        scp -i path/to/your/private-key.pem ec2-user@your-aws-instance-ip:/path/on/remote/server/file.txt /path/on/local/computer
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700820817829/921df414-210f-4b90-ac84-f4e2e4942e86.png align="left")
        
        ```bash
        scp -i Ubuntu_Key.pem ubuntu@ec2-16-170-221-173.eu-north-1.compute.amazonaws.com:/home/ubuntu/file2.txt .
        ```
        

### **4\. sudo apt/install :**

**Package Installer -**

A package installer is a software tool or system that facilitates the installation, removal, and management of software packages on a computer. These packages typically contain software applications, libraries, or other components that contribute to the functionality of a system.

On various operating systems, different package installers are used:

1. **Linux (Debian/Ubuntu):**
    
    * **Package Installer:** APT (Advanced Package Tool) is commonly used. Commands like `apt-get` or `apt` are used to manage packages.
        
2. **Linux (Red Hat/Fedora):**
    
    * **Package Installer:** YUM (Yellowdog Updater Modified) or DNF (Dandified Yum) is often used. Commands like `yum` or `dnf` are used for package management.
        
3. **Windows:**
    
    * **Package Installer:** MSI (Microsoft Installer) is a common format for Windows installers. Executable files with the extension `.exe` or `.msi` are often used.
        
4. **macOS:**
    
    * **Package Installer:** DMG (Disk Image) files or PKG (Package) files are commonly used. On macOS, the popular package manager is called Homebrew. Install a package: `brew install <package-name>`.
        

Package installers simplify the process of installing and updating software by handling dependencies, configurations, and other installation tasks. They provide a standardized and user-friendly way to manage software installations on a system.

<mark>Update vs Upgrade:</mark>

* `update` refreshes the list of available packages, while `upgrade` installs the latest versions of those packages.
    
* `update` doesn't modify the installed packages; it only updates the information about available packages.
    
* `upgrade` performs the actual installation of the latest package versions.
    

In summary, `sudo apt update` is typically run before `sudo apt upgrade` to ensure that the system has the latest information about available packages. The `update` command is about refreshing package lists, while the `upgrade` command is about updating the installed packages to their latest versions.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700821704663/4edae69c-808a-46f8-86c9-6b68f6502d50.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700821726579/d6b171a5-272a-4d5b-8da5-d7b224e6a40a.png align="center")

`Apt get`: This command serves as a versatile tool for installing, updating, and removing packages, along with managing package repository sources. Here are key apt-get commands:

`apt-get update`: Refreshes the package index files/link from the specified repositories, crucial after adding new packages or repositories.

`apt-get upgrade`: Installs newer versions of existing packages, also removing obsolete packages.

`apt-get install`: Installs one or more packages; for instance, `apt-get install nano` installs the nano text editor.

`apt-get remove`: Uninstall packages, excluding configuration files.

`apt-get purge`: Uninstall packages along with their configuration files.

`apt-get autoremove`: Removes packages installed as dependencies but no longer necessary.

**Note: Day 4 GitHub Task -**Basic Linux Shell Scripting for DevOps Engineers- You get on the Next Blog relevant to that blog.

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
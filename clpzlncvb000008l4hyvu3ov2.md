---
title: "Day6-DevOps"
seoTitle: "Shell Scripting Advanced | Advanced Shell Scripting"
seoDescription: ""Enhance your scripting skills with Advanced Shell Scripting. Dive into the intricacies of Shell scripting for a more powerful and efficient workflow.""
datePublished: Sun Dec 10 2023 14:48:02 GMT+0000 (Coordinated Universal Time)
cuid: clpzlncvb000008l4hyvu3ov2
slug: day6-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/4Mw7nkQDByk/upload/22139fb9ecc57a012212f2b3221b31cd.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1701617502816/1414e0f8-ff63-4b33-94c5-4599d8552fbf.png
tags: linux, aws, devops, shell-scripting, 90daysofdevops

---

## Shell Scripting Advanced :

1. ### Backup
    
2. ### Crontab
    
3. ### Functions
    
4. ### ACL(Access Control List)
    
5. ### **What is Backup?**
    

Backup means we have to create a copy of files/directories/projects of every day or time-interval/time stamp or monthly or yearly in minimal space which might be used for future purposes to recover files/directories/projects if any mishappen.

**Backing up involves making regular copies of files, directories, or projects on a daily, periodic, or scheduled basis, storing them efficiently to save space. These backups serve as a safeguard, enabling the recovery of files, directories, or projects in case of any unforeseen events or mishaps in the future.**

**<mark>How we can store folders efficiently?</mark>**

* We can compress or Zip the Folders/Files.
    

We can do backup in two different ways :

1. Daywise / Monthwise / YearlyWise (As per requirements)
    
2. Timestamp
    

**<mark>Let's see Some Scenario :</mark>**

* If you provided space :
    
    ```bash
    src_dir = /home/ubuntu/7DaysScript
    tgt_dir = /home/ubuntu/backup
    
    current_timestamp = $(date "+%Y-%m-%d-%H-%M-%S")
    echo $current_timestamp
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699469386571/6ad17321-a37d-472f-bdb5-2e300d80db14.png align="left")
    
    then output is :
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699469420306/dca93d6f-a24b-4cf7-bd36-a6ef3b58cde3.png align="center")
    
* If You script like this :
    
    ```bash
    src_dir= /home/ubuntu/7DaysScript
    tgt_dir= /home/ubuntu/backup
    
    current_timestamp= $(date "+%Y-%m-%d-%H-%M-%S")
    echo $current_timestamp
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699469825367/562d1fc0-ba5a-4d47-9869-20f285fd2b99.png align="left")
    
    Output :
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699469864658/5c11a29a-b206-433b-b0ee-8aeeb2ac3d5a.png align="left")
    
* If No spaces :
    
    ```bash
    src_dir=/home/ubuntu/7DaysScript
    tgt_dir=/home/ubuntu/backup
    
    current_timestamp=$(date "+%Y-%m-%d-%H-%M-%S")
    echo $current_timestamp
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699469979919/9ac56a20-979b-4754-aa4c-b108b5f14c6a.png align="left")
    
    Output :
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699470001567/2b7eaaa7-2fa8-4abe-8361-d7308899b2e3.png align="left")
    
* Here we learned how to write Timestamp:
    
    ```bash
    src_dir=/home/ubuntu/7DaysScript
    tgt_dir=/home/ubuntu/backup
    
    current_timestamp=$(date "+%Y-%m-%d-%H-%M-%S")
    echo $current_timestamp
    echo $(date)
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699475144272/7255b27c-0d5d-4f98-b257-857aedc1b99e.png align="left")
    
    Output :
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699475170093/cf80292f-a09b-4807-87ac-55f98e996e45.png align="left")
    

### **Archiving Files in Linux:**

Archiving files in Linux involves creating a compressed or uncompressed archive of one or more files or directories. Archiving is useful for bundling files, creating backups, and reducing storage space.

**What is Tar?**  
In Linux and other Unix-like operating systems, `tar` stands for Tape ARchiver 📼. It is a versatile command-line tool used for creating, extracting, and managing archive files. Archive files, also known as tarballs, are single files that contain multiple files and directories, making them convenient for data storage, distribution, and backup purposes 🗃️.

The "tar" command helps you put lots of files and folders together into one big file 📦. However, it doesn't shrink the file by itself. You can use it with other tools like gzip or bzip2 to make the big file smaller 🔄. Think of it as a double act: first, it packs everything neatly into a bundle using TAR, and then it squeezes that bundle to save space using GZIP 🌪️.

```bash
tar <options> <file>
```

* **<mark>.tgz - high compression :</mark>**
    
    Here's a summary of the most common options: 📃
    
    **Creation Options:** 🚀
    
    * `-c`: Creates a new archive file. ➕ 📁
        
    * `-z`: Compresses the archive using gzip. 🗜️ 💨
        
    * `-f`: Specifies the filename of the archive file. 📁 🏷️
        
    * `-v`: Displays verbose output, providing detailed information about the operation. ℹ️ 💬
        
    
    **Extraction Options:** 📦 🔓
    
    * `-x`: Extracts the contents of the archive file. 📤 📂
        
    * `-z`: Decompress the archive before extracting its contents (if applicable). 🗜️ 💨
        
    * `-f`: Specifies the filename of the archive file to extract. 📁 🏷️
        
    * `-C`: Extracts the contents to the specified directory. 📁 📌
        
    * `-v`: Displays verbose output during extraction. ℹ️ 💬
        
    
    **Additional Options:** ✨
    
    * `-t`: Lists the contents of the archive file without extracting them. 📃 🔎
        
    * `-A`: Appends files to an existing archive file. 📁 ➕
        
    * `-j`: Compresses the archive using bzip2 instead of gzip (optional). 🗜️ 🔋
        
    * `-r`: Replaces or updates existing files in the archive. 🔁 📑
        
    * `-W`: Verifies the integrity of the archive file. 🛡️ ☑️
        
    * `-P`: Preserves file permissions, ownership, and timestamps. 🔒 📁
        

What is Zip?

In Linux, `zip` is a command-line utility used for compressing files and creating archives. It helps you bundle one or more files or directories into a single compressed file, known as a ZIP archive. This compressed archive makes it easier to store, share, and transfer multiple files, saving disk space and facilitating efficient data management. In simple terms, the `zip` command allows you to put files together, squeeze them into a smaller package, and make them easier to handle. It's a handy tool for creating compressed archives in Linux and other Unix-like operating systems.

* **<mark>.zip - less heavy compression</mark>**
    
    **Creation Options:**
    
    * `-0`: Outputs the zip archive to standard output. 📤
        
    * `23-e`: Encrypts the zip archive with a password. 🔒
        
    * `-l <file>`: Creates a zip archive from a list of files. 📃
        
    * `-T <file>`: Excludes files and directories listed in a file. 🚫
        
    * `-z`: Uses ZIP64 format for files larger than 4GB. 📈
        
    
    **Common Options:**
    
    * `-c`: Creates a new zip archive. ➕
        
    * `-f <file>`: Specifies the name of the zip archive file. 📁
        
    * `-n <number>`: Sets the compression level (0-9). 🗜️
        
    * `-r`: Recursively zips all files and directories within the specified directory. ♻️
        
    * `-t`: Tests the integrity of a zip archive. 🔍
        
    * `-v`: Verbose output, showing detailed information during operation. 💬
        
    * `-P`: Sets the password for encrypted archives. 🔑
        
    * `-u`: Updates existing files in the archive with newer versions. 🔄
        
    * `-x`: Excludes specific files or directories from the archive. 🚫
        
    * `-z`: Compresses files within the archive using various compression methods (store, deflate, bzip2, lzma). 🗜️
        
    
    **Additional Options:**
    
    * `-A`: Adds Unicode support for filenames. 🌐
        
    * `-j`: Sets the compression level for the archive (0-9). 🎚️
        
    * `-m`: Creates a multi-part zip archive (useful for large files). 📁
        
    * `-o <file>`: Specifies the output directory for extracted files. 📁
        
    * `-q`: Quiet mode, suppresses non-error output. 🤫
        
    
    Comparison of .zip and .tgz:
    

| **Feature** | **zip** | **tgz** |
| --- | --- | --- |
| File format | Proprietary | Tar + Gzip (compressed TAR) |
| Compression algorithm | DEFLATE | Gzip |
| Default compression level | Lower | Higher |
| Encryption | Supported | Supported |
| Archiving multiple files | Yes | Yes |
| Archiving directories | Yes | Yes |
| Portability | Portable across platforms | Portable across platforms |
| Ease of use | Simpler syntax | More complex syntax |
| Common use cases | Compressing and archiving files for general use | Compressing and archiving files on Unix-based systems |

```bash
src_dir=/home/ubuntu/7DaysScript
tgt_dir=/home/ubuntu/backup

current_timestamp=$(date "+%Y-%m-%d-%H-%M-%S")
echo $current_timestamp
final_file=$tgt_dir/scripts-backup-$current_timestamp.tgz
echo $final_file

#Vi backupdata.sh
#./backupdata.sh
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699475493397/cac7b7b4-2c51-4ee2-af43-5e69dafb3850.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699475478905/8ef8da2d-8aaa-40d0-b38d-36d14a9293c6.png align="center")

```bash
src_dir=/home/ubuntu/7DaysScript
tgt_dir=/home/ubuntu/backup

current_timestamp=$(date "+%Y-%m-%d-%H-%M-%S")
echo $current_timestamp
final_file=$tgt_dir/scripts-backup-$current_timestamp.tgz
echo $final_file

#Vi backupdata.sh
#./backupdata.sh
tar czf $final_file -C $src_dir

echo "Backup Completed"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699476177583/9261afab-110f-4c4a-9bd1-926ad6224c1a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699476239547/dc4fd72e-16df-49da-b599-fd75bfca2551.png align="center")

Function Creation :

```bash
#!bin/bash

function create_backup {
                  src_dir=/home/ubuntu/7DayScript
                  tgt_dir=/home/ubuntu/backups
                  current_timestamp=$(date "+%Y-%m-%d-%H-%M-%S")
                  final_file=$tgt_dir/scripts-backup-$current_timestamp.tgz

}

echo "Starting Backup Process .. "
create_backup
echo " Backup Completed....."
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699477386448/0563b3a9-3d4c-4f47-b3c1-17e65d553da5.png align="center")

```bash
vi backupdata-func.sh
bash backupdata-func.sh

ls -la /home/ubuntu/backups
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699477479831/a1c18c3a-5bdc-4813-888c-ce996731e715.png align="center")

To create a tar archive file :

```bash
tar -cvf /mnt/backup.tar /var

/mnt/backup.tar: This is the path and name of the archive file 
                 that will be created. In this case, the archive file 
                 is named "backup.tar" and is located in the "/mnt" directory.

/var: This is the directory or list of files and directories that
      you want to include in the archive. In this case, it's the "/var" directory.
      The tar command will recursively archive the contents of the "/var" directory
      and include them in the "backup.tar" archive file.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701879754840/699dad60-14c6-451a-b493-8f754a45e9ce.png align="center")

To show file size in human-readable format:

```bash
du -sh /var
du -sh /mnt/backup.tar
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701879873653/492c94f5-b7c7-4b78-a56b-272ef8939d47.png align="center")

To extract a tar file on the default location(the current working directory):

```bash
sudo tar -xvf /mnt/New.tar

sudo tar -xvf New.tar 

# -x - Extract files from an archive.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702201814553/a156bf3d-e18d-471c-aefb-7a98b75fdb2a.png align="center")

To extract a tar file on the specific Location:

```bash
#if you are in same folder where Tar File 
tar -xvf New.tar -C /home/ubuntu

#if you are in different folder
tar -xvf /mnt/backuo.tar -C /home/ubuntu
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702202304777/43b111ae-03dd-47d3-9f69-bc92ba20c4f1.png align="center")

To create a tar archive file with compress in size (gzip):

```bash
sudo tar -cvzf /mnt/New1.tar.gz Ankit
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702207293822/e4d69703-feb7-4846-814e-8a8984f77ffe.png align="center")

To create a tar archive file with compress in size (gzip):

```bash
sudo tar -xvzf /mnt/New1.tar.gz
sudo tar -xvzf /mnt/New1.tar.gz -C /mnt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702207619006/c487486b-7dfa-4c91-a6e9-36daa5802e92.png align="center")

To create a tar archive file with compress in size (bzip/bz2)

```bash
sudo apt-get update
sudo apt-get install bzip2

sudo tar -cvjf /mnt/New2.tar.bz2 Ankit
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702207935646/2fe2f466-7a99-4d2a-b591-519f374ed8d2.png align="center")

To create a tar archive file with compress in size ((bzip/bz2)

```bash
sudo tar -xvjf /mnt/New2.tar.bz2

sudo tar -xvjf /mnt/New2.tar.bz2 -C /mnt/
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702208051602/98e4a525-d335-4b08-8fcf-49d38738ee91.png align="center")

To create a tar archive file with compress in size (xz) :

```bash
sudo tar -cvjf Ankit.tar.xz Ankit
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702213740227/76f68e58-0305-464e-839b-c6bd895ec311.png align="center")

To create a tar archive file with compress in size (xz) :

```bash
sudo tar -xvjf Ankit.tar.xz
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702213858232/b702f4f0-c64d-4e41-8b5c-7a5611d5be4b.png align="center")

### Job Automation:

**Job automation in Linux refers to the practice of using tools, scripts, and processes to <mark>automate repetitive and routine tasks</mark> within a Linux environment. The goal is to <mark>streamline operations, reduce manual intervention, minimize errors, and improve overall system efficiency.</mark>**

Types of Job Automation:

1. at -
    
    * "at" is a command-line tool for scheduling jobs to run at specific times.
        
    * It is typically used to schedule jobs that need to <mark>run once or at a specific time and date</mark>.
        
    * For example, you could use "at" to schedule a job to run every day at 5:00 PM.
        
    * To use "at", you would type the following command:
        
        ```bash
        at time job
        ```
        
    * Where "time" is the time you want the job to run, and "job" is the command you want to run.
        
    * For example, to schedule a job to run every day at 5:00 PM, you would type the following command:
        
        ```bash
        at 5:00 PM every day job
        ```
        
2. crontab-
    
    * Crontab is a file that contains a list of jobs to be run at specific times.
        
    * It is typically used to schedule jobs that need to <mark>run on a regular basis,</mark> <mark>such as daily, weekly, or monthly</mark>.
        
    * To use crontab, you would type the following command:
        
        ```bash
        crontab -e
        ```
        
        * This will open the crontab file in a text editor.
            
        * You can then add lines to the file to schedule jobs.
            
    * Each line in the crontab file contains six fields:
        
        ```bash
        1. Minute 
        2. Hour 
        3. Day of month
        4. Month 
        5. Day of week 
        6. Command
        ```
        
        * For example, to schedule a job to run every day at 5:00 PM, you would add the following line to the crontab file:
            
            ```bash
            0 17 * * * job
            ```
            
            * This line tells the cron to run the job "job" at the 0th minute of the 5th hour of every day of the month.
                

| **Feature** | **At** | **Crontab** |
| --- | --- | --- |
| Use case | Scheduling jobs to run once or at a specific time and date | Scheduling jobs to run on a regular basis |
| Syntax | at time job | 0 5 \* job |
| Flexibility | Less flexible | More flexible |

Creating a cronjob so we can automate a backup process to take backup after a certain interval time.

A crontab file is where you write the automation code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699477749357/e63a56e7-c39d-4693-ba06-64087a2423c3.png align="center")

You can visit this site for cron schedule - [https://crontab.guru/](https://crontab.guru/)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699478054052/f7e88f88-0100-41be-8701-2681b11a0639.png align="center")

At every 1 minute

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699478259565/017323fd-46a0-4e9b-a80f-f98e8908750c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699478563184/fc181c29-671a-488b-8ed4-92e08aed0150.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699478799977/c7a6ac58-8b5c-4c6f-8777-43453e9e1e94.png align="center")

**<mark>How to stop cronjob?</mark>**

Ans: remove the cronjob in crontab.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699478925202/6039e5c5-6263-421e-8a1d-226af002e603.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699478972033/54fbad21-a994-449c-9a6f-8e2b9c1d6089.png align="center")

To a set job with "at" command:

Before entering at command first, check your server date and time.

```bash
#date
at 14:16
echo "Hello" > Hello.txt 
# ctrl+d (write and quit)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702217843153/fdbb080d-7d9f-4623-a8da-7697849e6365.png align="center")

To show pending a job:

```bash
atq
```

if the job is executed then no output is shown.

To remove a job:

```bash
atrm 7 8 9
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702217976327/387b67df-6c5a-4a20-a16d-46b9cbbc87fa.png align="center")

To restrict users from accessing "at" :

```bash
vim /etc/at.deny
Ankit  (add here user name)
:wq (write&quit)
```

To start crond service:

The `crond` service is commonly used on systems that use the SysV init system. However, on Ubuntu, the default init system is systemd, and the cron service is managed by the `cron` service, not `crond`.

To start the cron service on Ubuntu using systemd, you can use the following command:

```bash
sudo systemctl start cron
```

To enable crond service (Permanent on)

```bash
sudo systemctl enable cron
```

For set cron jobs :

```bash
crontab -e

#If you want to edit the crontab for a specific user, you can use:
crontab -u username -e
# Replace username with the actual username.
```

![](https://miro.medium.com/v2/resize:fit:1005/1*ukNvgqV-HTHTebPHZMFNgg.png align="center")

To show cron jobs of the current user

```bash
crontab -l
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702218467819/80c74a90-cda9-4137-8aad-354a1bf98bca.png align="center")

To remove cron jobs

```bash
crontab -r
```

or, go to the crontab file and remove the job lines

```bash
#crontab -e
```

To show the cron job, other users :

The command `crontab -u shub -l` is used to list the cron jobs for a specific user, in this case, the user with the username "shub". When you run this command, it will display the current user's (in this case, "shub") cron jobs.

```bash
crontab -u ubuntu -l
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702218610169/071f0af5-5a5a-4d9e-9621-e7c44b87d3ea.png align="center")

To restrict users from cron service:

```bash
vim /etc/cron.deny
```

If the `/etc/cron.deny` and `/etc/cron.allow` files don't exist, and you want to restrict access to the `cron` service, there's another way to achieve this on systems using the `pam` module.

You can use the `/etc/security/access.conf` file to control access to various services, including `cron`.

```bash
sudo nano /etc/security/access.conf
```

### ACL(Access Control List):

The `getfacl` and `setfacl` commands in Linux are used for working with Access Control Lists (ACLs) on files and directories. ACLs provide a more fine-grained control over file permissions than traditional Unix permissions.

### `getfacl` **Command:**

The `getfacl` command is used to display the ACLs of a file or directory.

```bash
getfacl Hello.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702219031607/8205f5d5-b4e7-4e60-932f-2a44f90c4f5f.png align="center")

The output will show the ACL entries for the specified file or directory.

### `setfacl` **Command:**

The `setfacl` command is used to set or modify the ACLs of a file or directory.

```bash
setfacl options acl_specification filename

setfacl -m u:username:rw- testme.sh 
```

This command adds read and write permissions for the specified user (`username`) to the ACL of the [`testme.sh`](http://testme.sh) file.

Here are some common options for `setfacl`:

* `-m`: Modify the ACL. You can use this option to add or modify ACL entries.
    
* `-x`: Remove specific ACL entries.
    
* `-b`: Remove all ACL entries, essentially setting the ACL to default.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699479633562/5bdd3dcc-8d3c-4a79-8ce1-d44b63968523.png align="center")

\*\*Note: Day 5 GitHub Task

* **Refer to Task5 :** [https://github.com/LondheShubham153/90DaysOfDevOps/tree/master/2023/day05](https://github.com/LondheShubham153/90DaysOfDevOps/tree/master/2023/day05)
    
    Code Solution: Still Working
    

---

🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏

* I sincerely hope this blog helps you save valuable time, allowing you to cherish moments with your loved ones. Keep smiling and spread the love!😄😄. Thank you for reading.🤝🤝
    
* Your support means the world to me. If you’ve found this blog enjoyable and informative, Please take a moment to hit that cheerful Like button and share it with others. Thank you for being a part of this journey!🙏🙏.
    
    ..........................................................................................................................................
    
* **Follow/Connect Me:** [**LinkedIn**](https://www.linkedin.com/in/ankit-gupta2/) **|** [**Medium**](https://medium.com/@ankitgupta_974) **|** [**GitHub**](https://github.com/ankitAMD)**|**[**Hashnode**](https://hashnode.com/@NinjaAnkit)**|**[**Linktree**](https://linktr.ee/ninjaankit)**🔔🔔🔔🔔.**
    
* Please Support Me through **“**[**Buymeacoffee**](https://www.buymeacoffee.com/AnkitGupta1) **”** ☕️.
    
    ..........................................................................................................................................
    
* **<mark>Below are the Links to a series of Detailed | Step by Step of WordPress Website Hosting on AWS Lightsail :</mark>**
    
    🚀 **Part 1:** [How to host a WordPress website on AWS LightSail.](https://aws.plainenglish.io/how-to-host-a-wordpress-website-on-aws-lightsail-8808b70f7f7c)
    
    🔍 **Part 2:** [Find Login Credentials of the Dashboard of WordPress AWS Lighstail.](https://www.clickaws.com/find-wordpress-password-in-aws-lightsail/)
    
    🌐 **Part 3:** [Setting up a Lightsail Static IP Address from Dynamic IP Address.](https://medium.com/@ankitgupta_974/setting-up-a-lightsail-static-ip-address-from-dynamic-ip-address-4a0628f63c52)
    
    📌 **Part 3.1:** [Dynamic IP address of Instances in AWS Lightsail.](https://medium.com/nerd-for-tech/the-dynamic-ip-address-of-instances-in-aws-lightsail-b3dfb1562171)
    
    🌐 **Part 4:** [How to Register a Domain Name with Amazon Web Service | Register a Domain Name using AWS Route53.](https://aws.plainenglish.io/how-to-register-a-domain-name-with-amazon-80a1bf809859)
    
    🔗 **Part 4.1:** [Connect a Route53 Registered Domain to AWS Lightsail Instance.](https://aws.plainenglish.io/connect-a-route53-registered-domain-to-aws-lightsail-instance-website-bdd2d57a927c)
    
    🛡️ **Part 5:** [Set up a Free SSL Certificate on WordPress AWS Lightsail.](https://www.clickaws.com/how-to-setup-or-enable-free-ssl-certificate-on-your-wordpress-aws-lightsail-instance/)
    
    ..........................................................................................................................................
    
    🙏 ***Thank you for being a part of our community!***
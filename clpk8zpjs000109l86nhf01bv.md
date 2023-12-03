---
title: "Day 5-DevOps"
seoTitle: "Linux Advanced and Shell Scripting"
seoDescription: "Unlock the power of Linux with advanced commands and shell scripting. Elevate your DevOps game with essential skills and efficient techniques."
datePublished: Wed Nov 29 2023 20:57:10 GMT+0000 (Coordinated Universal Time)
cuid: clpk8zpjs000109l86nhf01bv
slug: day-5-devops
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/Im7lZjxeLhg/upload/cfa1569564b0c3c8abc0d921b9756902.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1701087485139/acc44239-12eb-4b37-9405-55b2a05178c1.png
tags: linux, aws, devops, terraform, shell-scripting

---

Hello everyone, I'm on Day 6 of my DevOps learning journey, starting from Day 0. Today, I'll be discussing advanced Linux Advanced commands and Shell Scripting that are essential for DevOps and Cloud Computing tasks. Let's explore! Additionally, I'll be providing the answers to the Day-4 task in the DevOps challenge.

Topics We covered:

1. How to see and modify Logs
    
2. grep, awk, find command
    
3. Shell Script
    
4. Activities and Task
    

## What is Kernel?

The kernel is the core component of an operating system that acts as a bridge between the computer's hardware and software. It is responsible for managing system resources, such as memory and CPU, and providing essential services for the functioning of other software components. The kernel handles tasks like process scheduling, memory management, device communication, and system calls. It plays a crucial role in ensuring that various software applications can run on a computer by facilitating communication with the underlying hardware.

## What is Shell?

A shell is a unique user program that serves as an interface for users to interact with operating system services. It takes commands in a human-readable format from users and translates them into instructions understandable by the kernel. Acting as a command language interpreter, the shell executes commands received from input devices like keyboards or files. It initiates when a user logs in or opens a terminal.

## What is Linux Shell Scripting?

A shell script is like a computer program that you run using a Linux shell, which is a command-line interpreter. Think of it as a set of instructions written in a language that the shell understands. These scripts, often seen as scripting languages, can do things like handling files, running programs, and displaying text.

**<mark>Explain in your own words and examples, what is Shell Scripting for DevOps.</mark>**

Shell scripting for DevOps involves using scripting languages, such as Bash, to automate tasks in the software development and deployment process. It's like creating a series of instructions that a computer can execute automatically.

For example, instead of manually configuring servers, deploying applications, or managing infrastructure, you write scripts that perform these tasks. These scripts can be triggered automatically or run on-demand, saving time and reducing the chance of errors. Shell scripting is a powerful tool in the DevOps toolkit, promoting efficiency, consistency, and automation across various stages of software development and deployment.

### **<mark>What is </mark>** `#!/bin/bash?` **<mark>can we write </mark>** `#!/bin/sh` **<mark>as well?</mark>**

Yes, `#!/bin/bash` is known as a shebang or hashbang. It is placed at the beginning of a script in Linux and Unix-like operating systems to specify the interpreter that should be used to execute the script. In this case, it indicates that the Bash shell should be used.

You can also use `#!/bin/sh` as a shebang, which specifies the system's default shell. However, keep in mind that different systems may have different default shells. Using `#!/bin/bash` explicitly ensures that the Bash shell is used, providing consistency across different environments.

### **<mark>Regular Expression</mark>**

Regular expressions are special characters that help search data, matching complex patterns.

### **<mark>GREP (Global Regular Expression Print) Command</mark>**

`grep` is a command-line utility in Unix and Linux operating systems used for searching patterns in files or streams of text.

* **Basic Usage:**
    
    ```bash
    grep pattern file
    ```
    
    Searches for the specified pattern in the given file.
    
* **Options:**
    
    * `-i`: Case-insensitive search.
        
    * `-r` or `-R`: Recursively search directories.
        
    * `-n`: Show line numbers.
        
    * `-v`: Invert match, i.e., show non-matching lines.
        
    * `-E`: Interpret the pattern as an extended regular expression (ERE).
        
    * `-A`, `-B`, `-C`: Show lines After, Before, or Around the match.
        
* **Examples:**
    
    ```bash
    grep "error" logfile.txt    # Search for lines containing "error" in logfile.txt
    grep -i "warning" *.log     # Case-insensitive search for "warning" in all .log files
    grep -rn "pattern" /path    # Recursively search for pattern in /path, showing line numbers
    ```
    
* **Common Usage:**
    
    * Checking log files for errors or warnings.
        
    * Searching for specific content in source code.
        
    * Extracting information from command outputs.
        

`grep` is a versatile tool for pattern matching, making it a fundamental component in command-line text processing.

**<mark>Search a word(string in File)</mark> :**

```bash
grep root /etc/passwd
grep Ankit /etc/passwd
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196110622/ee3a264e-d1b5-4e3c-9327-9756035873bd.png align="center")

**<mark>Search a string in multiple Files</mark> :**

```bash
grep root /etc/passwd /etc/group
grep Ankit /etc/passwd /etc/group
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196259060/8ff8d7ba-7201-47c6-a642-da751ec69a41.png align="center")

**<mark>Search a string insensitive in file</mark>** :

```bash
grep -i Root /etc/passwd
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196354841/010e2f81-2a5c-4fca-95a9-171c6a08a2f2.png align="center")

**<mark>Search a string in all files recursively</mark> :**

```bash
sudo grep -r root /
sudo grep -r Ankit /
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196393116/85f6d4b2-9819-48a0-840b-a8ad7ff64a1c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196497591/c811ee3d-1583-43ab-a1b8-a438ca82b732.png align="center")

**<mark>Inverting the string match</mark> :**

```bash
grep -v root /etc/passwd

# -v: This option inverts the match, meaning it selects all lines 
#     that do not match the specified pattern.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196592288/ee24cf53-ce44-4554-be5a-7594a0d28de0.png align="center")

**<mark>Displaying the string match total line no</mark> :**

```bash
grep -c root /etc/passwd

#-c: This option is used to count the number of lines 
#    that match the specified pattern.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196735617/ea3812ff-4eec-4422-b8a2-b6d3a4aa5f90.png align="center")

**<mark>Display all file names that match the string</mark> :**

```bash
grep -l root /etc/passwd /etc/shadow

# -l: This option is used to display only the names of files that contain
#      the specified pattern, not the actual matching lines.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196950164/e51ea843-a875-449c-b93e-60b0c4568ed6.png align="center")

**<mark>Display file names that do not contain the string</mark> :**

```bash
grep -L root /etc/passwd /etc/shadow
# -L: This option is used to display the names of files that do not contain the specified pattern.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701196980858/892d0ab5-631b-42c5-ac94-d6d77ed1c220.png align="center")

**<mark>Displaying the string match line with the number</mark> :**

```bash
grep -n root /etc/passwd

# When you run grep -n root /etc/passwd, it will output lines containing 
# the pattern "root" in the /etc/passwd file, and each line will be prefixed
# with the line number where the match is found. This can be helpful
# for quickly locating information within a file.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701197170364/84fa35e2-90ba-460c-b235-46b07e5d0fea.png align="center")

**<mark>Display the lines that start with a string :</mark>**

```bash
grep ^root /etc/passwd

# This is the regular expression being used for the search. 
# The caret (^) is a metacharacter that anchors the search pattern 
# to the beginning of a line. So, ^root looks for lines that start 
# with the string "root."
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701197705041/66fb349d-ec91-4d06-828c-8ca43cd59630.png align="center")

**<mark>Display the lines that end with a string :</mark>**

```bash
grep /bin/bash$ /etc/passwd

# This is the regular expression being used for the search.
# /bin/bash specifies the shell, and the $ is a metacharacter 
# that anchors the search pattern to the end of a line. 
# So, /bin/bash$ looks for lines where the shell is set to /bin/bash 
# at the end of the line.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701197890479/9a8f7867-b8a4-40e2-bf02-aff2143c6ae9.png align="center")

**<mark>Search and redirect output in a new file:</mark>**

```bash
grep root /etc/passwd > /home/ubuntu/find.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701198149471/26fab1ca-f7ff-46c3-a3b5-244e9993e883.png align="center")

Breaking down the components:

* `grep root /etc/passwd`: Searches for lines in the `/etc/passwd` file that contain the word "root."
    
* `>`: Redirects the output of the `grep` command to a file.
    
* `/home/ubuntu/find.txt`: Specifies the file path where the output will be saved. In this case, it's the `find.txt` file located in the `/home/ubuntu` directory.
    

After running this command, the file `/home/ubuntu/find.txt` will contain the lines from `/etc/passwd` that includes the word "root."

### **<mark>Find Command</mark>**

The Linux Find command is one of the most important and much-used commands in Linux Systems.

The "Find" command is used to search and locate the list of files and directories based on conditions you specify for files that match the arguments.

Find can be used in a variety of conditions like you can find files by permissions, users, groups, file type, data, size, and other possible criteria.

**<mark>Find Files under the Home directory</mark> :**

find /home -name shub.txt

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701202425166/b222c7be-cc67-47cd-a374-180bfea1f963.png align="center")

**<mark>Find Files with suid permission</mark> :**

```bash
find / -perm 4755
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701270988298/e8aae38a-554e-4ab3-a7c0-9fb14443faff.png align="center")

The command `find / -perm 4755` searches for files with the setuid bit set. The setuid bit is a special permission that allows a user to execute a program with the permissions of its owner.

Breaking down the components:

* `find`: Initiates the find command.
    
* `/`: Specifies the starting directory for the search (in this case, the root directory).
    
* `-perm 4755`: Specifies the permissions to search for. In this context, it looks for files with the setuid bit set (4 for read, 2 for write, and 1 for execute, totaling 4 + 2 + 1 = 7). The number 4755 represents the octal notation for the setuid permission.
    

Running this command will list files with the setuid bit set, typically indicating executable files that run with the permissions of their owner.

**<mark>Find Files with guid permission</mark> :**

```bash
find / -perm 2644
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271038091/da7c7139-af4e-47a0-bd6f-2426cf9334f7.png align="center")

The command `find / -perm 2644` searches for files with specific permissions. In this case, it looks for files with the octal permission 2644.

Breaking down the components:

* `find`: Initiates the find command.
    
* `/`: Specifies the starting directory for the search (in this case, the root directory).
    
* `-perm 2644`: Specifies the permissions to search for. In octal notation, 2644 represents the permission mode. The leading "2" indicates the setgid bit, "6" indicates read and write permission for the file owner, and "4" indicates read permission for the group.
    

Running this command will list files with the specified permissions.

**<mark>Find Files with sticky bit permission:</mark>**

```bash
find / -perm 1755
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271089068/f0df35da-83b5-4ed3-a339-ee67444a767d.png align="center")

The command `find / -perm 1755` searches for files with specific permissions. In this case, it looks for files with the octal permission 1755.

Breaking down the components:

* `find`: Initiates the find command.
    
* `/`: Specifies the starting directory for the search (in this case, the root directory).
    
* `-perm 1755`: Specifies the permissions to search for. In octal notation, 1755 represents the permission mode. The leading "1" indicates the sticky bit, and "755" indicates read, write, and execute permission for the file owner and read and execute permission for the group and others.
    

Running this command will list files with the specified permissions. The setuid (suid) bit is often set in executables to allow them to run with the permissions of the file owner.

**<mark>Using Find Command based on users:</mark>**

```bash
find / -user root
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271267674/37f6f980-cf8c-4845-baf3-cc400bac26f9.png align="center")

The command `find / -user root` searches for files owned by the user "root" starting from the root directory ("/").

Breaking down the components:

* `find`: Initiates the find command.
    
* `/`: Specifies the starting directory for the search (in this case, the root directory).
    
* `-user root`: Specifies the user ownership to search for. In this case, it looks for files owned by the user "root."
    

Running this command will list files and directories owned by the root user within the specified directory and its subdirectories.

**<mark>Using Find Command based on groups:</mark>**

sudo find / -group Ankit

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271320529/fd0d9b62-14b7-4155-bfa3-5e1721a2ca8d.png align="center")

The command `find / -group shubgrp` searches for files that belong to the group "shubgrp" starting from the root directory ("/").

Breaking down the components:

* `find`: Initiates the find command.
    
* `/`: Specifies the starting directory for the search (in this case, the root directory).
    
* `-group shubgrp`: Specifies the group ownership to search for. In this case, it looks for files that belong to the group "shubgrp."
    

Running this command will list files and directories that have the specified group ownership within the specified directory and its subdirectories.

**<mark>Search the file with less than 10 MB in a folder</mark>**:

```bash
find /tmp -size -10M
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271364202/ede733c2-bafe-4a1d-843c-6053adf6a088.png align="center")

The command `find /tmp -size -10M` searches for files in the "/tmp" directory that are smaller than 10 megabytes.

Breaking down the components:

* `find`: Initiates the find command.
    
* `/tmp`: Specifies the starting directory for the search (in this case, the "/tmp" directory).
    
* `-size -10M`: Specifies the size criterion. Files smaller than 10 megabytes will match.
    

Running this command will list files within the "/tmp" directory that are smaller than 10 megabytes.

**<mark>Search the file with more than 10MB in a folder</mark>**:

```bash
find /tmp -size +10M
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271431154/39592185-be82-4829-b573-adbb54c4dc9a.png align="center")

The command `find /tmp -size +10M` searches for files in the "/tmp" directory that are larger than 10 megabytes.

Breaking down the components:

* `find`: Initiates the find command.
    
* `/tmp`: Specifies the starting directory for the search (in this case, the "/tmp" directory).
    
* `-size +10M`: Specifies the size criterion. Files larger than 10 megabytes will match.
    

Running this command will list files within the "/tmp" directory that are larger than 10 megabytes.

**<mark>Head:</mark>**

Display top specific no line of the line

head -n 15 /etc/passwd

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271513838/e2b4fb51-b845-4bab-8664-0951778390b9.png align="center")

**<mark>Tail :</mark>**

Display bottom specific no line of the line

```bash
tail -n 15 /etc/passwd
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701271548167/2f54aab3-d745-4beb-9c6a-25c092695ed2.png align="center")

```bash
find ~/ -name application.log

find ~/ -name *.log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698859382631/22cb91e3-41d2-44f9-9e53-9b29380202e7.png align="center")

```bash
find ~/ -user ubuntu
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698859474910/de466119-cd62-46b7-a4b8-974b8a48fdac.png align="center")

```bash
find ~/ -group DevOps
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698859856176/4c6efecb-e18d-46db-8f98-90f5b6b0abb5.png align="center")

### **Log Files:**

We created a "log" directory and then created an "application.logs" file in that directory.

I searched on Google for "sample log file" and the copy pasted that log file into an "application.logs" for practicing.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701277589287/0069bb21-9e11-4fb5-ba1f-c2e99850014e.png align="center")

```bash
grep -i trace application.logs
grep -i trace application.logs > trace_only_for_qa.log
cat trace_only_for_qa.log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701277971177/ff2a98a5-8bbe-4190-8a59-ee3fdefad157.png align="center")

**<mark>AWK</mark>** is a powerful programming language used for text processing and data extraction. It is particularly useful for working with structured text files, such as those containing columns of data. Here's a detailed overview of the AWK command:

### Basic Syntax:

```bash
awk 'pattern { action }' filename
```

* **pattern**: Specifies a condition or pattern to match lines.
    
* **action**: Specifies the action to be performed for lines that match the pattern.
    
* **filename**: Specifies the input file.
    

### Key Concepts:

1. **Fields:**
    
    * By default, AWK treats each whitespace-separated word as a field.
        
    * Fields are accessed using `$1`, `$2`, ..., `$NF` (where `NF` is the number of fields).
        
2. **Patterns and Actions:**
    
    * Patterns are conditions that, when true, trigger an action.
        
    * If no pattern is specified, the action is applied to all lines.
        
    * Actions are enclosed in curly braces `{}`.
        
3. **Built-in Variables:**
    
    * `NR`: Number of records (lines) processed.
        
    * `NF`: Number of fields in the current line.
        
    * `FS`: Field Separator (default is whitespace).
        
    * `OFS`: Output Field Separator.
        
4. **Operators:**
    
    * `==`, `!=`: Equality and inequality.
        
    * `~`, `!~`: Match and not match (regular expressions).
        

### Examples:

1. **Print Specific Columns:**
    
    ```bash
    awk '{print $1, $3}' filename
    ```
    
2. **Conditional Print:**
    
    ```bash
    awk '$2 > 50 {print $1, $2}' filename
    ```
    
3. **Calculate and Print Sum:**
    
    ```bash
    awk '{sum += $3} END {print "Total:", sum}' filename
    ```
    
4. **Using Patterns:**
    
    ```bash
    awk '/pattern/ {print $0}' filename
    ```
    
5. **Custom Field Separator:**
    
    ```bash
    awk -F',' '{print $1, $2}' filename.csv
    ```
    
6. **Using Variables:**
    
    ```bash
    awk '{total += $NF} END {print "Average:", total/NR}' filename
    ```
    
7. **Built-in Functions:**
    
    ```bash
    awk '{print toupper($1)}' filename
    ```
    

### AWK in Shell Scripts:

AWK commands can also be used within shell scripts for more complex tasks. The versatility and simplicity of AWK make it a powerful tool for text processing and data manipulation in the command line.

```bash
awk '{print $1,$2,$3}' trace_only_for_qa.log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701278119244/c011ffae-ffe9-4903-ab16-86188d3a3eb7.png align="center")

```bash
awk '{print $1,$2,$3}' trace_only_for_qa.log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701278202126/9fa96657-0ab6-4354-8463-c0296ce45594.png align="center")

```bash
awk '{print NR $1,$2,$6}' trace_only_for_qa.log

#Also print the Number of Line
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701278254276/391b62c0-d87d-4daa-a033-1a367628e350.png align="center")

```bash
awk '{print NR $1,$2,$6}' trace_only_for_qa.log | head -3
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701278365877/fed0b449-f0de-4abe-9e1e-dcc2914f28e6.png align="center")

```bash
 awk 'NR>10 && NR<30 {print NR, $1, $2, $6}' application2.log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701279227222/da3c1826-8f9a-4d8f-b948-1cb466687288.png align="center")

```bash
awk /TRACE/  application.logs
awk /EVENT/  application.logs
awk /INFO/  application.logs
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701279824949/0af42959-179a-45fd-b562-de6d6a7001e5.png align="center")

```bash
 awk '/INFO/  {print NR,$1,$2,$4}' application.logs 
 awk '/INFO/  {print NR,$1,$2,$4}' application.logs | head -n 10
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701280131262/62f1ccf8-0edd-4bb0-bf42-78601c28bc64.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701280067378/b969898c-cefc-4af0-87b8-e7ea115d05c5.png align="left")

```bash
awk 'NR>20 && NR<40 && /INFO/  {print NR,$1,$2,$4}' application.logs
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701280235133/3c4f68b3-e567-48c6-8b37-4bbe635e9f82.png align="center")

```bash
 awk 'NR>20 && NR<40 && /INFO/  {print NR,$1,$2,$4}' application.logs > info_qa_team.log
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701281409386/8bbd3de1-6ca0-4762-bad9-43a0d594856d.png align="center")

```bash
awk '$2>"08:52:00" && $2<"08:53:00" && /INFO/  {print NR,$1,$2,$4}' application.logs
Sort using time
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701281872426/2adee620-57e6-47fc-8b95-1292b811790d.png align="center")

A Shell Script is a set of commands for the computer to follow.

.sh is the file ending that tells the computer it's a script.

Before running the script, make it executable by changing its permission.

#!/bin/bash - This is a code that says, "Hey computer, get ready for a bash script!"

```bash
vi makedirectory.sh
# content 
#!/bin/bash
echo "What is your Folder Name ? "
read foldername
mkdir $foldername
echo "$foldername is created Successfully"
chmod 700 makedirectory.sh
#end
bash makedirectory.sh

or

./ makedirectory.sh
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701285938025/e0cb2337-7eab-4310-9e5a-2295b23d0230.png align="center")

```bash
#Showargument.sh Script

#!/bin/bash
echo "first argument $1"

echo "Second argument $2"

echo "All argument $@"

#bash Showargument.sh Hello Linux This
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701286710673/38098701-e377-47e6-a8f2-546df5c6804c.png align="center")

```bash
#Script for installing any package

#!/bin/bash
echo "installing $1"
sudo apt update
sudo apt-get install $1

# bash installer.sh nginx
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701287041829/d6a7c22d-6b3b-40d7-959b-d22e7c2b8f05.png align="center")

```bash
#Script for installing any package withot asking yes no

#!/bin/bash
echo "installing $1"
sudo apt update -y
sudo apt-get install $1 -y

# bash installer.sh nginx
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701287289198/16064f24-91c4-4108-b2f2-74bec930c8e7.png align="center")

In many cases, Bash-specific features are used in scripts, so specifying `#!/bin/bash` is a common practice to avoid any potential compatibility issues.

* Write a Shell Script which prints `I will complete #90DaysOofDevOps challenge`
    

```bash
#!/bin/bash
echo "I will complete #90DaysOofDevOps challenge"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701289444671/539c7d94-4c61-43d8-b32d-205bde88db0e.png align="center")

* Write a Shell Script to take user input, input from arguments, and print the variables.
    

```bash
#!/bin/bash
echo "Enter Your Name"
read YourName
echo "First Argument $1"
echo "your name is $YourName"
                              
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701289842359/17b8e80f-a42e-45cf-89a3-06332ec09b53.png align="center")

* Write an Example of If else in Shell Scripting by comparing 2 numbers
    
    ```bash
    #!/bin/bash
    
    echo "Enter First Number: $1"
    read num1
    
    echo "Enter Second Number: $2"
    read num2
    
    if [ $num1 -gt $num2 ]; then
        echo "$num1 is greater than $num2"
    elif [ $num1 -eq $num2 ]; then
        echo "$num1 is equal to $num2"
    else
        echo "$num1 is smaller than $num2"
    fi
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701291063381/7bb36425-84b6-4b8a-aca9-cf5b570b2124.png align="center")
    
    \*\*Note: Day 4 GitHub Task - **Completed** (see above response).
    
* **Refer to Task4:**
    
    [https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day04/README.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day04/README.md)
    
    ---
    
    🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏🙏
    
    I sincerely hope this blog helps you save valuable time, allowing you to cherish moments with your loved ones. Keep smiling and spread the love!😄😄. Thank you for reading.🤝🤝
    
    Your support means the world to me. If you’ve found this blog enjoyable and informative, Please take a moment to hit that cheerful Like button and share it with others. Thank you for being a part of this journey!🙏🙏.
    
* **Follow/Connect Me:** [**LinkedIn**](https://www.linkedin.com/in/ankit-gupta2/) **|** [**Medium**](https://medium.com/@ankitgupta_974) **|** [**GitHub**](https://github.com/ankitAMD)**|**[**Hashnode**](https://hashnode.com/@NinjaAnkit)**|**[**Linktree**](https://linktr.ee/ninjaankit)**🔔🔔🔔🔔.**
    
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
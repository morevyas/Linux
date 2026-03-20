# Linux CMD #

## Check current directory
shows the where you are currently located in the filesystem.
pwd **Present working Directory**.
It is tell you exactly where you are in the filesystem.

	pwd

## list files and folders
It is used to shows the files and directories inside the folder

	ls

check the detailed information **(permissions, size, date)**

	ls -l
output ex.

	-rw-r--r-- 1 user user 245 Mar  5 12:30 file.txt
	
check the hidden files
hidden file start with **(.)**
	ls -a

## Change the directory ##
used to move from **one directory to another directory**

	cd folder_name

**Go to previous directory**

	cd ..

**Go to the home directory**

	cd ~
**Go to the root directory**

	cd /

## Make directory ##
**make a new directories(folders)**

	mkdir direoctory_name

**make a multiple directories at one time**

	mkdir directory1 directory2 directory3

## Create a file ##
create a new empty file 

	touch file_name

**make a multiple files at one time**

	touch file1 file2 file3


## Copy a file ##
copy a file or directories from one file to another file

	cp source destination


example :

	cp file1.txt backup.txt

**copy file to another directory**

	cp file_name /home/user/Documents

**copy a directory**

	cp -r dir1 dir2
**(-r)** means recursive copy

## Move a file ##
move a file from one directory to another 
also renames the file using the move command

	mv source destination

example : 

	mv file1 Documents/

rename the file

	mv old_name new_name

## Remove the file ##

delete a file 

	rm file_name

delete a directory
**(-r) means recursive delete**

	rm -r folder 

force to delete 

	rm -rf folder

## Managing Users
**Managing users in Linux** means creating, modifying, deleting users and controlling their access, passwords, and permissions.

**Add a new user**

	sudo useradd user-name

create users with home directory

	sudo useradd -m username

**Set password**

	sudo passwd username

### Modify Username

change user-name

	sudo usermod -l newname oldname

Change home directory

	sudo usermod -d /new/home -m username

### Delete Users

Delete user only

	sudo userdel username

Delete user with home directory

	sudo userdel -r username

## Password Management

Change the Password

	passwd username

## Managing Groups
A **group** is a collection of users used a manage permissions collectively, simplify access control, share files securely.

**Create group**

	sudo groupadd groupname
 
 **Add user to group**
 
	sudo usermod -aG groupname username

**Remove user from group**

	sudo gpasswd -d username groupname

**Check Current user**
	
		whoami

### User Management Files

| File  | Purpose |
|----|-----|
| /etc/passwd | User account details
| /etc/shadow | Encrypted passwords |
| /etc/group | Group Details




## Display the file content ##
show the file content in the terminal

	cat file_name


### Print the text ###

print the txt to the terminal.

	echo Hello
 
 output :
		
	Hello


add text to the file

	echo "Hello" > file_name

	
	
## File Permission

Linux file permission commands include **`chmod`** for modifying access rights

### Permission types

 - u -> User
 - g-> Group
 - 0 -> Others


|  Permission    | Symbol |  Value  |
|--------------|------------------|------------|
 | Read         |r        | 4|
 | Write  |   w             | 2|
 | Execute |x               |1  |
 

#### Change  Permissions

	**chmod 755** filename

ex:

	755  {rwx r-x r-x (common for programs)}

execute permission


	chmod +x filename

**view permissions**

	ls -l file


### change the owner of file 

	chown user filename


## Search Command
`find` is a **powerful command-line utility** used to search for files and directories in a directory

	find [path] [options] [expression]

ex:

	find . -name  "file.txt"


### serach types

|  Type     |       Meaning|
|-------------|------------|
| f | file |
|d | directory|
|l | symbolic link  |


## check resource usage

**check resource usage in Linux**, you use different commands for CPU, memory, disk, and processes. Here’s a complete guide with explanations and commands
-   performance tuning
-   troubleshooting slow systems
-   detecting overload or failures


	### CPU Usage Monitoring
show a real-time CPU usage and show a lists processes using CPU

	top


`htop` is **an interactive process viewer** for Linux—basically a more powerful, user-friendly version of `top`

	htop

`mpstat` is a Linux tool used to monitor **CPU usage per processor (core)**. It’s part of the **`sysstat`** package.


	mpstat

### Memory Usage

`free` is a simple Linux command to check **memory (RAM) and swap usage**.

	free
To **check file in sizes - KB/MB/GB**

	free -h

### Disk Usage
Disk usage

	du
	du -sh *

`df` (disk free) is used in Linux to check **disk space usage on filesystems**.

	df

To check in sizes -KB/MB/GB instead of blocks

	df -h
## Networking

**Networking is the process of connecting computers to share data, communicate, access services**

### Types

 - IPV4  **(Public)**   -32 bits 
 - IPV6 **(Private)**  -128 bits  

check the ip address of machine

	ip a
	ip addr
	ip address show
	
### Network Connections

show the active connections and services

	netstat -tulnp

real time bandwidth usage

	iftop

**To check the running time, number of users and load average**

	uptime

show a routing table

	ip r

test the connectivity

	ping ipv4
	ping google.com

### Archive and Compression
Used to **archive multiple files/directories** into one file (optionally compressed).

	tar
	
- c → create
    
-   v → verbose
    
-   f → filename
- x → extract

ex:

	tar -cvf filename.tar file1 file2 dir/
	tar -xvf filename.tar



 Compress **single files only** (not folders)

	gzip file.txt

Decompress

	gunzip file.txt.gz


### For cross platform

like windows or linux sharing

create zip :

	zip filename.zip file1 file2

zip a dir.

	zip -r filename.zip dir/

Extract


	unzip filename.zip


### Help Command
**Shows full documentation for a command.** Manual pages 

	man ls
	man man

Detailed in structure

	info ls
for help 

	help command-name


Shwo the path of file 

	which file-name
ex :

	which python


### Package Management

**Package Management** in Linux is the system used to **install, update, remove, and manage software packages** on your system.
#### Benefits of Package Management

 - Easy Software Installation
 - Automatic Dependency Handling
 - Simple Updates & Upgrades
 - Easy Search & Information


#### Types of Linux Package Systems

**Debian based**
Tools : **apt** , **apt-get** , **dpkg**
Package format : **.deb**

**Red Hat based**
Tools : **yum** , **dnf** , **rpm** 
Package format : **.rpm**

**For Update a package list**

	sudo apt update //Debian-based 
	sudo yum update //Red-hat based

**Upgrade Package**
**-y**  -> give a permission

	sudo apt upgrade -y
	sudo yum upgrade -y
**Install package**

	sudo apt install python3
	sudo yum install python3

## Managing system units

Managing system units this usually refers to **`systemd` units**, which are managed using the `systemctl` command.

	systemctl

### What are System Units
a **unit** is any resource that the system manages a **Services, Mount, Devices, Sockets, Timers**

using ngix example :

**Start**

	sudo systemctl start nginx

**Stop**

	sudo systemctl stop nginx
	

**Restart**

	sudo systemctl restart nginx

**Reload**

	sudo systemctl reload nginx

**Check status**

	systemctl status nginx
		
**List units**

	systemctl list-units --type=service



## Bash history
**Bash history** is a feature in Linux that keeps a record of commands you’ve previously executed in the terminal. It helps you **reuse, search, and manage past commands efficiently**.

 **Check a command History**

	history

**Run a command by number**

	!number 

ex:

	!102
	
**run a last command**

	!!
	
reverse search

	ctrl + r

**Filter with grep**

	history | grep ssh


**Delete a History**

	history -c


### Streams in linux

In Linux, **streams** refer to the flow of data between programs and devices. Every process works with three standard data streams.
**A **stream** is simply a channel for input/output** (data flow)

Linux uses 3 standard streams:

|Stream   |  Description  |    File Description |
|---------|--------------------|--------|
| **stdin** | Standard input |  0 |
| **stdout**| Standard output | 1|
| **stderr** | Standard error | 2|




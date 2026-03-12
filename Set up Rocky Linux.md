# **Rocky Linux**
Rocky Linux is an open-source, enterprise-grade operating system designed as a free, downstream, and bug-for-bug compatible alternative to **Red Hat Enterprise Linux(RHEL**). 
It is primarily used for stable production servers, cloud computing, virtualization, and high-performance computing (HPC), serving as a direct replacement for CentOS,

**A Server** is designed for :

 - Host a Websites
 - Run Databases
 - Manage networks
 - Store files
 - Handle virtualization

## Rocky Linux and others.

|	OS				| Based On 			 | Typical Use 				|
|-----------------|----------------------|----------------------|
|Rocky Linux						| RHEL 					| Enterprise server
|Ubuntu | Debian |Server + Dekstops|
| Debian | Independent | Stability & focused systems|
| Fedora |RHEL | cutting edge developement|




# Set up Rocky Linux in Virtual-Box

## Install Virtual Box
	https://www.virtualbox.org/
	
## Download Rocky Linux Minimal ISO file

	https://rockylinux.org/download

Versions of it **Rocky linux 9 or Rocky Linux 10**

### Download a Virtual box 

#### Open a Virtual-Box ####

### Create a New Virtual Machine ###

point at left upper side to click

	"New"


### >Virtual machine name and operating system ###
**Name:**

	Rocky Linux

**VM Folder**
	
	C:/Users/--/VirtualBox VMs
					or
	D:/New Folder 
	(Make a new folder for virtual machine)
	(set a virtual machine storage path)
	

**ISO Image**

	C:/Downloads/Rocky 9.7 -x86_64-minimal
	
**Type:**

	Linux

**Version:**

Select OS verion 

	Red Hat (64-bit)	


**[ ]Uncheck to the Proceed with Unattended Installation**

**Click Next**

### >Specify virtual hardware ###

**Base memory**
	
	min. 4096

### Numbers of CPUs ###
	min. 2

**Click Next**

### >Specify virtual hard disk ###

**Disk size**

	min. 45.00 GB


**Click Finish**


### Go to "Setting" ###

"Setting->Network->
		Adapter 1 
			Attached to **Bridge Adapter**
			
	Ok



### Click on Start-> arrow ###

**Starting the installation process**

**set the language**

	English

**Installation Type** 

	Rocky Linux
	
**Storage set up**

	Use entire disk
click **Continue**

**Create user**
 **Name**
 
	 Your name
**Server name**

	Rocky Linux

**Username**
	
	enter username

**Password**

	enter passwrod
	

click **continue**

[ take 10-15 minutes]

**when finish, select:**

	 Reboot now



after reboot take a **blank Snapshot of Server** for future  to recover a new server 
 
	 go to the Virtual Box and click on Snapshot 
	 and save as  Blank Snapshot

### log in server ###
**using username and password**


**Update the server**

	sudo apt update

enter passwd:

	
check the **ip address of server** 
type a ip addr for check a server ip address 

	ip addr
ex: 127.0.1.1 is dynamic ipv4

(every time  start the server show the dynamic ipv4,
 set a static ipv4)






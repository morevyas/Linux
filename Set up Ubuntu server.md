# **Ubuntu Server**
Ubuntu Server is a **Linux-based operating system designed specifically for servers**. It is built on the Ubuntu distribution of Linux but **does not include a graphical desktop environment by default (CLI)**, 
Make it lightweight, stable, and optimized for managing **servers and services**.

**A Server** is designed for :

 - Host a Websites
 - Run Databases
 - Manage networks
 - Store files
 - Handle virtualization

## Difference between Ubuntu dekstop and Ubuntu server.

|	Features				| Ubuntu Dekstop 			 | Ubuntu Sever 				|
|-----------------|----------------------|----------------------|
|GUI						| Yes 					| No
|Resource Usage | Higher |Very low|
| Purpose | Personal Computers | Servers|
| Installed packages |Many apps | Minimal|
|Management | GUI + Tools |Terminal/ Remote |
| Remote access | Optional |Usually enabled (SSH) |



# Set up Ubuntu Server in Virtual-Box

## Install Virtual Box
	https://www.virtualbox.org/
	
## Download Ubuntu server ISO file

	https://ubuntu.com/download/server

Versions of it **22.04 LTS or 24.04 LTS**

### Download a Virtual box 

#### Open a Virtual-Box ####

### Create a New Virtual Machine ###

point at left upper side to click

	"New"


### >Virtual machine name and operating system ###
**Name:**

	Ubuntu Server

**VM Folder**
	
	C:/Users/--/VirtualBox VMs
					or
	D:/New Folder 
	(Make a new folder for virtual machine)
	(set a virtual machine storage path)
	

**ISO Image**

	C:/Downloads/Ubuntu-24.04-live-server-amd64.iso
	
**Type:**

	Linux

**Version:**

	Select OS verion 
	Ubuntu (64-bit)


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

	Ubuntu Server
	
**Storage set up**

	Use entire disk
click **Continue**

**Create user**
 **Name**
 
	 Your name
**Server name**

	ubuntu-server

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






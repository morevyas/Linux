# Configure a Server static ip #


**check network interface name**

	ip a
enp0s3 or enp0s8

	ip r

**Go to Netplan configuration Folder**

	cd /etc/netplan

**check list**

	ls 

00-installer-config.yaml

**Edit the file**
		
		sudo nano 00-installer-config.yaml

**then enter the**

	network:
	  version: 2
	  ethernets:
	    enp0s3: # enter your network interface
	      dhcp4: no
	      addresses:
	        - 192.168.*.*/24 # set a static 
	      routes:
	        - to: default
	          via: 192.168.*.* # enter your server ip
	      nameservers:
			     addresses: [8.8.8.8, 8.8.4.4]

 
 **save the file**
 
	 ctrl + 0, enter , ctrl + x

**apply a network configuration**

	sudo netplan apply

**verify static IP**

	ip a



## Access via SSH


	sudo apt install openssh-server

after installation :

	systemctl status ssh

Active: active (running)

If not 

	systemctl start ssh

	systemctl enable ssh

check status 

	systemctl status ssh

 **find server ip**

	ip a


ex . 192.168. * . * .


**Allow SSH in firewall**

	sudo ufw allow ssh

	sudo ufw allow 22


**Connect from windows**

1) Via **windows terminal / CMD**

open terminal/CMD 

enter :

	ssh username@ipv4
	passwd: *****
 


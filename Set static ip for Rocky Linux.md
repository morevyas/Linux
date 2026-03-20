# Configure a Server static ip #


**check network interface name**

	ip a
enp0s3 or enp0s8

	
**Check existing connection**

	nmcli con show
ex :
	
	NAME         UUID                                  TYPE      DEVICE
	System ens33 xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx  ethernet  ens33


## Set static ip
	
	sudo nmcli connection modify "Wired connection 1" \
	ipv4.addresses 192.168.--.--/24 //set a static ip
	ipv4.gateway 192.168.--.--  //machine ip
	ipv4.dns 8.8.8.8 \
	ipv4.method manual

### Restart the connection

	nmcli con down "System ens33"
	nmcli con up "System ens33"

### Restart the Network Manager

	systemctl restart NetworkManager


### Verify the ip 

	ip a

ex :

	192.168.--.--/24

### Editing network configuration file 
 
	/etc/sysconfig/network-scripts/ifcfg-ens**

 

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




**Connect from windows**

1) Via **windows terminal / CMD**

open terminal/CMD 

enter :

	ssh username@ipv4
	passwd: *****
 


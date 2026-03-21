# SCP

**`SCP`(secure copy protocol**) is a command used to securely transfer files between computer over the SSH
It encrypted the data during transfer

**copy a file from local machine to remote server**

	scp /path/to/local/file.txt user@IPV$:/path/to/destination

**copy file from remote server to local machine**

	scp user@ip:/home/user/filename

**copy file between two remote server**

	scp user1@ip:/path/to/filename user2@ip:/path/to/




Ip:10.129.176.78

1: What does the 3-letter acronym FTP stand for?

	File transfer protocol

2: Which port does the FTP service listen on usually?

	21

3: What acronym is used for the secure version of FTP?

	SFTP

4: What is the command we can use to send an ICMP echo request to test our connection to the target?

	ping

5: From your scans, what version is FTP running on the target?

	nmap -sV 10.129.176.78
	Starting Nmap 7.94 ( https://nmap.org ) at 2023-07-15 14:12 EDT
	Nmap scan report for 10.129.176.78
	Host is up (0.16s latency).
	Not shown: 999 closed tcp ports (conn-refused)
	PORT   STATE SERVICE VERSION
	21/tcp open  ftp     vsftpd 3.0.3
	Service Info: OS: Unix
	
	Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
	Nmap done: 1 IP address (1 host up) scanned in 19.75 seconds

	vsftpd 3.0.3

6: From your scans, what OS type is running on the target?

	From nmap we can retrieve this:
	Service Info: OS: Unix
	
7:What is the command we need to run in order to display the 'ftp' client help menu?

	ftp -h

8: What is username that is used over FTP when you want to log in without having an account?

	anonymous

9:What is the response code we get for the FTP message 'Login successful'?

	ftp 10.129.176.78
	Connected to 10.129.176.78.
	220 (vsFTPd 3.0.3)
	Name (10.129.176.78:kali): anonymous
	331 Please specify the password.
	Password: 
	230 Login successful.
	Remote system type is UNIX.
	Using binary mode to transfer files.

10: There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system.

	ls

11: What is the command used to download the file we found on the FTP server?

	get

12: submit root flag

	if we get flag.txt from the ftp connection we get a flag.txt file were is this flag:
	035db21c881520061c53e0536e44f815    
	
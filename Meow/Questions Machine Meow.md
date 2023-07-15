
IP: 10.129.48.41

1: What does the acronym VM stands for?

	Virtual Machine

2:What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.

	Terminal

3: What service do we use to form our VPN connection into HTB labs?

	OpenVpn

4:What is the abbreviated name for a 'tunnel interface' in the output of your VPN boot-up sequence output?

	tun

5:What tool do we use to test our connection to the target with an ICMP echo request?

	Ping

6:What is the name of the most common tool for finding open ports on a target?

	nmap

7:What service do we identify on port 23/tcp during our scans?

	nmap 10.129.48.41     
	Starting Nmap 7.94 ( https://nmap.org ) at 2023-07-15 14:02 EDT
	Nmap scan report for 10.129.48.41
	Host is up (0.19s latency).
	Not shown: 999 closed tcp ports (conn-refused)
	PORT   STATE SERVICE
	23/tcp open  telnet

	Nmap done: 1 IP address (1 host up) scanned in 16.19 seconds

	Telnet

8:What username is able to log into the target over telnet with a blank password?

	Doing a basic google search we found out that the root user can log in without password

9:  Submit root flag:

	Once inside the machine we can ls and check the files that are on the system. We can see a file named flag.txt, if we cat that file we get this flag:
	b40abdfe23665f766f9c61ecba8a4c19

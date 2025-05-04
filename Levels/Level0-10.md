## Level 0
### Look -> ssh
#### solve: 
- just follow the steps on site don't be loser!
password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

## Level 1 -> 2
### Look -> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)
#### solve:
- In Unix/Linux systems, the filename `-` is treated as a special argument in many commands.
```bash
ls -la
cat ./-
```
password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx


## Level 2 -> 3
### Look -> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

#### solve:
- Both methods ensure the shell passes the correct **single argument** to the command
```bash
cat spaces\ in\ this\ filename
or
cat "spaces in this filename"
```
password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx


## Level 3 -> 4
### Look -> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

#### solve:
- The hidden file was not visible with `ls`, so it was found using `ls -la` and the password inside was retrieved with the `cat` command.
```bash
cd inhere/
ls -la
cat ...Hiding-From-You
```
password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
## Level 4 -> 5
### Look -> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

#### solve:
- use cat and rememmber level 1 method
```bash
file ./*
cat ./-file07
```
password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## Level 5 -> 6
### Look -> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

#### solve:
- . : Search the current working directory only
- -type f : Look for files only (Exclude Directories)
- -size 1033c : Look for files that are exactly 1033 bytes in size (Find uses “c” to represent bytes)
- -not -executable : Find only non executable files
- -exec file {} + : Execute the `file` command on all the results returns by find
```bash
find . -type f -size 1033c -not -executable -exec file {} + | grep ASCII
```
password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG 

## Level 6 -> 7
### Look -> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) ,[du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html), [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

#### solve: 
- . : Search the current working directory only
- -type f : Look for files only (Exclude Directories)
- -size 33c : Look for files that are exactly 33 bytes in size (Find uses “c” to represent bytes)
- -user bandit7: Find only bandit7 user files
- -group bandit6: Find bandit6's group files
- -not -executable : Find only non executable files
- -exec file {} + : Execute the `file` command on all the results returns by find
```bash
find . -type f -size 33c -user bandit7 -group bandit6 -not -executable -exec file {} + | grep ASCII

cat (file)

```
password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

## Level 7 -> 8
### Look -> [man](https://manpages.ubuntu.com/manpages/noble/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

#### solve:
- grep: Print lines that match patterns.

```bash
grep millionth data.txt
```
password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

## Level 8 -> 9
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

#### solve: 
- sort:
- uniq -u:
```bash
sort data.txt | uniq -u
```
password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

## Level 9 -> 10
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

#### solve:
- cat data.txt: print **data.txt**
- strings -e s: means look for single-byte character strings(standard ASCII).
- grep == : Filters the output of `strings`, showing only the lines that contain `==`.

```bash
cat data.txt | strings -e s | grep ==
```
password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
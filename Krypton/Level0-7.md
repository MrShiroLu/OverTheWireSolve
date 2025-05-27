## What is Krypton
**[Krypton](https://overthewire.org/wargames/krypton/)** is one of the wargames offered by **OverTheWire**, a platform designed to help you build foundational cybersecurity skills through hands-on challenges.

**Krypton** focuses on classical cryptography and is ideal for **beginners** who are interested in learning about:
- Basic encryption and decryption techniques
- Classical ciphers (e.g., Caesar, Vigenère)
- Frequency analysis and pattern recognition
- Manual and scripted cryptanalysis
- Understanding historical encryption methods
- Applying logic and problem-solving to break ciphers
## Level 0 -> 1
### Look -> base64
#### Solve 
- you can use decoder [website](https://www.base64decode.org/)
```bash
vim decode.txt
	S1JZUFRPTklTR1JFQVQ=
base64 --decode decode.txt
```
**password**: KRYPTONISGREAT

## Level 1 -> 2
### Look -> tr, rot encryption
#### Solve
```bash
cd /krypton/krypton1
cat krypton2 | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
**password**: LEVEL TWO PASSWORD ---> ROTTEN

## Level 2 -> 3
### Look -> 
#### Solve
- A to M (1 -> 13) it's being the 13th character
- 26 - 12 = 14
```bash
cat krypton3 | tr 'A-Za-z' 'O-ZA-No-za-n'
```
**password**: CAESARISEASY

## Level 3 -> 4
### Look -> Frequency Analysis ,  Substitution Cipher
#### Solve
- look for information this [site](https://www.101computing.net/frequency-analysis/)
```bash
cd /krypton/krypton3
for i in {A..Z}; do cat found1 found2 found3 | tr -cd $i | wc -c | tr -d '\n'; printf " $i \n"; done | sort -nr
```
**password**: BRUTE

## Level 4 -> 5
### Look -> 
#### Solve
- StackOverflow has nice explanation of how to solve this problem -> [site](has a very nice explanation of how to solve this problem)
- use for decrypt https://www.dcode.fr/vigenere-cipher
	- set decryption method  `Knowing the key-length/size, number of letters` set 6
	- click decrypt
-  you will see CLEAR TEXT but it's not true password don't want gap
**password**: CLEARTEXT
## Level 5 -> 6
### Look -> 
#### Solve
- similar with level 5 bu we don't know key length
- should we look all key possibilitys
**password**: RANDOM

## Level 6 -> 7
### Look -> 
#### Solve
```bash

```
**password**: 
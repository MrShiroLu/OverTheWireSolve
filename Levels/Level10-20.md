## Level 10 -> 11
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
#### Solve:
- base64 -d: decode data
```bash
base64 data.txt -d
```
password: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

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
password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

## Level 12 -> 13
### Look -> grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file
#### Solve:
- a
```bash

```
password: 
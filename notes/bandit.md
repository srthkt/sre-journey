#bandit (overthewire): Levels 0 to 13 

| Level | Goal | Command |
|---|---|---|
| 0 | Read 'readme' | 'cat readme' |
| 1 | Read a file named '-' | 'cat ./-' |
| 2 | Read 'spaces in this filename' | 'cat spaces\ in\ this\ filename' |
| 3 | Read the readable file in 'inhere/' | 'file *' then 'cat <file>' |
| 4 | Find the readable file among '-file00' to '-file09' | 'file ./file*' |
| 5 | Find a 1033-byte, non-executable file  | 'find .- type f -size 1033c ! -executable' |
| 6 | Find a file owned by 'bandit7' , group 'bandit6', 33 bytes | 'find / -user bandit7 -group bandit6 -size 33c 2>/dev/null' |
| 7 | Find the line with 'millionth' | 'greo millionth data.txt'|
| 8 | Find the line that appears once | 'sort data.txt \| grep "=="' |
| 9 | Find readbable strings in a binary | 'strings data.txt \| grep "=="' |
| 10 | Decode base64 | 'base64 -d data.txt' |
| 11 | Decode ROT13 | 'tr 'a-zA-Z' 'n-za-mN-ZA-M' < data.txt' |
| 12 | Undo layers of compression | 'xxd -r' , then 'file' + 'gunzip'/'bunzip2'/'tar -xf' in a loop |
| 13 | Use the ssh key to log in as bandit14 | 'scp -P 2220' to copy the key, then 'ssh -i sshkey.private' |

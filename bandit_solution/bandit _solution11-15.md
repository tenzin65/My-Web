<h1>Bandit Solution</h1>

<h2>Bandit 11</h2>

```

bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$ man tr
bandit11@bandit:~$ tr -c data.txt
tr: missing operand after 'data.txt'
Two strings must be given when translating.
Try 'tr --help' for more information.
bandit11@bandit:~$ cat data.txt | tr a-zA-Z n-za-mN-ZA-M
The password is 7x16WNeHi15YkIhWsFFIqoognUTyj9Q4
bandit11@bandit:~$ 

```
<h2>Bandit 12</h2>

```

bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ mkdir /tmp/tap
bandit12@bandit:~$ cp data.txt /tmp/tap
bandit12@bandit:~$ cd /tmp/tap
bandit12@bandit:/tmp/tap$ ls
data.txt
bandit12@bandit:/tmp/tap$ xxd -r data.txt > data
bandit12@bandit:/tmp/tap$ ls
data  data.txt
bandit12@bandit:/tmp/tap$ file data
data: gzip compressed data, was "data2.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 574
bandit12@bandit:/tmp/tap$ mv data file.gz
bandit12@bandit:/tmp/tap$ gzip -d file.gz
bandit12@bandit:/tmp/tap$ ls
data.txt  file
bandit12@bandit:/tmp/tap$ file file
file: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tap$ mv file file.bz2
bandit12@bandit:/tmp/tap$ bzip2 -d file.bz2
bandit12@bandit:/tmp/tap$ ls
data.txt  file
bandit12@bandit:/tmp/tap$ file file
file: gzip compressed data, was "data4.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/tap$ mv file file.gz
bandit12@bandit:/tmp/tap$ gzip -d file.gz
bandit12@bandit:/tmp/tap$ ls
data.txt  file
bandit12@bandit:/tmp/tap$ file file
file: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tap$ mv file file.tar
bandit12@bandit:/tmp/tap$ tar xf file.tar
bandit12@bandit:/tmp/tap$ ls
data5.bin  data.txt  file.tar
bandit12@bandit:/tmp/tap$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tap$ rm file.tar
bandit12@bandit:/tmp/tap$ rm data
rm: cannot remove 'data': No such file or directory
bandit12@bandit:/tmp/tap$ ls
data.txt  data5.bin
bandit12@bandit:/tmp/tap$ file file
file: cannot open `file' (No such file or directory)
bandit12@bandit:/tmp/tap$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tap$ mv data5.bin data.tar
bandit12@bandit:/tmp/tap$ tar xf data.tar
bandit12@bandit:/tmp/tap$ ls
data6.bin  data.txt  data.tar
bandit12@bandit:/tmp/tap$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tap$ mv data6.bin data.bz2
bandit12@bandit:/tmp/tap$ bzip2 -d data.bz2
bandit12@bandit:/tmp/tap$ ls
data  data.txt  data.tar
bandit12@bandit:/tmp/tap$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tap$ mv data data.tar
bandit12@bandit:/tmp/tap$ ls
data.txt  data.tar
bandit12@bandit:/tmp/tap$ tar xf data.tar
bandit12@bandit:/tmp/tap$ ls
data8.bin  data.txt  data.tar
bandit12@bandit:/tmp/tap$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/tap$ mv data8.bin data.gz
bandit12@bandit:/tmp/tap$ gzip -d data.gz
bandit12@bandit:/tmp/tap$ ls
data  data.txt  data.tar
bandit12@bandit:/tmp/tap$ file data
data: ASCII text
bandit12@bandit:/tmp/tap$ cat data
The password is FO5dwFscCbai1H0h8J2eUks2vdTDwAn

```
<h2>Bandit 13</h2>

```

bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
PS C:\Users\Tenzin Dakar> scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
bandit13@bandit.labs.overthewire.org's password:
sshkey.private            100% 1679  4.1KB/s  00:00

```
<h2>Bandit 14</h2>

```

PS C:\Users\Tenzin Dakar> ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
bandit14@bandit:~$ ls
bandit14@bandit:~$ cat /ect/bandit_pass/bandit14
cat: /ect/bandit_pass/bandit14: No such file or directory
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4UWWeTyJk8ROof1qqmcBPaLh7LDC PvS
bandit14@bandit:~$ nc localhost 30000
^C
bandit14@bandit:~$ nc localhost 30000
MU4UWWeTyJk8ROof1qqmcBPaLh7LDC PvS
Correct!
8xCjmngoKbGLhHFAZLGE5Tmu4M2tKJQo

```
<h2>Bandit 15</h2>

```

openssl s_client -connect localhost:30001
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

```
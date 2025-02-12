<h1> Bandit Solution</h1>
<h3>Command I have learned</h3>

```

<ul>
<li>c: it is used for byte, k: for kilobyte, m: megabyte.</li>
<li>-size: it is use to know the file size.</li>
<li>find /: start the search from root directory.</li>
<li>-group: filter the file that belong to group.</li>
<li>wc: it is used to count the word, bytes or character in a file.</li>
<li>sort: sort the data in file in ascending order.</li>
<li>uniq -u: filter only unique line and remove duplicate. </li>
<li>-w: it select the match words.</li>
<li>-d: it is used to decode the file or text.</li>
</ul>
```
<h2>Command Executed </h2>
<h3>Bandit 6</h3>

```

shh bandit6@bandit.labs.overthewire.org -p 2220<br>
password:morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj<br>
bandit6@bandit:~$ ls<br>

bandit6@bandit:~$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null<br>
/var/lib/dpkg/info/bandit7.password<br>

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password<br>
morbNTDkSW6jILUcOymOdMaLnOLLFVAaj<br>

bandit6@bandit:~$
```
<h3>Bandit 7</h3>

```

shh bandit7@bandit.labs.overthewire.org -p 2220<br>
password:dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc<br>
bandit7@bandit:~$ ls<br>
data.txt<br>

bandit7@bandit:~$ grep -w millionth data.txt<br>
millionth dfwvzFQi4mUOwfNbFOe9RoWskMLg7eEc<br>

bandit7@bandit:~$
```
<h3>Bandit 8</h3>

```

shh bandit8@bandit.labs.overthewire.org -p 2220<br>
password:4CKMh1JI91bUIZZPXDqGanal4xvAg0JM<br>
bandit8@bandit:~$ ls
data.txt

bandit8@bandit:~$ wc -l data.txt
1001 data.txt

bandit8@bandit:~$ cat data.txt | sort | uniq -u
4CKMh1J1I91bUIZZPXDqGanal4xvAgOJM

bandit8@bandit:~$

```
<h3>Bandit 9</h3>

```

shh bandit9@bandit.labs.overthewire.org -p 2220<br>
password:FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey<br>
bandit9@bandit:~$ strings data.txt | grep "=="
the passwordi is FGUW5iLLVJrxX9kMYMmLN4MgbpfMiqey

bandit9@bandit:~$


```
<h3>Bandit 10</h3>

```

shh bandit10@bandit.labs.overthewire.org -p 2220<br>
password:11dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr<br>
bandit10@bandit:~$ ls<br>
data.txt

bandit10@bandit:~$ cat data.txt
VGhLIHBhc3N3b3JkIGLZIGROUJE3M2ZaS2IWwULJZREZTR3NnMLIXbnBOVmozcVJyCg==

bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKbORRsDFSGsg2RWnpNVj3qRr

bandit10@bandit:~$

```



<h1>Bandit Solution </h1>

LEVEL (16-17)

```


ssh bandit16@bandit.labs.overthewire.org -p 2220

bandit16@bandit:~$ nmap localhost -p 31000-32000

bandit16@bandit:~$ncat – ssl localhost <port>

cd /tmp

touch pvt16.key

nano pvt16.key

ls -l pvt16.key

chmod 700 pvt16.key

use ssh -i pvt16.key bandit17@localhost to log in the next page of the level

```

LEVEL (17-18)

```


ssh bandit17@bandit.labs.overthewire.org -p 2220

bandit17@bandit:~$ diff passwords.old passwords.new

42c42

< ktfgBvpMzWKR5ENj26IbLGSblgUG9CzB

—

> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

bandit17@bandit:~$ exit

you will see bye-bye when trying to log into bandit18 this is related to the next level

then you will get password :-x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

```

LEVEL (18-19)

```

ssh -t  bandit18@bandit.labs.overthewire.org -p 2220 /bin/sh       

man ssh | grep terminal

-T      Disable pseudo-terminal allocation.

-t      Force pseudo-terminal allocation.

bandit18@bandit.labs.overthewire.org’s password:x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

$ ls

readme

$ cat readme

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

$ exit

then you will get password :-cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

```

LEVEL (19-20)

```

bandit19@bandit:~$ ls

bandit20-do

bandit19@bandit:~$ ./bandit20-do

Run a command as another user.

  Example: ./bandit20-do id

bandit19@bandit:~$ ./bandit20-do id

uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)

bandit19@bandit:~$ ./bandit20-do ls

bandit20-do

bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

bandit19@bandit:~$ exit

then you will get password :-0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

```
level (20-21)

```

bandit20@bandit:~$ ls

suconnect

bandit20@bandit:~$ ./suconnect

Usage: ./suconnect <portnumber>

This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.

for this level you need to make your own portal to do that we need to open two terminals 
for text level
after doing the above command than use the same portal of bandit20 in the new terminal
and use
bandit20@bandit:~$ nc -lvp 1234

Listening on 0.0.0.0 1234

Connection received on localhost 34940

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO(paste the password of bandit20)



then open the previous terminal and use
bandit20@bandit:~$ ./suconnect 1234



after the password get match ,sending the next password:- EeoULMCra2q0dSkYj561DX7s1CpBuOBt

```
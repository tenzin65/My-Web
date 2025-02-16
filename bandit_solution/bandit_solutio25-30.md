 level 25-26

 ```

ssh bandit25@bandit.labs.overthewire.org -p2220
bandit25@bandit:~$ ls

bandit26.sshkey

bandit25@bandit:~$ ssh -i bandit26.sshkey -p 2220 -l bandit26 bandit.labs.overthewire.org        

The authenticity of host '[bandit.labs.overthewire.org]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names.

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

before enter yes minimise your terminal

then you will get 



  For support, questions or comments, contact us on discord or IRC.



  Enjoy your stay!



  _                     _ _ _   ___   __  

 | |                   | (_) | |__ \ / /  

 | |__   __ _ _ __   __| |_| |_   ) / /_  

 | '_ \ / _` | '_ \ / _` | | __| / / '_ \ 

then type v to go in vim than esc + coln and type 
:shell=/bin/bash

esc+coln

:shell

bandit26@bandit:~$ cat /etc/bandit_pass/bandit26

then you will get password :-s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

```

Level 26-27

```

bandit26@bandit:~$ ls

bandit27-do  text.txt

bandit26@bandit:~$ ./bandit27-do whoami

bandit27

bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
then you will get the password :-
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

```

Level 27-28

```
bandit27@bandit:~$ mkdir /tmp/boy

bandit27@bandit:~$ cd /tmp/boy

bandit27@bandit:/tmp/boy$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo 

Cloning into 'repo'...

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names.

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit27/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

                                                       



                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames




bandit27-git@localhost's password: put the password for the previous 

bandit27@bandit:/tmp/boy$ ls

repo

bandit27@bandit:/tmp/boy$ cd repo/

bandit27@bandit:/tmp/boy/repo$ ls

README


bandit27@bandit:/tmp/boy/repo$ cat README

then you will get the password:- Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

```

Level 28-29

```
bandit28@bandit:~$ mkdir /tmp/gg

bandit28@bandit:~$ cd /tmp/gg

bandit28@bandit:/tmp/gg$ ls

bandit28@bandit:/tmp/gg$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo

Cloning into 'repo'...

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names.

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit28/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

                                                       



                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames



bandit28-git@localhost's password: 

bandit28@bandit:/tmp/gg$ ls

repo

bandit28@bandit:/tmp/gg$ cd repo/

bandit28@bandit:/tmp/gg/repo$ ls

README.md

bandit28@bandit:/tmp/gg/repo$ cat README.md

# Bandit Notes

Some notes for level29 of bandit.



## credentials



- username: bandit29

- password: xxxxxxxxxx



bandit28@bandit:/tmp/gg/repo$ git log

commit 817e303aa6c2b207ea043c7bba1bb7575dc4ea73 (HEAD -> master, origin/master, origin/HEAD)

Author: Morla Porla <morla@overthewire.org>

Date:   Thu Sep 19 07:08:39 2024 +0000
  fix info leak



commit 3621de89d8eac9d3b64302bfb2dc67e9a566decd

Author: Morla Porla <morla@overthewire.org>

Date:   Thu Sep 19 07:08:39 2024 +0000



    add missing data



commit 0622b73250502618babac3d174724bb303c32182

Author: Ben Dover <noone@overthewire.org>

Date:   Thu Sep 19 07:08:39 2024 +0000



    initial commit of README.md

bandit28@bandit:/tmp/gg/repo$ git show 817e303aa6c2b207ea043c7bba1bb7575dc4ea73

commit 817e303aa6c2b207ea043c7bba1bb7575dc4ea73 (HEAD -> master, origin/master, origin/HEAD)

Author: Morla Porla <morla@overthewire.org>

Date:   Thu Sep 19 07:08:39 2024 +0000



    fix info leak



diff --git a/README.md b/README.md

index d4e3b74..5c6457b 100644

--- a/README.md

+++ b/README.md

@@ -4,5 +4,5 @@ Some notes for level29 of bandit.

 ## credentials

 

 - username: bandit29

-- password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

```

Level 29-30

```
bandit29@bandit:/tmp/tmp.fKw3o0o2ko/repo$ git log

commit 6ac7796430c0f39290a0e29a4d32e5126544b022 (HEAD -> master, origin/master, origin/HEAD)

Author: Ben Dover <noone@overthewire.org>

Date:   Thu Sep 19 07:08:41 2024 +0000



    fix username



commit e65a928cca4db1863b478cf5e93d1d5b1c1bd6b2

Author: Ben Dover <noone@overthewire.org>

Date:   Thu Sep 19 07:08:41 2024 +0000



    initial commit of README.md

bandit29@bandit:/tmp/tmp.fKw3o0o2ko/repo$ git show e65a928cca4db1863b478cf5e93d1d5b1c1bd6b2

commit e65a928cca4db1863b478cf5e93d1d5b1c1bd6b2

Author: Ben Dover <noone@overthewire.org>

Date:   Thu Sep 19 07:08:41 2024 +0000



    initial commit of README.md



diff --git a/README.md b/README.md

new file mode 100644

index 0000000..2da2f39

--- /dev/null

+++ b/README.md

@@ -0,0 +1,8 @@

+# Bandit Notes

+Some notes for bandit30 of bandit.

+

+## credentials

+

+- username: bandit29

+- password: <no passwords in production!>

+

bandit29@bandit:/tmp/tmp.fKw3o0o2ko/repo$ git branch -a

* master

  remotes/origin/HEAD -> origin/master

  remotes/origin/dev

  remotes/origin/master

  remotes/origin/sploits-dev

bandit29@bandit:/tmp/tmp.fKw3o0o2ko/repo$ git checkout   remotes/origin/dev

Note: switching to 'remotes/origin/dev'.
You are in 'detached HEAD' state. You can look around, make experimental

changes and commit them, and you can discard any commits you make in this

state without impacting any branches by switching back to a branch.



If you want to create a new branch to retain commits you create, you may

do so (now or later) by using -c with the switch command. Example:



  git switch -c <new-branch-name>



Or undo this operation with:



  git switch -



Turn off this advice by setting config variable advice.detachedHead to false



HEAD is now at 081ac38 add data needed for development

bandit29@bandit:/tmp/tmp.fKw3o0o2ko/repo$ ls

code  README.md

bandit29@bandit:/tmp/tmp.fKw3o0o2ko/repo$ cat README.md

# Bandit Notes

Some notes for bandit30 of bandit.



## credentials



- username: bandit30

- password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

```


# THM Linux Fundamentals 2

[TryHackMe | Login](https://tryhackme.com/jr/linuxfundamentalspart2)

---

## Task 1 - Intro
 - Run your first few scripts and executables!
---

## Task 2 - Accessing Your Machine Using SSH (Deploy)

```shell
ssh tryhackme@10.10.231.129
```

---

## Task 3 - Introduction to Flags and Switches

> 1. What directional arrow key to go down a man page?
```
down
```

> 2. What flag would we use to display the output in a human readable way?
```shell
ls -h
```

---

## Task 4 - Filesystem Interaction Continued

> 1. How to create a file "newnote"?
```shell
touch newnote
```

> 2. On the deployable machine, what is the file type of "unknown1" in "tryhackme's" home directory?
```shell
ASCII text
```

> 3. How would you move "myfile" to "myfolder"?
```shell
mv myfile myfolder
```

> 4. What are the contents of "myfile"?
```shell
THM{FILESYSTEM}
```

---

## Task 5 - Permissions 101

```shell
total 16K
-rw-r--r-- 1 user2     user2       14 May  5  2021 important
-rw-r--r-- 1 tryhackme tryhackme   16 May  5  2021 myfile
drwxr-xr-x 2 tryhackme tryhackme 4.0K May  4  2021 myfolder
-rw-r--r-- 1 tryhackme tryhackme   17 May  4  2021 unknown1
```

> 1. Who is the owner of "important"?
```
user2
```

> 2. Command to switch to "user2"?
```shell
su user2
```

> 3. Switching to that user, whats the contents of "important"?
```
THM{SU_USER2}
```

---

## Task 6 - Common Directories

> 1. What is the directory we'd expect logs to be in?
```
/var/log
```

> 2. Which directory is similar to how ram works?
```
/tmp
```

> 3. Home directory of the root user?
```
/root
```

---

## Task 7 - Conclusions & Summaries

> Nice work! This room was quite theory-heavy and covered quite a range of the fundamentals in getting you familiar with Linux. See you next in [[THM-Linux-Fundamentals-3]]

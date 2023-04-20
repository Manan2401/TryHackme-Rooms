# THM Linux Fundamentals 3

[TryHackMe | Linux Fundamentals Part 3](https://tryhackme.com/room/linuxfundamentalspart3)

---

## Task 1 - Intro

> Welcome to part three of Linux Fundamentals. This room is going to showcase some useful utilities and applications that you are likely to use day-to-day.

---

## Task 2 - Deploy Your Linux Machine

---

## Task 3 - Terminal Text Editors

> Create a file using Nano

```shell
nano NewFile.txt
```

> Edit "task3" located in "tryhackme"'s home directory. Whats the flag?

```
THM{TEXT_EDITORS}
```

---

## Task 4 - General/Useful Utilities

- Downloading files
  - ```wget https://domain.com/path/to/file.extension```

- Transfering files from your host - SCP (SSH)

  - Secure copy (SCP) allows transfering files between to computers using the SSH protocol to provide authentication and encryption.

  - ```scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt```

  - ^ copies important.txt from the local machine to transferred.tx in the /home/ubuntu directory of the remote machine

  - ```scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt```

  - ^ Tranfers /home/ubuntu/documents.txt from a remote machine to a notes.txt on our local machine.

- Serving files from your host - WEB

  - All we need to start the module is `python3 -m  http.server`

  
  > Start a web server in the tryhackme home directory and wget .flag.txt. What is the flag?
  
  ```
  THM{WGET_WEBSERVER}
  ```
  
  ---
  
  ## Task 5 - Processes 101

### Viewing Processes

> If we lauch a process after the process with pip 300 what would the new pid be?

```
301
```

> If we wanted to cleanly kill a process what signal do we send?

```
SIGTERM
```

The default signal of the ```kill``` command is SIGTERM.

> Locate the process that is running on the deployed instance (MACHINE_IP). What flag is given?

```
THM{PROCESSES}
```

> What command would you use to stop the service "myservice"?

```shell
systemctl stop myservice
```

> What command would we use to start the same service on the boot-up of the system?

```shell
systemctl enable myservice
```

> WWhat command would we use to bring a previously backgrounded process back to the foreground?

```shell
fg
```

---

## Task 6 - Maintaining Your System: Automation

> When will the crontab on the machine run?

```
@reboot
```

---

## Task 7 - Maintaining Your System: Package Management

Introduction to package management with apt.

---

## Task 8 - Maintaining Your System: Logs

> What is the IP address of the user who visited the apache site?

```
10.9.232.111
```

> What file did they access?

```
catsanddogs.jpg
```

---

## Task 9 - Conclusions & Summaries

To recap, in this room the following topics were introduced:

- Using terminal text editors
- General utilities such as downloading and serving contents using a python webserver
- A look into processes
- Maintaining & automating your system by the use of crontabs, package management, and reviewing logs

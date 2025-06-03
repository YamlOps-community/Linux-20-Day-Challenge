# Day 5: Managing Files and Directories

## Task

__Reading:__  
- Linux Basics for Hacks - Chapter 5: Files and Directorie

## Deliverables:
- Submit command history for file operations
- Note any useful command options you discovered
- Write a short note on the difference between `find` and `locate`
- Write and publish a blog or social media post on all or any of the topics covered in the past 5 days


## STUDY

```
Not every user of a single operating system should have the same level of access to files
and directories.

```

```
The root user can do basically anything on the system

```

### Permissions

_[] read
_[] write
_[] Execute

#### Granting ownership 

```chown``` 

```chgrp```

```d``` starting with d it is directory

```-``` starting with r is file

```r``` means read permission

```w``` write permission

```x``` executable

```sh

drwxr-xr-x   3 root root  4096 Mar 24 21:37 runit
drwxr-xr-x   2 root root  4096 Mar 24 21:37 samba
drwxr-xr-x   2 root root  4096 Mar 24 21:37 systemd
drwxr-xr-x   2 root root  4096 Mar 24 21:36 tabset
drwxr-xr-x   3 root root  4096 Mar 24 21:37 tasksel
drwxr-xr-x  44 root root  4096 Mar 24 21:37 terminfo
drwxr-xr-x   4 root root  4096 May  6 23:48 themes
drwxr-xr-x   2 root root  4096 May  6 23:48 thumbnailers
drwxr-xr-x   2 root root  4096 Mar 24 21:37 ucf
drwxr-xr-x   3 root root  4096 Jan 28 00:36 util-linux
drwxr-xr-x   5 root root  4096 Mar 24 21:37 vim
drwxr-xr-x   4 root root  4096 May  6 23:48 X11
drwxr-xr-x   4 root root  4096 May  6 23:48 xml
drwxr-xr-x   2 root root  4096 Mar 24 21:37 xrdp
drwxr-xr-x  19 root root  4096 Mar 24 21:37 zoneinfo

```

#### Change Permission

```chmod``` change mode, only the root or file owner can change permission

#### Octal and Binary Representations of Permissions

```001``` x

```002``` w

```004``` r

### Change Permission with UGO (<USER><GROUP>, <OWNER>)


```u+x```

```o+x```

```g+w```

Several of these combination can be used.

#### Using Unmask

For Kali and most debian, the unmask is set to 022 

### Temporary Root Permissions with SUID






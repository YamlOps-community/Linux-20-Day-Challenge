# Permissions in Linux Day 6: Understanding Permissions

## Tasks:

__Reading:__  
- Chapter 6: Permissions and Processes Management

__VIEWING PROCESSES__

The ```ps``` is the primary tool for checking processes on linux kernel. It assign a ```PID``` to the processes created and thid ```PID``` are used to track whatever is happening within the kernel.

```sh
┌──(kunleobasoro㉿DESKTOP-U6U7C75)-[~/Linux-20-Day-Challenge/day_06]
└─$ ps
    PID TTY          TIME CMD
   7204 pts/8    00:00:00 bash
  12046 pts/8    00:00:00 ps

```
Running the ```ps``` command with the options ```aux``` will show all processes running on the system for all users.

```sh


┌──(kunleobasoro㉿DESKTOP-U6U7C75)-[~/Linux-20-Day-Challenge/day_06]
└─$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.1  22444  4728 ?        Ss   04:00   0:57 /sbin/init
root           2  0.0  0.0   3060  1280 ?        Sl   04:00   0:16 /init
root           6  0.0  0.0   3076  1408 ?        Sl   04:01   0:00 plan9 --control-socket 7 --log-level 4 --server-fd 8 --
root          53  0.0  0.1  42048  3968 ?        Ss   04:01   0:25 /usr/lib/systemd/systemd-journald
root          81  0.3  0.1  32644  4480 ?        Ss   04:01   1:47 /usr/lib/systemd/systemd-udevd
root         122  0.0  0.0   7216  1408 ?        Ss   04:01   0:01 login -- kunleobasoro
root         158  0.0  0.0   4268  1664 ?        Ss   04:01   0:09 /usr/sbin/cron -f
message+     167  0.0  0.0   7860  2432 ?        Ss   04:01   0:13 /usr/bin/dbus-daemon --system --address=systemd: --nofo
root         171  0.0  0.0 219644  2432 ?        Ssl  04:01   0:10 /usr/sbin/rsyslogd -n -iNONE
root         172  0.0  0.1  17648  4224 ?        Ss   04:01   0:11 /usr/lib/systemd/systemd-logind
kunleob+     175  0.0  0.0   4332  1792 pts/1    Ss+  04:01   0:00 -bash
root         209  0.0  0.0   3068   896 ?        Ss   04:01   0:00 /init
root         210  0.0  0.0   3084   900 ?        S    04:01   0:00 /init
kunleob+     211  0.0  0.0   7284  1536 pts/2    Ss+  04:01   0:00 -bash
root         212  0.0  0.0   3068  1024 ?        Ss   04:01   0:00 /init
root         213  0.0  0.0   3084  1028 ?        S    04:01   0:01 /init
kunleob+     214  0.0  0.0   7404  2688 pts/3    Ss+  04:01   0:01 -bash
root         690  0.0  0.0   5156  1664 hvc0     Ss+  04:07   0:01 /sbin/agetty -o -- \u --noreset --noclear --keep-baud 1
root         932  0.0  0.0  19692  3200 ?        Ss   04:11   0:00 (agetty)
root        6508  0.0  0.0   3064   896 ?        Ss   08:21   0:00 /init
root        6509  0.0  0.0   3080   768 ?        S    08:21   0:02 /init
kunleob+    6510  0.0  0.0   2676  1536 pts/0    Ss+  08:21   0:00 sh -c "$VSCODE_WSL_EXT_LOCATION/scripts/wslServer.sh" 8
kunleob+    6511  0.0  0.0   2676  1536 pts/0    S+   08:21   0:00 sh /mnt/c/Users/Toyin/.vscode/extensions/ms-vscode-remo
kunleob+    6516  0.0  0.0   2676  1536 pts/0    S+   08:21   0:00 sh /home/kunleobasoro/.vscode-server/bin/848b80aeb52026
kunleob+    6520  2.0  0.7 1313380 31276 pts/0   Sl+  08:21   4:11 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
kunleob+    6564  0.1  0.3 1307392 14344 pts/0   Sl+  08:21   0:13 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
kunleob+    6583  9.1 13.0 55542924 516912 pts/0 Rl+  08:21  18:48 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
kunleob+    6597  0.7  0.5 1118316 21836 pts/0   Rl+  08:22   1:26 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
root        6608  0.0  0.0   3064   896 ?        Ss   08:22   0:00 /init
root        6609  0.0  0.0   3080   768 ?        S    08:22   0:00 /init
kunleob+    6636  0.0  0.0   2676  1664 pts/7    Ss+  08:22   0:00 /bin/sh -c cd '/home/kunleobasoro/Linux-20-Day-Challeng
kunleob+    6637  0.0  0.0   2676  1664 pts/7    S+   08:22   0:00 /bin/sh
kunleob+    6650  0.0  0.2 993200  9292 pts/7    Sl+  08:22   0:02 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
kunleob+    6760  0.0  0.0   2676  1536 pts/7    S+   08:22   0:00 /bin/sh
kunleob+    7088  0.1  0.5 998152 22772 pts/0    Sl+  08:22   0:21 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
kunleob+    7204  0.0  0.0   7552  3072 pts/8    Ss   08:24   0:00 /bin/bash --init-file /home/kunleobasoro/.vscode-server
root       11628  0.0  0.0   3076   896 ?        Ss   11:02   0:00 /init
root       11629  0.0  0.0   3076   896 ?        S    11:02   0:00 /init
kunleob+   11630  0.3  0.4 990300 16036 pts/4    Ssl+ 11:02   0:08 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
root       11641  0.0  0.0   3076   768 ?        Ss   11:02   0:00 /init
root       11642  0.1  0.0   3076   768 ?        S    11:02   0:03 /init
kunleob+   11645  0.5  0.4 992276 17812 pts/6    Ssl+ 11:02   0:13 /home/kunleobasoro/.vscode-server/bin/848b80aeb52026648
kunleob+   12309  101  0.1   9328  3968 pts/8    R+   11:47   0:00 ps aux

```
The ```ps aux``` display the following details like ```PID```, ```USER```, ```%CPU```, etc.

When you enter the ps command, the processes are displayed in the order they were
started, and since the kernel assigns PIDs in the order they have started, what you see
are processes ordered by PID number

The `top` command gives a list dynamically every 10seconds by default.

```sh
┌──(kunleobasoro㉿DESKTOP-U6U7C75)-[~/Linux-20-Day-Challenge/day_06]
└─$ top
top - 13:00:27 up  8:09,  0 user,  load average: 13.57, 33.86, 30.48
Tasks:  43 total,   1 running,  42 sleeping,   0 stopped,   0 zombie
%Cpu(s): 16.5 us, 26.3 sy,  0.0 ni, 51.1 id,  3.3 wa,  0.0 hi,  3.0 si,  0.0 st 
MiB Mem :   3857.3 total,    120.3 free,   2954.1 used,    966.2 buff/cache     
MiB Swap:   1024.0 total,      1.0 free,   1023.0 used.    903.1 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                            
   6597 kunleob+  20   0 1121132  26968  12160 S  11.3   0.7   1:39.58 node                                               
   6520 kunleob+  20   0 1325156  54440  16384 S   0.7   1.4   4:50.99 node                                               

```

#### Process Priority with nice

The `nice` command set priority for processes. With `nice` you can elevate which processes should have the needed resources allocated to it.

`The values for nice range from –20 to +19, with zero being the default value. A high nice value translates to a low priority, and a low nice value translates to a
high priority (when you’re not being so nice to other users and processes). When a
process is started, it inherits the nice value of its parent process.`

#### Changing the Priority of a Running Process

The `renice` command takes absolute values between –20 and 19 and sets the priority to
that particular level, rather than increasing or decreasing from the level at which it
started



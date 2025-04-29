Ip a


1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    link/ether 00:15:5d:98:52:45 brd ff:ff:ff:ff:ff:ff
    inet 172.24.30.48/16 brd 172.24.255.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::215:5dff:fe98:5245/64 scope link
       valid_lft forever preferred_lft forever


ifconfig


eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.24.30.48  netmask 255.255.0.0  broadcast 172.24.255.255
        inet6 fe80::215:5dff:fe98:5245  prefixlen 64  scopeid 0x20<link>
        ether 00:15:5d:98:52:45  txqueuelen 1000  (Ethernet)
        RX packets 6227  bytes 7189679 (7.1 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 3936  bytes 293469 (293.4 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 34  bytes 2856 (2.8 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 34  bytes 2856 (2.8 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


Netstat / ss -tuln


Netid State  Recv-Q Send-Q Local Address:Port Peer Address:PortProcess
udp   UNCONN 0      0         127.0.0.54:53        0.0.0.0:*
udp   UNCONN 0      0      127.0.0.53%lo:53        0.0.0.0:*
udp   UNCONN 0      0          127.0.0.1:323       0.0.0.0:*
udp   UNCONN 0      0              [::1]:323          [::]:*
tcp   LISTEN 0      4096   127.0.0.53%lo:53        0.0.0.0:*
tcp   LISTEN 0      4096      127.0.0.54:53        0.0.0.0:*
tcp   LISTEN 0      4096               *:22              *:*


Ping


PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=255 time=302 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=255 time=173 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=255 time=170 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=255 time=86.3 ms
64 bytes from 8.8.8.8: icmp_seq=5 ttl=255 time=26.9 ms
64 bytes from 8.8.8.8: icmp_seq=6 ttl=255 time=315 ms
64 bytes from 8.8.8.8: icmp_seq=7 ttl=255 time=447 ms
64 bytes from 8.8.8.8: icmp_seq=8 ttl=255 time=362 ms
64 bytes from 8.8.8.8: icmp_seq=9 ttl=255 time=385 ms
64 bytes from 8.8.8.8: icmp_seq=10 ttl=255 time=546 ms
64 bytes from 8.8.8.8: icmp_seq=11 ttl=255 time=226 ms
64 bytes from 8.8.8.8: icmp_seq=12 ttl=255 time=49.4 ms
64 bytes from 8.8.8.8: icmp_seq=13 ttl=255 time=39.0 ms
64 bytes from 8.8.8.8: icmp_seq=14 ttl=255 time=55.0 ms
64 bytes from 8.8.8.8: icmp_seq=15 ttl=255 time=41.5 ms
64 bytes from 8.8.8.8: icmp_seq=16 ttl=255 time=62.2 ms
64 bytes from 8.8.8.8: icmp_seq=17 ttl=255 time=73.4 ms
64 bytes from 8.8.8.8: icmp_seq=18 ttl=255 time=23.7 ms
64 bytes from 8.8.8.8: icmp_seq=19 ttl=255 time=35.5 ms
64 bytes from 8.8.8.8: icmp_seq=20 ttl=255 time=29.1 ms
64 bytes from 8.8.8.8: icmp_seq=21 ttl=255 time=25.8 ms
64 bytes from 8.8.8.8: icmp_seq=22 ttl=255 time=37.5 ms
64 bytes from 8.8.8.8: icmp_seq=23 ttl=255 time=33.8 ms
64 bytes from 8.8.8.8: icmp_seq=24 ttl=255 time=60.3 ms
64 bytes from 8.8.8.8: icmp_seq=25 ttl=255 time=38.7 ms
64 bytes from 8.8.8.8: icmp_seq=26 ttl=255 time=57.1 ms
64 bytes from 8.8.8.8: icmp_seq=27 ttl=255 time=24.3 ms
64 bytes from 8.8.8.8: icmp_seq=28 ttl=255 time=51.5 ms
64 bytes from 8.8.8.8: icmp_seq=29 ttl=255 time=30.2 ms
64 bytes from 8.8.8.8: icmp_seq=30 ttl=255 time=49.7 ms
64 bytes from 8.8.8.8: icmp_seq=31 ttl=255 time=19.7 ms
64 bytes from 8.8.8.8: icmp_seq=32 ttl=255 time=209 ms
64 bytes from 8.8.8.8: icmp_seq=33 ttl=255 time=68.9 ms
64 bytes from 8.8.8.8: icmp_seq=34 ttl=255 time=40.4 ms
64 bytes from 8.8.8.8: icmp_seq=35 ttl=255 time=21.6 ms
64 bytes from 8.8.8.8: icmp_seq=36 ttl=255 time=45.7 ms
64 bytes from 8.8.8.8: icmp_seq=37 ttl=255 time=160 ms
64 bytes from 8.8.8.8: icmp_seq=38 ttl=255 time=50.1 ms
64 bytes from 8.8.8.8: icmp_seq=39 ttl=255 time=24.2 ms


Traceroute



traceroute to google.com (216.58.214.174), 64 hops max
  1   10.0.2.2  1.354ms  1.391ms  1.100ms 
  2   *  *  * 
  3   *  *  * 
  4   *  *  * 
  5   *  *  * 
  6   *  *  * 
  7   *  *  * 
  8   *  *  * 
  9   *  *  * 
 10   *  *  * 
 11   *  *  * 
 12   *  *  * 
 13   *  *  * 
 14   *  *  * 
 15   *  *  * 
 16   *  *  * 
 17   *  *  * 
 18   *  *  * 
 19   *  *  * 
 20   *  *  * 
 21   *  *  * 
 22   *  *  * 
 23   *  *  * 
 24   *  *  * 
 25   *  *  * 
 26   *  *  * 
 27   *  *  * 
 28   *  *  * 
 29   *  *  * 
 30   *  *  * 
 31   *  *  * 
 32   *  *  * 
 33   *  *  * 
 34   *  *  * 
 35   *  *  * 
 36   *  *  * 
 37   *  *  * 
 38   *  *  * 
 39   *  *  * 
 40   *  *  * 
 41   *  *  * 
 42   *  *  * 
 43   *  *  * 
 44   *  *  * 
 45   *  *  * 
 46   *  *  * 
 47   *  *  * 
 48   *  *  * 
 49   *  *  * 
 50   *  *  * 
 51   *  *  * 
 52   *  *  * 
 53   *  *  * 
 54   *  *  * 
 55   *  *  * 
 56   *  *  * 
 57   *  *  * 
 58   *  *  * 
 59   *  *  * 
 60   *  *  * 
 61   *  *  * 
 62   *  *  * 
 63   *  *  * 
 64   *  *  * 


Dig




; <<>> DiG 9.18.30-0ubuntu0.20.04.2-Ubuntu <<>> google.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 22955
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;google.com.			IN	A

;; ANSWER SECTION:
google.com.		137	IN	A	216.58.214.174

;; Query time: 3 msec
;; SERVER: 127.0.0.53#53(127.0.0.53) (UDP)
;; WHEN: Tue Apr 29 20:19:42 WAT 2025
;; MSG SIZE  rcvd: 55


Nmap



Starting Nmap 7.80 ( https://nmap.org ) at 2025-04-29 20:27 WAT
Nmap scan report for ubuntu-focal (10.0.2.15)
Host is up (0.000048s latency).
Not shown: 999 closed ports
PORT   STATE SERVICE
22/tcp open  ssh

Nmap done: 1 IP address (1 host up) scanned in 0.05 seconds



127.0.0.1	localhost

# The following lines are desirable for IPv6 capable hosts
::1	ip6-localhost	ip6-loopback
fe00::0	ip6-localnet
ff00::0	ip6-mcastprefix
ff02::1	ip6-allnodes
ff02::2	ip6-allrouters
ff02::3	ip6-allhosts
127.0.1.1	ubuntu-focal	ubuntu-focal


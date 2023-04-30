---
title: HTB Notes
published: true
---
Here is a set of scripts and tools that is helpful with HTB CTF's.

```
##Initiating a quick port enumeration

$ports=$(nmap -Pn -p- --min-rate=1000 -T4 -iL Hosts.txt | grep ^[0-9] | cut -d '/' -f 1 | tr '\n' ',' | sed s/,$//)
nmap -Pn -sC -sT -p$ports -iL Hosts.txt -oA ~/my_data/APT-Labs/DetailedScan-APT
```

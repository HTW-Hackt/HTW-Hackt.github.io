---
layout: blogpost
title: TryHackeMe - Quickstart
author: HTW Hackt
date: 6.Dec 2024
description: This guide covers how to start using the learning platform TryHackMe.com.
---

# Create an Account

[TryHackMe](https://tryhackme.com), or short THM, is a beginner friendly platform to learn cyber security.
We recommend this platform for beginners and use it in our newbie events and trainings. THM offers *Walktrough* and *Challenges (CTF)* rooms, more on that later. For now we need an account. Althoug THM offers a subscription service which provides access to additional rooms, the free version is sufficient for a long time and wide area of things to learn.

You can sign up for an account [here](https://tryhackme.com/signup) and need to provide a username, e-mail and password. You should use a password manager.
Then you will be asked some questions to personalize your learning experince, this affects which *Learning Paths* will be recommended to you.

THM offers different *Learning Paths*, consisting of different rooms. Each path is design to for you to learn and experiment in different topics or fields. You can do single rooms, but for a guided experience you should commit to a path fitting for your experience and interest.

The way you learn on THM is by doing rooms. *Walktrough* rooms are intended to provide you with basic knowledge and theoretical background information. *Challenge* or *CTF* rooms are intended to provide you a hand on labs experience. In these rooms you will need to know some basics and depending on the difficulty you will get more or less tips and guidance on how to hack the box.

Once you're signed up you can acces a wide range of *Learning Paths* and *Walktrough* or *Challenge* rooms.

To hack a box you usually need to compromise it and escalate your privileges. Meaning you need to abuse a misconfiguration or vulnerability to get access and then escalate this access to root/admin privileges.
And to compromise it in the first place you will need some tools, this is where Kali comes into play. Once you have your Kali running and are connected via a vpn you can start hacking!

See our guide on Installing Kali: [Guide: Install Kali](./InstallKali.md)


#  TryHackMe VPN

THM does provide the intentionally vulnerable VMs but they only are accessable through their Virtual Private Network *VPN*. 
Once you are logged in you can find a room explainung how to connect yourself to the THM VPN [here](https://tryhackme.com/r/room/openvpn). 
This room provides more information than we need (e.g. how to install openvpn on Windows/Mac). Because of oure suggestet setup you only need follow the Tasks 1, 4 and 6.

## VPN Config File

In Task 1 you find a link and instruction to download your VPN config file.

## Connect to THM VPN

OpenVPN should already be installed on you system, however if this is not the case for whatever reason you can follow the instructions of Task 4 to install OpenVPN.
* First: open a Terminal. (Keyboardshortcut: ctrl + alt + t)
* Second: type "sudo apt update" - This step is left out in the THM room but should be done bevore every install of any software ... this command updates your package sources 
* and Third: type "sudo apt install openvpn" - This actually installes the openvpn package

Tip: If you did not adjust the download path when downloading the vpn config file, the location of your vpn config file will be "/home/*yourUserName*/Dowloads/*yourUserName*.ovpn"

## Check VPN Connecetion

Lastly you can check your VPN connection in Task 6.

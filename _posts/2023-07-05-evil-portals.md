---
title: Evil Portals & Evil Twin Wi-Fi Hacking
author:
  name: Robert Head
  link: https://github.com/n1ghtx0w1
date: 2023-07-05 08:00:00 -0500
categories: [Blog, Cybersecurity]
tags: [Evil Portals & Evil Twin Wi-Fi Hacking, Understanding Evil Portals, The Evil Twin, PhishPi, Flipper Zero Evil Portal WiFi AP, Tools of the Trade, Aircrack-NG, HAK5 Wifi Pineapple]
image:
  src: https://www.hideipvpn.com/wp-content/uploads/2022/09/evil_twin_attack.png
  width: 1000   # in pixels
  height: 400   # in pixels
  alt: evil twin
---

Hackers make use of various techniques to infiltrate networks and compromise unsuspecting victims. Among these techniques; evil portals, and evil twin Wi-Fi attacks have gained notoriety for their deceptive tactics. I'm going to briefly explain these hacking methods and shed light on some of the tools employed by red teamers and hackers to exploit them.

## Active Portals
Active portals, also known as captive portals, are a type of network authentication mechanism commonly used in public Wi-Fi networks, such as those found in hotels, airports, or coffee shops. When a user connects to an active portal network, they are redirected to a login or registration page before gaining full access to the internet. These portals serve as a means for network administrators to control and manage user access, enforce terms of service agreements, or collect user information for marketing purposes. However, active portals can also be exploited by malicious actors who create deceptive login pages to trick users into divulging sensitive information, such as usernames, passwords, or credit card details. Therefore, it is crucial for users to exercise caution when using active portal networks and ensure that the portal page they interact with is legitimate and secure to avoid falling victim to phishing attacks or data breaches.

## Understanding Evil Portals
Evil Portals, also referred to as rogue portals, are malicious Wi-Fi networks created with the intention of deceiving and exploiting unsuspecting users. These portals imitate legitimate Wi-Fi hotspots, making them appear trustworthy to users seeking to connect to the internet. Once a user connects to an Evil Portal, they are redirected to a spoofed login page that resembles a familiar website or service, such as a social media platform or online banking portal. The user is then prompted to enter their login credentials or other sensitive information, which is captured by the attacker.

The purpose of Evil Portals is to harvest user data, including usernames, passwords, credit card information, and other personal details, for malicious purposes such as identity theft, financial fraud, or unauthorized access to accounts. Hackers employ various techniques and tools to create convincing portal pages that closely resemble the legitimate sites they imitate, increasing the likelihood of users unknowingly divulging their information. 

## The Evil Twin
Evil Twin Wi-Fi attacks involve the creation of a fraudulent wireless network that closely resembles a legitimate one. By mimicking the name (SSID) and other characteristics of a trusted network, the attacker tricks unsuspecting users into connecting to the malicious network instead. Once connected, the attacker can intercept and manipulate the victim's internet traffic, potentially gaining access to sensitive information such as login credentials, financial data, or personal details.

To execute an Evil Twin attack, hackers use specialized tools that allow them to create an exact replica of the target network. These tools enable the attacker to monitor all communication between the victim's device and the internet, making it easy to eavesdrop, perform man-in-the-middle attacks, or inject malicious content. Evil Twin attacks exploit the inherent trust that users place in Wi-Fi networks, as most people assume that networks with familiar names are safe to connect to. 

## PhishPi
PhishPi is a powerful tool widely used by red teamers and ethical hackers for executing captive portal attacks and cloning websites. Based on a Raspberry Pi, PhishPi allows hackers to set up Evil Portals with ease. Its customizable features and user-friendly interface make it a popular choice for performing simulated attacks, helping organizations identify vulnerabilities in their Wi-Fi networks and raise awareness about the risks of falling victim to Evil Portals.

[Home-Grown-Red-Team](https://github.com/assume-breach/Home-Grown-Red-Team)

## Flipper Zero Evil Portal WiFi AP
Flipper Zero Evil Portal is another noteworthy tool used in Wi-Fi hacking. Built specifically for Flipper Zero devices, it simplifies the process of setting up Evil Twin attacks. By emulating a target Wi-Fi network, Flipper Zero Evil Portal can lure unsuspecting users into connecting, granting the attacker access to their sensitive information.

This project turns a Wi-Fi dev board into an open access point. When users try to connect to this access point they will be served a fake login screen. User credentials are sent to the Flipper and logged into an SD card. This tool is also deployed to help red teamers understand how victims fall prey to simulated attacks.

[Flipper Zero Evil Portal](https://github.com/bigbrodude6119/flipper-zero-evil-portal)

## Tools of the Trade
Red teamers and hackers employ a range of tools to execute evil portal and evil twin attacks. Other widely used tools by red teamers and hackers include Wi-Fi Pineapple, a versatile platform for wireless penetration testing, and Aircrack-ng, a powerful suite of tools for Wi-Fi network auditing and cracking.

[HAK5 WiFi Pineapple](https://shop.hak5.org/products/wifi-pineapple)

[Aircrack-NG](https://www.aircrack-ng.org/)

## Conclusion
Evil portals and evil twin Wi-Fi hacking presents are threats to individuals, organizations, and their sensitive data. As cyber threats continue to evolve, it is crucial for security professionals and individuals alike to stay informed about these techniques and the tools employed by hackers. By understanding the risks associated with these attacks, adopting robust security measures, and promoting awareness, we can fortify ourselves against the shadowy world of Wi-Fi hacking and ensure a safer digital landscape.

Exercise caution when connecting to Wi-Fi networks, especially in public places, to avoid falling victim to these deceptive practices. Verifying the authenticity of Wi-Fi networks, ensuring the presence of secure connections (HTTPS), and using virtual private networks (VPNs) can help mitigate the risks associated with Evil Portals and safeguard sensitive information from falling into the wrong hands.

---

<img align="center" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHVmbGdsbDFheTRjcW1oeDdwbjJlb2FmMmVpbnBmZTYwMGtyZHQwYiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/ZvLUtG6BZkBi0/giphy.gif" alt="wifi hacking" width="600" height="300">

---

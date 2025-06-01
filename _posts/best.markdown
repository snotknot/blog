---
layout: post
title:  "Networking 101"
published: false
permalink: "/networking101.html"
---

Networking basics is relatively easy to learn. I am going to write as if you know nothing.

# IP Addresses
(We will be talking about IPv4 IP addresses only in this portion of the guide)

IP addresses are a way to identify a device on a network. They are a series of numbers. 

i.e; 192.168.1.1

This is a common and basic IP address of a router on a home network. Also known as a default gateway address.

IP addresses come in a bunch of different forms. You have local IP addresses that belong to devices locally on a network, and then you have public IP addresses that are used on the public internet.

IPv4 addresses are 32 bits long, or 4 octets.

octet = 8 bits 
32/8 = 4

AKA an IP address has 4 octets.

Sticking with the IP 192.168.1.1:
                      1   2  3 4 <--- octet indicator
192 = 1st octet 
168 = 2nd octet 
1 = 3rd octet 
1 = 4th octet 

The 4 "portions" of an IPv4 address that are separated by periods are always the octets.

IPs have classes. It's easy to tell what class an IP is by simply looking at the first octet. Whatever range the number of the first octet is determines the class.

Class A: 1 - 126
Class B: 128 - 191
Class C: 192 - 223
Class D: (Multicast): 224-239
Class E (Reserved): 240-255

This means our example IP address of 192.168.1.1 is a class C address, as the first octet of 192 falls within the class C range.

Basic binary knowledge will be required to proceed forward. Reference [this](https://www.youtube.com/watch?v=o9BIuMklUWA) video.

If all 8 bits of an octet in binary are enabled or "turned on", then the numbers add to 255. This means that the maximum number an IPv4 octet can be is 255. 

IP addresses are broken into 2 parts:
- network portion 
- host portion 

Network portion: 
The network portion determines the network the IP belongs to, as well as how many devices can be on the network.

Class A: 1st octet = network portion, remaining 3 octets = host portion
Class B: First 2 octets = network portion, remaining 2 octets = host portion
Class C: First 3 octets = network portion, remaining 1 octet = host portion

The more host bits an IP address has = more devices that can fit on the network.

Class A networks can have up to 16 million devices on it. This is why class A networks are the most common in enterprise environments where hundreds, if not thousands of devices may be on a network at any given time.

A traditional home network on the other hand, such as the one at your house, will typically be a class C network. This will allow no more than 254 devices on the network. This is obviously more than enough for most home networks.

To tell if 2 IP addresses are on the same network (aka subnet), you determine the class, and then see if the network portion of both addresses are the same.

Same network:
192.168.1.12
192.168.1.19

Not the same network: 
192.168.1.129
192.168.68.125
        ^ 
        different network

Host portion: 
The host portion of an IP address is used to identify the host.

ie: 
192.168.1.1 = router 
192.168.1.2 = xbox
192.168.1.3 = laptop
192.168.1.4 = smart tv

# DHCP 

Dynamic Host Configuration Protocol (DHCP) is the traditional protocol used to assign devices an IP address when they connect to a network. When you connect your laptop to your wifi at home, your router will use DHCP to assign your laptop a local IP address.

Local, or "private" (same thing) IP addresses are not unique. What is unique however, are MAC addresses. Any hardware with a radio in it designed for wifi communications will have its very own unique MAC address assigned to the physical Network Interface Card (NIC) unique to the specifc handset.

DHCP uses what's known as IP tables. This is a table of data that links an IP address to a MAC address, allowing the network to have a unique link between each device onthe network.

The reason local IPs are not unique is because of the nature of a dynamic IP. Unless configured otherwise, a device will be assigned or "leased" a dynamic IP address. When that device disconnects, that IP address lease will expire, and that same IP may be assigned to a different device in the future.

Other than IPs, DHCP will assign devices the proper default gateway, subnet mask, and DNS settings.

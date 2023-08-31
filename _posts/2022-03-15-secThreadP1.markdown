---
layout: post
title:  "snotknot's security thread (part 1)"
published: true
permalink: "/snotknot-security-thread-part-1.html"
---

Last Updated: 8/23/23

## Introduction

Hello all, I go by “snotknot” online and I am a security enthusiast who wants to share my knowledge. I’ve always wanted to write one of these threads because there’s a lot of misinformation out there. Before we get started, it’s important to know that although I am passionate about what I will be teaching in these threads, that doesn’t mean you should blindly trust everything I say. You definitely need to do your own research too and you should use this thread more as a template and not a “go-to” resource. It’s easy to know what’s fact and what’s lies when you become more experienced at the craft, but as a beginner it can be tricky and you’re likely to be deceived. This thread of course won’t be bullet proof and there may be some things that I get wrong. 

Upon reading these threads, you will obtain a greater understanding of the techniques that the best at their craft use to remain anonymous on the internet. You will also learn the methods many of them use to enhance their privacy and security online. The title is a bit misleading, it's not just a security thread as you'll quickly come to realize.

I cannot stress this enough - These threads do not cover "everything". Teaching EVERY detail of EVERY aspect of these various crafts would be way too time consuming and overall not efficient as there are way too many situational variables that differ from person to person. On top of that: You, the reader, will not remember everything taught regardless. You are better off instead trying to learn these various topics via trial and error and it will all come naturally with time.

Reading only does so much, you also need to have some hands on experience to balance it out. You can spend 5 years reading books on how to drive as well as the laws, etc., but you will never actually learn driving if you don't get behind the wheel. Make sense?

![](https://cdn.i-scmp.com/sites/default/files/styles/landscape/public/d8/images/canvas/2022/09/15/04964401-037d-434c-88d4-765f2e8ddd1f_5b91181c.jpg?itok=AxQ-gGmm&v=1663223815)

Throughout this thread in particular, you will realize that I often reference hackers for my examples to help demonstrate points. I do that not because I condone hacking, but rather because hackers are big targets for Law Enforcement. This makes them relatively good examples to use when it comes to the topic of anonymity, which is a topic we will be covering on quite a bit throughout these threads.

Lastly, don’t expect this thread to be proofread by an English professor. There will be some grammatical errors here and there, and there will certainly be lots of comma splicing and run-on sentences. 

Let's get started.

Please take the time to read the thread I have linked below. I highly recommend that you don’t continue reading this thread until you have read the entirety of the Jolly Roger’s security thread. You will likely be confused if you skip the thread and read these threads first. It’s pretty lengthy so take your time. Jolly Roger’s security thread is a great starting point for beginners to teach them the basics of tor, tails, and other fundamentals. It’s important to start by building fundamentals. You will realize that I will touch on and teach topics that were already covered in the Jolly Rogers thread. This is due to the fact that I already wrote those portions of my thread before including Jolly Roger's thread as a resource. I recommend reading them as I may introduce a few new things.

Jolly Roger’s Security Thread (2014)

Link (clearnet): 
[https://afga.neocities.org/cyber/1B-JOLLY-ROGER.PDF](https://afga.neocities.org/cyber/1B-JOLLY-ROGER.PDF)
	
Mirror (clearnet): 
[https://www.lopp.net/pdf/Jolly_Rogers_Security_thread_for_Beginners.pdf](https://www.lopp.net/pdf/Jolly_Rogers_Security_thread_for_Beginners.pdf)

## Prerequisites

- Basic computer science fundamentals 
- Networking Fundamentals (IP addresses, subnetting, OSI Model, Routing, Switching)
- Virtual Machine knowledge and experience
- Linux fundamentals

## Don't meet the prerequisites?

If you currently do not meet the bar when it comes to the listed prerequisites, this section will provide you with some material to help jump start your journey. 

**Computer Science** 

100+ Computer Science Concepts Explained:
[https://www.youtube.com/watch?v=-uleG_Vecis](https://www.youtube.com/watch?v=-uleG_Vecis)

### **(x86)**

I am going to key in here and write this section AS WELL as linking you outside sources to prevent you from making a popular mistake. 

It is important to know that x86 is a CPU architecture. This is also known as an ISA, or "Instruction Set Architecture". x86 is a "CISC", or "Complex Instruction Set Computer" architecture. What this means is that it is a powerful CPU architecture used by more power demanding computers such as Desktops & laptops. x86 is the ISA used by most computers in the world including the one you're using right now, most likely.

The 2nd most popular CPU architecture (ISA) is ARM. ARM is a "RISC", or "Reduced Instruction Set Computer" architecture. As the name implies, it is a reduced CPU architecture for smaller, less demanding computers such as smartphones or embedded devices. Newer Apple computers are starting to use ARM, with Apple's new M1 & M2 chips.

ISA's are essentially a way for software to communicate with the CPU. How is the CPU going to execute code if the software isn't designed for the CPU architecture? This is why software that run on Windows won't run on your phone or vice versa, unless if they're ported to a different platform. 

The mistake that people make while learning about ISA's are that they try to learn **EVERY** detail about x86, ARM, or both. This is a HUGE mistake. ISA's are very complex and you do not need to know all of the various details, unless if you're trying to create an operating system from scratch using that architecture or whatever. This is similar to trying to learn EVERYTHING about cryptography. You're not a cryptographer. If you try to learn everything about everything then you're going to burn yourself out. It is NOT possible. There is not one single human on the planet who knows "everything" about IT, or even any of its subsets: cryptography, cybersecurity, etc. You just have people who are really good at certain aspects of IT than others. Lower your expectations and don't be so harsh. Study smarter, not harder.

Not that I cleared that up, I will leave you with this: What you need to focus on is the fact that x86 exists, ARM also exists, know the differences between the two (one is CISC, the other is RISC), and then learn how an x86 CPU executes code. That's all a CPU is, right? It just executes instructions.

This will require you to learn how RAM works as well. Temporary data is stored in RAM, right? RAM is volatile. Nonvolatile (permanent) storage would be your HDD/SSD.

Your RAM (Memory) will have what's called a "stack", also referred to as a memory stack. This stack will contain values, which are logical memory addresses that are made up of hexadecimal values. The memory addresses indicate where in the logical memory space the data is located. Let's say the integer "4" is stored in memory. Well, then 0x4 could be stored at the memory address: 0x0012FF90. 

"0x0012FF90" is just an example. Don't think too deep into it.

0x4 is "4" in hex, "0x" just indicates that the value is a hex value. Not all hex values have to begin with "0x", it's just a universal indicator of a hex value.

The numbering system we use in the real world is decimal notation. This is base10, correct? The characters in base10 are: 1234567890. 

Hex is base16, and the characters are 12345689ABCDEF. It's just 1-9, then A-F.

CPUs execute machine code, and the type of machine code they execute is binary (base2). When humans read the code of a compiled binary, they read what's called "Op codes", AKA "Operation Codes" which will be written in Hex instead of Binary. OpCodes are another form of machine code, and is the variant that humans read. This is because it's a more convenient way for humans to read the compiled binary. We don't wanna sit here and fucking read binary all day, right?

Next, you need to learn how the CPU interacts with these memory addresses, some in which may contain instructions to execute on the CPU, while some may contain values such as our example "0x4".

This is where the x86 CPU pointers come into play. I will now redirect you to a source that will teach the rest of the basics of x86 pointers as well as a basic assembly rundown.

Hopefully this helps.

Malware analysis - part 1: My intro to x86 assembly (Credit: cocomelonc):
[https://cocomelonc.github.io/tutorial/2021/10/03/malware-analysis-1.html](https://cocomelonc.github.io/tutorial/2021/10/03/malware-analysis-1.html)

Intro to x86 Assembly Language (Credit: Davy Wybiral):
[https://www.youtube.com/playlist?list=PLmxT2pVYo5LB5EzTPZGfFN0c2GDiSXgQe](https://www.youtube.com/playlist?list=PLmxT2pVYo5LB5EzTPZGfFN0c2GDiSXgQe)

**VMs**

Virtualization Explained (Credit: PowerCert Animated Videos):
[https://www.youtube.com/watch?v=UBVVq-xz5i0](https://www.youtube.com/watch?v=UBVVq-xz5i0)

Link to VirtualBox, one of the many publicly available hypervisors: 
[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

How to create a Win10 VM using VirtualBox (Credit: TopNotch Programmer):
[https://www.youtube.com/watch?v=sBzL_zoYt6o](https://www.youtube.com/watch?v=sBzL_zoYt6o)

**Linux**

Wikipedia:
[https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)

Linux in 100 Seconds (Credit: Fireship):
[https://www.youtube.com/watch?v=rrB13utjYV4](https://www.youtube.com/watch?v=rrB13utjYV4)

Below is a video showing you how to virtualize Ubuntu, the most popular Linux distribution, using VirtualBox.

How to install Ubuntu 22.10 LTS in VirtualBox 2023 (Credit: TopNotch Programmer):
[https://www.youtube.com/watch?v=hYaCCpvjsEY](https://www.youtube.com/watch?v=hYaCCpvjsEY)

Below is a video that will introduce you to the terminal & basic commands to run.

Introduction to Linux and Basic Linux Commands for Beginners (Credit: sakitech):
[https://www.youtube.com/watch?v=IVquJh3DXUA](https://www.youtube.com/watch?v=IVquJh3DXUA)

**Networking**

These videos posted by Network Direction are what helped me personally learn networking. I took in depth notes on Google Docs and studied them. I advise you doing the same.

Network Fundamentals (Credit: Network Direction):
[https://www.youtube.com/watch?v=cNwEVYkx2Kk](https://www.youtube.com/playlist?list=PLDQaRcbiSnqF5U8ffMgZzS7fq1rHUI3Q8)

Here is another similar playlist made by someone else. I have not watched these personally, however they appear to be high quality and the instructor seems to be good.

Networking Fundamentals (Credit: Practical Networking)
[https://www.youtube.com/playlist?list=PLIFyRwBY_4bRLmKfP1KnZA6rZbRHtxmXi](https://www.youtube.com/playlist?list=PLIFyRwBY_4bRLmKfP1KnZA6rZbRHtxmXi)

Real world example of TCP using Wireshark (Credit: Chris Greer)
[https://www.youtube.com/watch?v=HCHFX5O1IaQ](https://www.youtube.com/watch?v=HCHFX5O1IaQ)

**tips for successfully reading this thread** 
- Don’t skip ahead/skim through the thread, read in order
- read the jolly rogers security thread before proceeding past this point
- if there is something you do not understand, use Google to fill in any voids
  
If you're wanting to remain anonymous, maximize your security, privacy and so on... then above is what I personally would recommend learning. I already know this is going to generate a fuck ton of controversy but I am a firm believer that you should learn the basics of computers and networking before you rely on them to keep you anonymous. 

Many people believe there is a “go-to cheat code” that beginners can skip to in able to remain anonymous, maximize their security, etc. It doesn’t work like that. Foundational building blocks are crucial to focus on instead of cheating and skipping the basics. You have to walk before you can run if you want to master any of these crafts. 

It’s kind of like saying you can rely on autopilot in a car if you don’t know how to drive. No, you need to learn the basics of driving as well as HOW TO DRIVE so you can take over if autopilot fails you. You can’t rely on it.. we’re not there yet with technology. 

![](https://www.teslarati.com/wp-content/uploads/2021/03/tesla-model-y-crash-detroit.jpeg)

Same thing with online anonymity, you can’t just rely on Tor and Tails to make you a ghost on the internet. You can't just rely on a VPN and a password manager for your security, or a cookie auto delete extension for your privacy. These tools are not bulletproof and you may (and will) need to adjust your setup as necessary. Having the proper tools is only half of the equation. You need to also know how to use them efficiently. Granted using Tails with no knowledge is better than not using Tails with no knowledge (i.e., average Joe activist who isn’t tech savvy), but if being anonymous is an absolute must for you, then it’s crucial that you learn what’s under the hood.

If you're, for example, trying to be anonymous, then you need to know the science to breaking down online anonymity and the formula contains the methods in which can be used to identify you. Let’s say you’re a whistleblower live booting Tails and using Tor to conduct your activities. Your Tails install is connected to your home Wi-Fi and you’re storing files that are evidence to your Tails persistent volume with no intentions of wiping that USB. Notice how I mentioned you’re using your home Wi-Fi and storing evidence to your USB without any intentions of ever wiping it? This is bad opsec. That’s bad practice and consistently following these bad habits will one day come back for you.

Granted nobody is perfect but that’s why you should learn the basics of whatever you’re doing so that you actually know how it works and what’s going on behind the scenes, therefore making it less likely for you to make a mistake. Do you think career black-hat hackers know every detail about Nmap or the other tools they use? Most of them do not, but what they do understand quite well is how these tools work under the hood from a technical perspective.

Someone once told me this: Forensic investigators use automated forensic tools to make their lives easier. This is also known as "push button forensics", where you just "push a button" and the tool does everything for them. If they did not have these tools at their disposal, they would still have the knowledge on how to parse these different OS artifacts manually without relying on an automated toolkit. 

This is the mindset that I learned from many of my mentors and I encourage you to adopt the same mindset. When you learn something, try to establish a knowledge pyramid; where foundational building blocks are at the bottom of the pyramid and the more advanced will be at the top. Work your way up. 

Are you trying to be a software developer? Don't start with writing code, hold the fuck on... How is that code compiled? How is that code ran on the CPU? How is that program loaded into memory and how does the CPU execute instructions off the memory stack? 

Learning CPU instruction set architectures such as x86 as well as x86 assembly is not the easiest task and will take time.

I fully understand that if you’re wanting increased anonymity, for example, then using tools such as Tails without the basic computing and networking knowledge can benefit you. What I’m trying to say is if you require a heightened level of anonymity where you absolutely cannot be identified under any circumstances (i.e., if you're a whisleblower), then it's an absolute must to learn what is going on under the hood to higher the chances of you being successful and not being unmasked.

## Reality check

Unfortunately, the world that we live in today does not value privacy. They have fucking smart fridges now collecting your data as well as the other 50 [IoT](https://en.wikipedia.org/wiki/Internet_of_things) devices that you probably have in your house. Everything is becoming “modern” and integrating technology for no reason. Some useful, most are pointless and a reason to steal and sell your data. People these days are so stupid that companies are like “we have this useful product that can make your life easier but it spies on you and collects your data!” and people eat that shit up and only see the pros and don’t give a fuck about the privacy cons because the lack of privacy is so normalized in today’s world. Companies are slowly shoving the mindset of “privacy doesn’t matter” into the minds of our generation to “normalize” it for their own gain. The problem with security minded individuals aren’t that these devices exist, but rather their lack of configuration to better suit your privacy and needs. How do you really know your amazon Alexa isn’t just a microphone in your living room for the feds or hackers to leverage? Any modern day  phone is sealed shut and are a pain in the ass to open without using Bob the Builder’s tool kit and avoiding the warranty, so how do you know your phone is really off when you power it off? The lack of reassurance from proprietary closed source software and hardware is what makes them scary and questionable by many across the globe. You’re essentially just trusting the manufacturing company without any reason to be secure.
	
If you're interested, Edward Snowden covers more on this topic on his podcast with Joe Rogan. You can check it out [here](https://www.youtube.com/watch?v=VFns39RXPrU).
	
I didn’t bring anything new to the table with the paragraph above, everybody knows that privacy is a myth today but really the point of that paragraph is to refresh your mind with reality and to educate the people who maybe didn’t already know. Now that you’re in the right mindset, it’s also important to know that there is no such thing as being 100% anonymous on the internet. There are of course things that you can do to increase your anonymity, but honestly your OPSEC (things you do that can aid in identifying you) is what matters the most. We’ll discuss OPSEC in the next section if you’re confused so don’t worry. You could take every possible step to increase your security online successfully but if you make one stupid OPSEC mistake to blow your cover then it’s all game over. It only takes one slip up. 

Depending on your situation will obviously determine the steps you take to modify your setup to achieve your desired outcome. Some people don’t want to be “anonymous” on the internet, but want increased privacy. Remember: TOR, Tails, VPNs, accessing the dark web is all legal. It’s how you use it all that determines the legality of what you’re doing. If you’re simply browsing the dark web on security forums then you’ll be fine. I won’t discuss this any further because it’s common sense: use things for illegal shit = illegal. If you can’t comprehend what would be legal or illegal then you probably should start there. If you’re not sure on the legality of something, that’s fine… verify first or don’t do it at all. The point is you need to alter your habits/setup depending on your goals. I won’t sit here and list every single possible situation that you may be in right now. You need to obviously adjust accordingly. Be open minded. 

Lastly: You will not learn all of this overnight. It comes with time and experience, you need to be dedicated to learning the concepts. The urge to learn should be a genuine feeling. Everything discussed in this thread isn’t necessarily “hard”, but more of a “you have to do it to know” type of a thing so that’s why you should get hands on experience using the tools and methods that you learn not only from these threads, but elsewhere online. Security is a very large and broad subject. If you aren’t dedicated then you’re probably going to fall behind. 

## Privacy vs. Anonymity

I know it may be confusing at times to understand the differences between privacy and anonymity, so I created this newly added section to help people better understand the differences. It's not as complicated as it may seem.

With privacy, we're essentially controlling who has and doesn't have access to our data. For example, let's say we want to detach ourselves from central tech companies. We can do this by running the Linux operating system, using the Firefox web browser, as well as the DuckDuckGo search engine. By doing all of this, we're successfully detached from all of the major tech companies that are known for collecting and selling off your data to the highest bidder.

How, you may ask? Let's break it down.

Pros of using Linux: 

- Not using Windows = not using a Microsoft product = allows us to break free from the restrictions of Windows
- Not using Windows = not using a Microsoft product = allows us to guarantee our data isn't being collected by Microsoft
- Not using windows = less malware will be designed to run on our system (vast majority of malware is written for Windows, with the second being MacOS)
- Linux is open source, which guarantees full control over your system
- Linux is open source, which guarantees there's no malicious backdoors running on your system (you can't guarantee this with Windows)
- The only thing windows is better for is photo/video editing, and gaming. Linux is better or just as good as Windows for everything else

Pros of using Firefox: 

- Alternative to Chrome, which is developed and maintained by Google, which is one of the evil tech companies we're trying to avoid from spying on us
- Firefox uses its own engine which is way more secure than Chrome or Chrome variants (Chromium, etc.)
- Data is stored locally, appose to Chrome where it's stored over the internet to Google servers
- Less of a resource hog than Chrome

Pros of using DuckDuckGo:

- Alternative to Google, which again, is one of the companies we're trying to avoid 
- Doesn't collect your personal information, therefore you likely won't be involved in Data breaches (at least from DuckDuckGo)
- Doesn't log your IP address and blocks tracking cookies 

This gives us more power over who has our data as it guarantees other big companies (Microsoft, and Google) aren't actively spying on us and collecting our data. With the setup above, it rules Google and Microsoft out of the picture. If we don't use any social media, then Twitter, Facebook, etc. won't have our data either. This allows us to pick and choose exactly what companies do and don't have our data. The companies who have our data is determined by which companies we register accounts for and actively use. Privacy also gives us the option to decide who has access to our data, and for how long. For example, I despise Google, but I can't live without YouTube. This means that Google can still collect my data whenever I'm on YouTube. That's fine. I'm willing to trade off some data collection for access to YouTube. Allowing Google to collect my data for the hour I'm on YouTube every day is better than allowing Google to always spy on me by constantly using their various products such as YouTube, and their search engine Google 24/7. Less data is being collected on me, for a shorter time frame. The second I disconnect from Youtube, I'm completely disconnected from all major tech companies as YouTube is the only social media that I "actually" use. In contrast, compare this to if I used every social media out there while running Windows and Google Chrome. This would mean Microsoft, Google, Twitter, Reddit, Facebook, and Tiktok at the minumum would all be actively collecting my data 24/7. Jesus fucking christ. No thank you.

## The Dark Web, The Deep Web, The Clearnet, and the differences

If you ask the average Joe what the dark web is, they likely will have no idea what you're talking about. Many have "heard" of the dark web but never knew it actually existed. Well, contrary to their belief, the dark web is very much a thing. 

Many also get the dark web and the deep web mixed up with eachother, and many believe they are the same thing. The dark web is different from the deep web.

In terms of the clearnet, or the "clear web", most people know what that is. 

#### Darkweb 

The darkweb is a subset of the deepweb where darknets live. The silk road, Tor, that's all the darkweb. You may hear people call the darkweb the deepweb. They're not wrong. The darkweb can be called the deepweb, but the deepweb can't be called the darkweb.

(Wikipedia)

> The dark web is the World Wide Web content that exists on darknets: overlay networks that use the Internet but require specific software, configurations, or authorization to access. Through the dark web, private computer networks can communicate and conduct business anonymously without divulging identifying information, such as a user's location.

The "specific software" they're referring to is Tor, which is configured in a way to allow access to darknet websites and is required to access the dark web. The darknets are the actual webservers hosting the darknet websites and are often referred to as "hidden services", or "onion servers". 

Tor (The Onion Router) is a web browser based on Firefox that allows access to the dark web. It was given the name, "The Onion Router" because it offers "layers" (like an onion) of protection to anyone using it on the internet. This is also why any darknet webserver has the ".onion" extension at the end of the URL.. hence why they're called onion servers.

Most of this should be a refresher from the Jolly Rogers security thread (linked in the Introduction section).

Enough boring lore, what is the dark web and why is it used? All types of content (even those that are illegal) can be hosted on the dark web. There's no restrictions. There are no "guidelines" you have to follow while using the dark web. It's just an anarchy version of the internet. The only exceptions are forums and other types of sites on the darkweb that have their own unique admin specific rules, but those rules are only unique to that darknet. For example, many morally pruden darknet admins will prohibit any form of doxxing, child exploitation material, or any other form of illegal content. They do this mainly so that their servers won't be targetted by Law enforcement, but many of the admins do it for their own moral reasons as well.

Dread is a great example. Dread is essentially a free-speech version of reddit that is hosted on a darknet. It's also way better than reddit if you're looking for security related topics and other nerdy computer stuff.

I want to take a minute to explain the Silk Road, which was an anonymous darknet marketplace used to sell drugs and other services. In fact, the Jolly Rogers security thread that you read was written by a silk road user. The Silk Road doesn't exist today as the owner of it was arrested and the site was shutdown. However, there are still many other marketplaces today that are trying to mimic the success of the Silk Road. Everyone on the dark web knows the origin of the Silk Road as it's a staple in the Dark web world. I'll link a documentary down below, I highly recommend watching it as there are many OPSEC mistakes to learn from that Ross (the owner) made that lead to not only his arrest, but many others as well as the ultimate shutdown of the Silk Road.

Documentary:
[https://www.youtube.com/watch?v=GpMP6Nh3FvU](https://www.youtube.com/watch?v=GpMP6Nh3FvU)

OpSec lessons: 
[https://www.youtube.com/watch?v=HBTYVVUBAGs&t](https://www.youtube.com/watch?v=HBTYVVUBAGs&t)

#### Deep Web 

The deep web is essentially any part of the clearnet (or clear web) that cannot be indexed by a search engine. For example, if you log into your Google account and go into your settings, that settings page lives in the deep web. You obviously can't just find the URL to your Google account's settings on the Google search engine, that doesnt make any sense. Even if you send that URL to someone, they're going to have to authenticate with your credentials before they can even access your settings page. There's a lot of underlying backend services and webservers that are responsible for powering a variety of other frontend services and webservers. That's a big part of the deepweb.

#### Clearnet

The clearnet, also known as the "clear web" or "surface web", are the normal parts of the internet that you're used to. Google, YouTube, that's all the clearnet. If you don't need Tor to access it, it's mostly safe to say it's the clearnet. 

#### Black Web 

The "black web" doesn't exist. When people say "black web", what they really mean is the dark web. If you don't believe me, just google "black web" and google will be like "wtf are you talking about? you mean the dark web?"

## OPSEC

Operational Security (OPSEC) as a whole is a pretty broad term initially used in the Military just like a lot of IT terminology. It’s all the same concept but in security it’s essentially the small details or things you do that may be used to identify you. An example is you posting personal information on social media, that’s bad OPSEC. This doesn't mean you can't post personal information on the internet, but rather you should keep your personal life and public life separate. If you're wanting to be "anonymous", then now you have not only a public and personal life, but an "anonymous" life as well. They shouldn't cross reference at any point.

There's typically three "lives" that you will have to live: personal life, online life, and anonymous life.

Personal life: Your personal life is reserved for immediate friends and family. This is where you post personally identifiable information.

Online life: Your online life is reserved for your online activities. If you want privacy between your personal life and online life, then you obviously need to make sure that you don't cross reference personal information into your online life and vice versa. For example, you as the reader know my online life because you're reading my blog which is tied to my online life. With a bit of effort, anyone can identify who I am personally as this isn't my anonymous life, therefore I don't really take steps to prevent people from identifying me.

Anonymous life: Self explanatory. Your anonymous life is reserved for the side of you where you want to remain anonymous online. If you perform any illegal actiities, this is probably where it resides. At least it should be. If you legally and nonchalantly browse the dark web, you also should prioritize anonymity under every circumstance.

For your anonymous life, don't brag to anyone about the things you’re doing online that could potentially be illegal. Don’t tell anything to anyone. Keep to yourself, even if what you're doing is legal. It doesn't matter. Legal or illegal, your goal is to not be unmasked. You make that at a lot easier if you nonstop talk about everything you do. The reasons are pretty obvious but I will go into detail anyway. You have to pay attention to your own OPSEC while you’re online. If you drag other people into your activities, that's one additional person's OPSEC you have to rely on. The chances of you getting caught are now twice as likely because now there are two people who can make a mistake at any moment. As long as we’re on the topic, do not work with other people. There are some exceptions that make this okay as long as you triple check you’re doing everything correct to hide your identity, but that shouldn’t be something you worry about or participate in until you have more experience. I'll reiterate this from my introduction: Illegal activities are not condoned. I use illegal activities as a base example, that isn't me telling you to go out there and commit crimes.

Think about the things that can so south very quickly if people are aware of your activities because you’ve told them or involved them. They may tell other people who then tell other people, and before you know it everyone knows about your activities. 

Kevin Mitnick is a great example. He was (and still is, just on the good side now) a hacking prodigy who was arrested because his friends ratted him out for no reason, just to snitch to be an asshole. You also have to rely on anyone you involve to not snitch. If police get involved and your friends are interrogated, I can promise you they will rat you out if it means their sentence is reduced. Even if they won’t rat you out, they will probably fall for their interrogation tactics mind game tomfoolery. Everyone thinks otherwise, but I can guarantee you that unless you have the worlds most loyal best friend to ever fucking exist who will take a sentence to the face for you, then it’s not going to go well for you. So for 99.99% of people who don’t have that friend, here is a summary for you: work alone, learn to be independent. You’re going to need to solo for the vast majority of your life. If you’re double thinking working solo, spend two minutes on Google and get back to me. I’ll get you started:

Link (clearnet):

[https://www.indybay.org/newsitems/2012/03/07/18708917.php](https://www.indybay.org/newsitems/2012/03/07/18708917.php) 


**This was published prior to the passing of Kevin Mitnick. RIP Kevin Mitnick.**

## OPSEC Reality Check

This section is suited mainly for those who have an anonymous life. Even if you don't have an anonymous life or if you don't care about people identifying you, I still recommend reading this section as it will shine light towards the reality of how scary the internet can be even when you make the smallest things public. None of this really matters in other situations unless if you're specifically trying to not be identified.
	
The lack of OPSEC is something that even the most experienced security experts struggle with from time to time. Nobody is perfect which is why I created this section because there’s a lot of things that we may do that don't seem like such a bad idea but in reality can actually be used to identify us. The following examples are designed to be a reality check of how scary even the smallest details you make public can haunt you later in life. I was reading an OPSEC related post on a security form a while back ago (edit: it just so happens to be that that thread was the Jolly Rogers thread linked above haha. I get a few things off as I was writing purely off memory, but it's still useful knowledge.). The OPSEC post author mentioned something along the lines of a fellow user on the form who mentioned in one of his posts that he was watching an old show on Netflix the night prior and even mentioned the movie by name. The author of the OPSEC post then went on to explain why this is a bad idea. Can you answer why this is a bad idea without reading ahead? Congratulations if you can. Now let’s talk about why this isn't a good idea. First of all, nobody cares about what you did last night. Let’s start there. You’re over sharing in your post, this is what is called “information disclosure”. This is an example of you disclosing way more information than necessary to the public. You might as well include at the bottom of your post your full name, SSN, and where you spent your evening today. Many believe this is perfectly fine because they believe it doesn’t matter what they say online if they’re anonymous regardless. Their mindset is, “I can say anything I want because nobody can prove that message came from me or that user account is ran by me!”. This is you being cocky and assuming you can’t get be unmasked. Shut the fuck up, you’re supposed to be a ghost on the internet. That’s like hacking into a server and then uploading a bunch of ASCII dicks and messages saying “your security is shit”. You’re literally just telling them that you’re there and making your presence known. That’s like shooting your gun in a stealth mission, except here you purposely shot your gun. If this was Tom Clancy’s Splinter Cell, it’d be game over. 

Summary: Don’t overshare, or share anything about your personal life.

This makes the job of police, or someone trying to identify you easier because now they know you watched a specific old movie last night. They have the movie, and date. If they're the police, all they have to do is subpoena Netflix for the list of people or accounts that watched that particular movie on that particular date. You’re helping them narrow down their subjects. It’s an old ass movie in this case so that makes it even easier. If they have a previously recorded first/last name, country, or state that they collected from a previous OPSEC mistake of yours, then they now have a name tied to an account, an IP address to compare and cross reference connections with, or a country to cross reference where the connection was made. Notice how that list is getting smaller and smaller? Eventually they will find you. Don’t even make your continent public. Anything can be used by the feds, it’s a cat and mouse game if you’re trying to do anything illegal.
	
Last story I promise. I’ll make this one up. Let’s say you’re on a security thread tied to an account where you try to remain anonymous. You create a post and within that post, you mention that you went to Walmart and bought a bunch of apples. Can this be used to identify you? If you believe doing this is a bad idea, then you’re in the minority of people who are correct. However, if you’re someone who thinks there is nothing wrong with this because “who the fuck is going to check the security footage at every Walmart in the world to find a guy buying apples?” then you’re an example of someone who is bad at OPSEC. Remember how I mentioned to not get cocky earlier? This is you not only assuming that this won’t happen, but you’re also assuming that it’d be that hard for police to do. You’re assuming that the police have no prior data about you. For all you know they could have your full name, address, etc. but the only reason you’re not in jail is because they need proof that you own that account and made that post. They now have that proof because they have Walmart’s security footage of you purchasing a “bunch” of apples which lines up with your post. Might not be the most rock solid evidence in the world but it’s one extra thing they have on you and it’s definitely something that will help convince a judge. Even if they don’t know who you are, now they do because your face is on camera, the credit card you used to buy your groceries can ID you, they have footage of your car so they know what car you drive, and they have your license plate on camera. See how scary that is? If they know who you are then it wasn’t even hard for them to narrow down what Walmart's to get the camera footage from because they know where you live due to them knowing who you are, so they just went to the closest few Walmart’s. It’s not like you live in California but drove to fucking New York City to buy apples, no they obviously know to check the closest stores.
	
Never assume you’re not on the radar of police. For all you know they could have no idea who you are or they could be driving to your house with a search warrant as you’re reading this. You have no way of knowing for sure so don’t assume and be cocky, it’s not like the police are going to send you a text message on your phone saying “hey btw we’re watching you!”. Never get comfortable in your tracks thinking you’re safe and always be one step ahead, by being paranoid and constantly checking your security to make sure it’s the best it can be. Even when you think you have a pretty good setup and believe there’s nothing you can do to improve, you still need to ask the occasional question of “am I sure there is nothing else I can do to improve my setup?”. 

## LEO & Snitch

I covered on this in my OPSEC sections, but I decided to make this its own section because of how important it is. LEO (Law Enforcement Officers) can and will interrogate your snitch friends. This is one of the main reasons as to why you should not involve your friends in any illegal activities you are participating in. I will reiterate this again: I don't support or condone illegal activities.

If I have any true crime readers, you know the power of interrogations. There are plenty of interrogation videos publicly available on the internet such as YouTube for you to watch. If you're dumb enough to talk during an interrogation in the first place, only then do you have to worry about the tactics that detectives will use. 

You're not legally obligated to talk throughout interrogations. Use the 5th ammendment to your advantage.

Quick summary: 
1. Keep to yourself 
2. Work alone 
3. Nobody will go to jail for you 

## Forensics
	
Computer forensics is something you need to really buckle down and study. Being aware of how computers function and the methods that police or someone trying to identify you will use on you to help identify or arrest you is crucial. Same goes for if someone gains unauthorized physical access to your computer or one of your drives. Police who work in forensics have one job: to find evidence on your computer to preserve for court to get you arrested. Your job is to obviously make their job harder so that doesn’t happen to you. If there’s no evidence on your computer, then what are they going to show up to court with? The answer is nothing… for the most part. It’s obviously trickier than that, fortunately though not by much. Assuming they don’t have evidence that you freely gave them by OPSEC mistakes online, then all that falls into consideration is what’s on your computer and any other devices. 

Search warrant:

> A search warrant is a court order that a magistrate or judge issues to authorize law enforcement officers to conduct a search of a person, location, or vehicle for evidence of a crime and to confiscate any evidence they find. 

Search warrants are going to be what you need to look out for. The judge who signs the search warrant specifies what items are to be searched for and ceased. The judge very likely will specify any electronics such as but aren't limited to:

- computer(s)
- any storage devices (HDD's, SSD's, USB's, SD Card's, etc.)

Essentially anything with an electronic chip in it will likely be on that list. If you didn’t take steps to prevent evidence from being stored or wiped on your devices, then you probably are going to be caught and arrested. 

FYI: Anyone can use these methods, not just police.

I’ll go over a couple of methods that police may use when they find files that may be potential evidence. They have to verify that it’s valid evidence and ties to your activities, correct? One method they may use is by checking the MAC times of your files. MAC stands for “Modified, Accessed, Created”. As you probably have guessed, these are the times a particular file on your computer was last modified, accessed, and when it was created. On Windows, if you right click on a file and go to “Properties”, you can see the MAC times. These times will be used to help create a timeline of your activities or may be proof that you last used something at a particular time.
	
Windows also has the capability of showing what programs on your computer were last ran, at what times, for how long, by what user, etc. There's a lot of methods that can be used on all operating systems, but Windows in particular makes these methods very easy to do. These are just a couple examples of methods that police will likely use. This is why keeping everything off disk is crucial so that there’s no files that can act as evidence that ties to your activities. Instead, all evidence should be maintained on some sort of external media (USB, SD Card, etc.) so that you can easily nuke these drives to permanently remove any evidence that was previously stored on them. You can nuke an SSD that has your Windows (or whatever OS you use) installed on it too if you’re being an idiot and storing everything directly to your computer’s main storage, but doing so would nuke your main OS install as well as any other data. It’ll also take ages since you’re trying to nuke a drive with a large capacity. 
	
You hopefully know that files you delete on your computer aren’t actually “deleted”. These files can be recovered not only by police, but anyone who downloads a file recovery tool which are easy to find online. Run one of these programs against a random flash drive you own, you’ll probably find files you forgot you ever made. This means if you sell an old Hard Drive to someone, they could potentially access some of your data even if you format it. You having to frequently nuke drives with evidence on them is another reason why you need to store them on small capacity external media, because it’s more convenient to nuke a 32gb USB Flash Drive than a 500gb SSD. Also, if you create a file that you know will be considered as evidence, don’t name the file any keywords that could hint your intentions. Let’s say you’re buying drugs on some sketchy ass marketplace (It's an example. Don't do drugs kids). Don’t name your file “top 10 drugs from (nameOfMarketplace)”. If you’ve ever used a file recovery application before, you may have realized that maybe files were recovered but they don’t contain any contents. You can only see the name of the file, meaning you know it existed at one point. If you don’t know how nuking a drive works, the program will overwrite the segments on the drive containing the data with other random data to overwrite it with fake data. However, it’s not always perfect and some segments may be missed. This is why you should run multiple passes when nuking a drive to ensure everything has been overwrote. One segment containing the metadata (name of file, etc) maybe was missed by the nuke, but the segments containing the actual contents of the file were successfully overwrote. Now you’re left with metadata of a file but you don’t have the contents. That’s why you may often see files with little to no file size. Do you see how this is bad if you name a file something that could help police? If they run a file recovery on your drive, they could find metadata of a file that existed at some point in time, even though they don’t have the contents. They have the name which alone may be evidence you participated in activities. In this hypothetical example, they are now aware that you know that particular marketplace exists due to you naming it by name in your file name, and they also know you likely visited that marketplace at some point due to you having a list of their best products. If you’re interrogated and claim that you weren’t aware the marketplace exists, but then police find this file, it will be evidence that counters your claim of “not knowing it exists”.
	
Having a BIOS password is also a pretty smart idea. This will obviously require an administrator password to access the BIOS on your computer. This all will also help if anything gets stolen, not much they can do. If they’re not tech savvy they’ll probably just throw it away or try to sell it. Their only other option will be to hard wipe it. Either way your data won’t be in their hands. Same thing goes for any flash drives or other external media that may be lost or stolen. 


## Tails
![](https://tails.net/contribute/how/promote/material/logo/tails-logo-flat-inverted-notagline.svg)

If you don’t know what Tails is then you didn’t read the Jolly Roger’s security thread like I told you to, so go back and fucking read it moron. ;). I love tails, it’s great. If you want to try it out, you can install the ISO from their site and virtualize it with KVM, Virtual Box, or whatever hypervisor of choice. Only run Tails in a VM if you’re testing out the features to see if you like it (some features also don’t work virtualized or are pointless). Don’t unironically virtualize Tails if you’re genuinely wanting privacy. I’ll discuss a couple reasons not to, but for a full list you can visit:

[https://tails.boum.org/doc/advanced_topics/virtualization/index.en.html](https://tails.boum.org/doc/advanced_topics/virtualization/index.en.html)

Tails is one of the best tools that you can utilize if you’re wanting to remain anonymous online. Even for general security needs, depending on your situation. Tails is considered an “amnesiac” operating system because it’s an anti-forensics operating system that runs portable on external media such as a flash drive. It’s a live boot OS that comes prepackaged with many security driven features by default such as automatically spoofing your MAC address with every boot, routing your traffic over the  Tor network, and much more. Tails does so much more than that and if you want a full comprehensive list then you should check their website. They go into all of the details.  I only use tails if I want to be anonymous, I don’t daily drive Tails as my main OS or use it to log into my personal online accounts. That’s fucking stupid. You either go all out and remain fully anonymous with Tails or you use a normal setup such as Windows, MacOS or Linux. There’s no in between in most cases. 

Most people use tails if they want to be a ghost and leave zero trace of their activity as if nothing ever happened. You can do that if you know how to properly utilize Tails and its features. The reason why tails is deployed as a live boot is to keep as much off your actual computer’s hard drive as possible. When you run a virtual machine, that virtual machine leaves traces on your host machine. How do you think that VM runs? It’s running locally on your computer as you hopefully know. Leaving traces of evidence on your computer obviously isn’t the best idea so you need to prevent that. Tails does that for you since it’s a portable plug and play OS. You’re just using your computer as the “control station” to control Tails. 

Also, do not download anything to disk on Tails. Many people believe that since they’re booting off a Tails USB, that any files they download will be stored to the USB. This is not true, the file will be temporarily stored to your computers hard drive. If you download something, specify the download location to your persistent volume (google “tails persistent volume tutorial”, if you don’t know what it os. it’s very easy to setup) or another safe option such as another USB. Just remember that if the file is potential evidence, whatever drive it’s on will need to be wiped afterwards. Wiping a file instead of an entire drive is also a valuable option in some situations but it’s just overall easier and also more secure to wipe an entire drive. I won’t show you how to use Tails. I promise it’s not hard… it really isn’t. Do 5 minutes of googling and watch a YouTube video or two and I you’ll get it in no time. Tails also isn’t the only “security driven OS” out there. There’s many, but Tails, QubesOS, and Whonix are the most popular.
	
Tails by default routes all network traffic through the Tor network. Yes, all of it. Any applications you use, if you ping something in your terminal, it all will go through Tor. The reason this is great is because typically on a normal computer running the Tor browser, only the Tor browser will be routing its traffic over Tor. What about other applications running in the background on your computer? Those won’t be going over Tor. This means you have other background services snitching on you because their traffic is being sent over your real IP address or your VPN or whatever. You’re not very anonymous if you’re doing a bunch of illegal acticities while your personal OneDrive account on your host machine is downloading a file off the internet or is updating, are you? If you gain enough attention to get the feds at your home then your computer will probably have enough evidence for you to be charged.

## Operating Systems
	
Many people overthink what OS they want to use. It obviously comes down to preference, what you need, and what you’re capable of using. 

A good rule of thumb is to **avoid Windows at all costs if you are doing anything illegal/sketchy online** and must remain anonymous. Windows is known to have backdoors and overall is proven to be a telemetry spyware garbage OS that sends everything imaginable to Microsoft servers. For example, Microsoft stores a copy of your Bitlocker key without your knowledge.  

It honestly doesn’t really matter as long as you know the risks that come with your OS of choice. For example, both MacOS and Windows are closed source proprietary operating systems. This means the source code isn’t public so you don’t actually know what’s going in the background on your computer. There’s no way to verify. You also need to be aware of the amount of bloated stuff Microsoft jams into their shitty operating system that runs over the network. So again, think about that when you’re doing anything fishy, questionable or illegal. Same goes for MacOS and linux in terms of applications running in the background although barely as much on linux. Also, both Windows and MacOS are terrible options from a security perspective. I won’t go too deep into detail but just know that of the three, Linux is the least targeted for hackers because most people run the other two. From a privacy perspective, Linux is your best option all the way. Linux is also open source and you have full control over your computer unlike MacOS or Windows.

You hopefully are able to tell that this is only relevant if you’re simply trying to increase your privacy/security online and not necessarily be relevant for being “anonymous”. If that’s your goal then the security driven operating systems below are for you. 

## Security/Anonymity Driven Operating Systems
	
This section will cover Tails, Whonix, and QubesOS. 

You obviously don't "have" to use these OS's to be anonymous on the internet, however it is recommended as they are designed for that exact purpose and take care of many factors for you. Can you take an ubuntu machine and configure it to be anonymous online? Of course you can, but it's more convenient to simply boot into a Tails USB, or a Whonix VM.

![](data:image/png;base64,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)



Whonix is another security driven OS similar to Tails, but instead of being designed to run in a live boot environment off external media, Whonix is designed to run in a virtual machine. If you want to leverage a security driven OS but don’t want to power down your computer to boot into a live boot USB then Whonix can be useful. Whonix allows you to switch in between your host OS and your Whonix VM simultaneously. Whonix obviously runs on a hypervisor on top of your host OS using Virtualbox, KVM, or whichever hypervisor. Depending on your needs Whonix may be useful but Tails is an anti-forensics amnesiac OS and most importantly, it runs off external media and doesn’t store anything to your actual computer. Due to Whonix running in a VM, the files to that VM will be stored to your actual computer. 

Yes, you can store the VM files to encrypted external media and boot off it that way to keep it off disk, but you still oppose the risk of your host OS performing activities automatically in the background either locally or over the internet that can ruin your OPSEC and unmask you without you knowing. Are there ways to counter this? Of course, remember how I said earlier to have an open mind and use what works for you? You can obviously create your own unique workarounds and modify your setup to make it bend to your needs. You just need to make sure that you’re not taking shortcuts that can ruin your OPSEC and only use these workarounds if they’re efficient and convenient. If having access to your host OS is a must, then you can create a workaround by disabling the NIC on your host OS by “ifconfig down”’ing it or whatever method works best to ensure nothing on your host can call out to the internet. There are ways to make it work and if putting in the effort to make these workarounds and exceptions in able to use Whonix sounds valuable to you, then go ahead and do it. For me however, it just sounds easier and more efficient to power off my computer, plug in my Tails USB, and boot directly into it. I never really find myself needing access to my host OS because all of the files I ever end up needing are either on my Tails persistent volume, or other encrypted external media. If you’re going to use Whonix, I recommend using it for KVM if you’re on linux. 



![](data:image/jpeg;base64,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)


 
Now let’s talk about QubesOS. QubesOS is a security driven OS that uses virtualization and compartmentalization to harden your security using permission restricted “qubes” or contained virtualized environments that are separate from every other aspect of your computer.  Unlike Tails or Whonix, QubesOS is designed to be installed bare-metal to your system and runs as its own hypervisor. QubesOS is a type-1 VM that uses XEN to function with bare-metal speeds. Ready for some homework? Take 30-45 minutes of your time and go to QubesOS’s website and read their documentation on how QubesOS works and why it’s great. They also have a FAQ section that answers a lot of interesting questions. Their website does a really great job at explaining in great detail how QubesOS works, holding your hand along the way and making it really easy to follow along and understand. 


QubesOS Intro Link (clearnet): 

[https://www.qubes-os.org/intro/](https://www.qubes-os.org/intro/)

QubesOS FAQ Link (clearnet): 
[https://www.qubes-os.org/faq/](https://www.qubes-os.org/faq/)

After reading through the material above, you can start to see how valuable QubesOS is. It really is one of the best options out there if you’re looking to turn a spare workstation you have into a dedicated “privacy friendly” computer. That’s the only way I personally would use QubesOS. The concept of QubesOS is great and it does offer a lot of value at its current state, but daily driving it or replacing it as your main OS is a really bad idea as it can be non user-friendly at times and arise a lot of issues from time to time. If you’re a beginner to Linux or unix environments or IT in general, do not try QubesOS. It is very advanced and will put a fuck ton of stress on a typical user. Don’t let that discourage you though, QubesOS truly is a masterpiece but to utilize the most out of it you need to know how virtualization and compartmentalization works. You need to understand the basics of QubesOS, and how it uses isolation to keep your data safe. All of this can be answered on their site. It took me an hour, if that, of reading their site and watching reviews on YouTube to understand how QubesOS works on a basic level. If you have a dedicated drive or computer to store it on, it’s great, but if Windows for example is the only OS on your computer, then don’t expect to replace it with QubesOS and have a fun time. QubesOS is great, but not as your “one OS for everything daily driver” type of great. It’s great for when you want privacy, but other than that you want to boot back into your Linux distro of choice, Windows, MacOS, etc. 
	
QubesOS is very resource heavy as you’d probably expect due to the amount of virtualization it uses. If you have anything below 16gb of RAM and at least a quad core CPU, don’t even try it. It’s definitely doable with less than 16gb but you’ll likely run out pretty quickly after having a few qubes open. I’ve also heard they’re pretty strict on hardware requirements. If you really want to get fancy, you  can use Qubes-Whonix. Yes, it’s exactly what you’re imagining. It’s whonix built into QubesOS. Instead of your host OS being Windows, Fedora, Arch, etc. while using Whonix, it’s QubesOS.
	
All of these different security based operating systems are great and have their pros and cons. If you’re trying to be a ghost on the internet, Tails is your best bet. If you’re just looking for a security friendly VM to fire up, whonix is great. If you want an OS that is shockingly good at privacy, use QubesOS. That doesn’t mean however, that you can’t use whonix or QubesOS to be fully anonymous, tails is just better suited for that directly out of the box in my opinion without configuration. Again, these setups can be modified.

## Cryptography
	
We as end users of a computer have the privilege of leveraging encryption. Can you imagine how hectic the internet, software, applications, etc. would all be if it weren’t for encryption? Encryption is also what you’re mostly going to be using to increase your privacy, anonymity, freedom, and security. A very large portion of activities that we do on our computers benefit from encryption and we often don’t even realize it, we just take it for granted. That’s exactly how it should be.
	
It's recommended to take time to learn how encryption works and why it’s viable. You should know what a cipher is as well as cipher-text. What are a few ciphers out there? You should study how a basic cipher works at a basic level, an example could be a substitutional cipher such as Rot13. You don’t necessarily need to explain with great detail how these different types of ciphers work, but understand what they are and the basics of them. You should at least know how a substitutional cipher works though, they’re very simple and a great introduction to learning encryption basics. I won’t go into private and public keys because the Jolly Rogers security thread covered more on that. The very, and I mean the absolute VERY vast majority of people don’t know everything about encryption and how each cipher works in great detail. That’s too much nor is it really relevant or viable information worth studying in most cases. What is worth studying however, is the basics of how encryption works. You should also know the difference between encryption, encoding, hashing, and hash salting. They are all different.

With encryption, you take the data you’re trying to encrypt (plaintext), and you use the encryption algorithm (cipher) to encrypt the data and scramble it into a form (ciphertext) that is only readable by the private key, also known as the "decryption key".

![](https://media.geeksforgeeks.org/wp-content/uploads/20210224215653/fgfdgrfgrf21.png)

The goal with encryption is that the data in which is being encrypted is meant to be securely stored temporarily, rather in a system or during transit, and is designed to be decrypted at some point in time. Does that make sense? The data that is encrypted is eventually going to be decrypted. 

With hashing, there’s no “unhashing” or reversing it back to plaintext with a key like you do with encryption. Once you hash data, there’s no reversing it. You can attempt to crack the hash value (the output result of hashed data), but that often takes a lot of computing power and is typically only successful if it’s a weak string that was hashed such as a weak password. With hashing, you use a hash function (similar to an encryption algorithm (cipher)), and then the hash function will scramble the plaintext data into a fixed-bit string value referred to as the hash value, or “checksum”.  

An example of someone running the "Get-FileHash" command in a Powershell instance to get the MDF checksum of an .exe file: 

![](https://webapps-cdn.esri.com/CDN/support-site/technical-articles-images/000020408/00N39000003LL2C-0EMf2000000FWuI.png)

File hashes are essentially the "fingerprints" of digital files. If even one byte of the file is modified, the file will be assigned a completely different hash value.

That’s the difference between encryption and hashing, that encryption is designed to temporarily secure data and then decrypt it when appropriate, whereas hashing is designed to permanently secure data without ever “dehashing” or “reversing the hash” back to plaintext. 
	
Encryption is typically used during online communications. For example, let’s say you’re messaging someone on your phone using an encrypted messaging app such as Facebook Messenger or Snapchat. When you send someone a message, the contents of your message (plaintext) are encrypted during transit to the receiver. Once it arrives at the receiver, the private encryption key (the key required to reverse the ciphertext back to plaintext) then decrypts the data and shows it in plain text to the person you’re messaging. Hashing is typically used to securely store user data to a database. For example, let’s say you’re creating a Google account. Google hashes your data (some of it), they don’t store it in plaintext on their servers. This includes your password. If Google suffers a data breach, your password won’t be leaked because your password is hashed. This means the hash value equivalent of your password is stored in Google’s servers, not your actual password. Are you following along? The hacker won’t have access to all of the user passwords stored on the server he compromised, but rather the password hashes. He can’t get your actual password unless if he manages to crack your password hash, but considering Google has a pretty good password policy, that very likely won’t happen. This means that even Google doesn’t know your password because even they can’t decrypt it. Why? Because it’s HASHED, not encrypted. They do have access to whatever data they encrypt however, since they own the private encryption keys to decrypt them. This should be obvious. You're using their servers.

So, to put this all together for it to make sense, I’ll hit you with this final example. Let’s say you make a Snapchat account and you message your friends. What does Snapchat have access to and what do they not have access to? Let’s start with what they don’t have access to. Snapchat does not have access to your password because your password is hashed before they store it on their servers. This goes for whatever other data they hash, but your password is definitely at least hashed (or so they claim). What they do have access to is your messages because they’re encrypted. They’re obviously encrypted, correct? That’s the only logical answer because it’d be impossible for them to be hashed due to your messages having to be unscrambled back into its original form for it to readable for the recipient, correct?? RIGHT?? Hopefully that makes sense. 

Here’s your homework. Try to decode this (you won’t have the knowledge on how to decode this from reading this thread, but if you do your own research you can figure it out. Hint: It uses a substitutional cipher):

	Pbatenghyngvbaf vs lbh jrer noyr gb qrpbqr guvf. Ubj qvq lbh qb vg? Qvq lbh cerqvpg vg jnf ebg13 be fbzr bgure sbez bs n fhofgvghgvba pvcure whfg ol ybbxvat ng vg? Qvq lbh hfr n pvcure qrgrpgbe fhpu nf gur bar sebz qpbqr? Ertneqyrff, tbbq wbo.

	~ fabgxabg

The message above is actually “encrypted”, to be technical, but the type of cipher (substitution) is extremely old (literally, we’re talking hundreds of years) to the point that it’s considered encoding by many because the key is not kept secret and doesn’t follow kerckhoff’s principle. 

Kerckhoffs's principle:

> a cryptosystem should be secure even if everything about the system, except the key, is public knowledge.

Encoding is just encryption’s little brother, because encoding is designed to scramble data into a bunch of random characters but it’s also designed to be easily decoded or unscrambled back to its original form. With encryption on the other hand, it’s not designed to be easily unscrambled. It’s designed to be securely encrypted and only decrypted by the private key which its methods are complex and unknown (follows kerckhoff’s principle). Hundreds of years ago that was a viable way of encrypting messages, but it’s so outdated now that the key is well known and is pretty much now as useful as encoding. If you want to get REALLY fucking technical and nerdy, it’s considered encrypting because it’s still considered cryptography, even speaking a different language can be considered cryptography. Other people who have the key to decrypt what you’re saying (if they speak the same language) can understand your message. Cryptography obviously isn’t just limited to computers and has existed for centuries. Did you know that languages were actually created for that very reason? People wanted to communicate but they only wanted to be understood by their allies. Hence why different languages were created because knowledge is power, and they wanted to keep that knowledge a secret and out of the hands of their adversaries while talking or writing.

![](https://emojiisland.com/cdn/shop/products/Nerd_with_Glasses_Emoji_2a8485bc-f136-4156-9af6-297d8522d8d1_large.png?v=1571606036)

The current encryption standards that are mainly used today are AES and RSA. Both of these follow the "standards" of modern-day cryptography and follow kerckhoff’s principle. AES (Advanced Encryption Standard), was created when an alternative for DES (Data Encrpytion Standard) was required. 

We utilitze AES daily as most websites are running over HTTPS, which utilize SSL/TLS. Both of these use AES. Cryptography advances with technology and time. AES will be useless years from now (maybe in 10 years, maybe in a hundred) when we have quantum computing and further advanced crpytography. 

I saved hash salting for last because it's boring as fuck. Hash salting is when random bytes of data are appended either into the hash value or at the end of the hash value. This makes cracking the hash harder as the threat actor will also have to work around the salted bits of the hash. Depending on the methods used for salting, the threat actor may have to determine the algorith used for the salting procedure to find out how it works and how to work around it. If bits are simply appended at the end, you usually can just remove the bits if you know which bits are the salted bits and not part of the hash. 

## Encrypting Drives, Files & VMs
	
Encrypting your drives is an easy thing that we all can do that brings a lot of value. There’s pretty much no reason not to; it’s fast, easy, and brings many benefits. The main reason is to keep your data safe. If your computer gets lost, stolen, or ceased by police, they will be met with an encrypted file system that requires a passphrase to decrypt it and allow access to it. If you lose your computer, then at least whoever finds it will be out of luck getting hands on your data and will be forced to sell it or wipe it. Same for if your computer is stolen. If police cease your computer, then they may have the capabilities to force you to give up the passphrase. I don’t know much about those laws so you may have to do some googling if you care. The point is however, that if it ever gets to that point then it shouldn’t matter regardless because you should have kept anything incriminating off disk and instead on encrypted external media that you wiped afterwards, correct? 

Other benefits that come from utilizing encryption on all your drives is if you install malware, it won't spread to other partitions or drives since the malware can't read or write to said partition/drive due to it being encrypted. However, if the drive is decrypted and mounted to your malware infested file system, the encryption will obviously be useless. 

It's a good idea to encrypt everything you can, within reason. It's not convenient to encrypt literally every file and folder on your file system, but if you have a folder that contains sensitive documents in it, it won't hurt to encrypt it real quick. Even a password protected zip file will work. Full disk encryption of your OS drive is a good start, but once you boot into your OS drive and enter the passphrase to decrypt it, the encryption benefits will disappear until the computer is shut down and encrypted once again. After all, this doesn't really matter, right? The only reason we're even encrypting our OS drive/partition in the first place is to prevent the data from being accessible by someone who steals our computer. This means that if your only layer of encryption is your OS drive and then you download malware that compromises your decrypted OS drive and file system, there won't be any additional layers of encryption that will prevent the attacker from obtaining sensitive data. Any files/folders will be there for them to potentially obtain. If the important files/folders are encrypted, the damage of the compromise will be way less severe as they'll only be able to access low hanging fruit that isn't encrypted. Again, you don't have to necessarily encrypt every file and folder, but rather the files and folders that contain extremely sensitive information that you wouldn't want anyone obtaining if they were to theoritically compromise your system in the future. Is there a folder on your system including tax documents? May want to encrypt that with a relatively strong password. 

Another good idea is to encrypt any virtual machines you may end up using. When you create a virtual machine, the hypervisor will store files belonging to the virtual machine on your system. These files are what make up the VM. If these files are hypothetically stolen by malware, the threat actor will have a copy of your VM and will be able to boot into your VM and access its contents. Granted, they'll need to access the windows/mac/linux/etc. user password to log in, but what if they crack it because you used a weak password such as "123"? What if you enabled auto login without a password? If it's hypothetically a VM that you used for finance related activities and they happen to obtain access to it, they will be able to use that VM from the last state you left it in. 

This should also be obvious but I'll mention it anyway: It's obviously a good idea from an OpSec perspective to encrypt any VMs you end up using for illegal activities. That encrypted VM should also be stored on encrypted external media such as a flash drive or SD card.


A good rule is to not download stupid shit. If you google “free gta 5 cheats download” and download them, then you’re likely going to install a form of malware including spyware or at the very least bloatware.

## IOT Devices
	
Internet Of Things (IOT) devices are as explained from Google: 
> “pieces of hardware, such as sensors, actuators, gadgets, appliances, or machines, that are programmed for certain applications and can transmit data over the internet or other networks”. 

This essentially means your typical smart device (i.e., smart fridges, smart watches), fitness trackers, smart security systems, and so on. In my opening section “Reality Check”, I threw a lot of shade towards IOT devices. The example that I used was the Amazon Alexa and I pretty much said it’s a corporate spying device that listens to everything you say. Avoiding IOT devices whenever possible is a really great idea not only for your privacy, but your wallet. There definitely are certain IOT devices that offer genuine advantages or convenience, but you need to be aware of the privacy concerns that come with owning them. This definitely isn’t me trying to say that you should never use these devices under any circumstances. Avoiding anything from Google, Facebook, or Amazon is a great starting place. These three companies are all very well known for their tendencies to heavily collect and sell your data. I know most people don’t give a fuck if Amazon knows or collects data based on their shopping habits. Who cares, right? The real privacy invasion is the risk of these devices being used to secretly spy on you. This is way more common from a device manufactured by one of these big name companies due to their high amounts of funding to make this happen. Since these devices are made by giant companies, they know people will buy their shit no matter what the product is. This makes their products even more open for these types of risks, and a bigger target for Law Enforcement to make a deal with these companies to create their own backdoor. Devices owned by these big companies are primarily all closed source proprietary garbage, and again, you’re blindly putting all of your trust into these devices. Bigger companies farm more traffic therefore making user data a valuable selling point for them to profit on, so you bet your ass 50% of the code that run these devices are going to be instructions to collect your data.
	
Buying products from big name companies may be questionable, but what about buying an IOT device from some cheap Chinese company? These devices will probably lack privacy, security, and efficiency due to them being cheap. At least with big name companies you know you’re going to get a product that is relatively secured with strong encryption and the alike. Knock off brand IOT devices are a big thing you want to avoid as their security flaws oppose a severe threat to your network. Hackers often target low hanging fruit to compromise whatever they can so that they can leverage or spread access across a network. These IOT devices are just another node on your network, so if they lack security then you’re putting your entire network at risk just because you bought some shitty $10 WiFi enabled smart light bulb. Do not add devices to your network that are littered with security flaws, that’s very basic security knowledge. That’s like going out of your way to purposely download an application to your computer that is vulnerable to exploits.

## Part II

Part II can be found [here](https://snotknot.github.io/blog/snotknot-security-thread-part-2.html).

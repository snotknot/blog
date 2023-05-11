--
layout: post
title:  "snotknot's security thread (part 2)"
published: true
permalink: "/snotknot-security-thread-part-2.html"
---

## Introduction

Welcome to part II of my security thread. I'm unfortunately pretty late to the party in terms of my planned release date for part II. Summer of 2022 was the plan. It's almost April of 2023 when writing this.

In part I, I introduced you to a thread that was created by a silk road user back in 2014. I hope that you were able to realize the age of that thread. Some things were out of date. Most of that thread is fortunately still relevant today which is why I included it as a resource despite its old age. Upon writing part I, I initially planned on copy/pasting sections of that thread and then "updating" it with todays relevant information. I soon scratched that idea as I realized that most readers would have the common sense to know what information they should or shouldn't trust in terms of how "relevant" the information is today. If you read a thread written in 2014 that says "this type of ram is popular!", I expect you to have the brain capacity to realize that may not apply today due to hardware changes. Whenever I discuss something that was covered in Jolly Roger's thread, I will make sure to update it with what is relevant today.

Within this thread, we will continue to discuss more important things relating to security, privacy, anonymity, OPSEC, and so on. This isn't just a "security" thread if that wasn't made apparent already. Parts I & II are just terminology rundowns or "educational" threads that fill the knowledge gap prerequisite. Part III is when it actually gets fun and we start doing stuff. Trust me, I know everyone just wants to skip to the fun part. It's important to learn what and why before learning how. I encourage that you do not skip along as it may one day come back to haunt you when you're not knowledgeable about a particular subject. Let's say hypothetically that you're doing something illegal on your computer. Your computer is encrypted but you leave your computer powered on and locked overnight. Do you see any issues with this? It's okay if you don't as we'll be covering this in detail throughout the thread (spoiler: RAM attacks). You also didn't pay that close of attention to the Jolly Roger thread as he covered on this topic. If you were to skip along, it's possible that you may have missed the part in the Jolly Roger's thread where he covers why this isn't such a good idea. That one mistake may have you arrested as police have access to a live unencrypted system. Reading the thread would have likely prevented you from making this mistake. This is why you should read everything and in order. Knowledge is power, literally.

I will reiterate from part I: I do NOT support or condone illegal activies. Illegal activities are used as a base example to help demonstrate points for various reasons. That doesn't mean illegal activities are encouraged. In fact, you won't learn how to do anything illegal reading these threads.

## What data does your ISP collect about you?

Your ISP (Internet Service Provider) is the company responsible for providing your internet connection. Registration with an ISP requires personally identifiable information. This should come as no surprise as you have to pay for this service with your personal credit card and provide your address for installation. 

You're instantly providing your ISP with your personal information, and will continue to provide them your data as you use their service. What exactly is this data?

Whenever you make a connection over the internet, your ISP will log the IP address, domain & subdomains that you made the connction to, as well as the date and times that the connections were made to said IP addresses/domains. For example, your ISP knows that you connected to google.com at 4:00pm last Thursday. Your ISP can't see the contents of your session (the data you're sending and receiving), they can only see smaller pieces of metadata. However, your ISP logs more data from connections that are not encrypted.

If you're accessing a website that utilizes HTTPS (the vast majority of websites nowadays), then the data logged by your ISP will be limited as it's an encrypted session. However, if you're connecting to a website that lacks HTTPS and instead is running over HTTP (not encrypted), then your ISP will be able to see everything going on during that session including the contents exhanged between you and the web server. 

Another thing that's useful to know is if you're using HTTP, your ISP can see the entirety of the URL instead of just the IP/domain/subdomain like they would if you used HTTPS. For example, if Google didn't use HTTPS, your ISP would be able to collect every search query you make on Google as Google appends your search query into the URL. For example, if you search "example123" on Google, the URL will look something like:

  https://www.google.com/search?q=example123&oq=example123&aqs=chrome..69i57.2598j0j1&sourceid=chrome&ie=UTF-8

Your ISP would log the entirety of this URL instead of just "google.com" if Google was running over HTTP. This is an HTTPS feature that encrypts the URL contents.

Thankfully this isn't the case as Google utilizes the HTTPS protocol which offers end-to-end encryption to our session. This means the data flow is encrypted, which prevents our ISP from logging the contents as they're not able to read our contents in the first place due to it being encrypted. Yay!!! Or is that something we should celebrate? Does this solve the whole data collection problem? Is encryption the savior we all need? Yes and no. It reduces the problem more than it solves it. The encryption only stops unauthorized people from snooping on the data flow to see what we're up to. Google can still see exactly what we're doing in plaintext as they own the encryption keys to decrypt our requests. 

The point to take away here is to not think your ISP doesn't collect the contents of your session because they "respect your privacy". This is not true. The only reason they don't collect the contents of your browsing sessions is because they're unable to majority of the time thanks to many online services utilizing encryption. This will prevent your ISP from logging the contents of most of your online sessions. If you establish a non-encrypted session to a server, your ISP will log everything including the contents as it will not be encrypted. If you download an image over HTTP or some other unencrypted network protocol, your ISP can retrieve that image just as anyone could who is snooping your data.

These are the main things you need to know about in terms of what data your ISP will collect on you. There's other things I didn't mention but they're common sense when you think about them. For example, your ISP is also able to tell how long you're on a particular website. This is due to the fact that all of your data flow will be routed through your ISP before it reaches the server you're connecting to. Your ISP is the message man who is forwarding all of your data as well as sending it back to you.     

The full comprehensive list of the data collected by your ISP will differ depending on the network protocols that were used throughout your internet activities. Some network protocols utilize encryption while others don't, and some protocols may collect data that others don't. A good rule of thumb that applies to all situations however is everything will be logged for unencrypted connections while less important metadata will be collected for encrypted sessions. 

Data collection exists for many reasons: data sells well, and for bulk collection ("AKA the goverment's euphemism for mass surveillance". ~ Edward Snowden)

## The truth about VPNs 

If you haven't been living under a rock recently then you definitely have had VPN advertisements shoved in your face while browsing social media. These are more common on YouTube as VPN providers will pay bigger YouTube channels to advertise their product. These advertisements will sometimes be misleading as the VPN providers may write nonsense on the script they're paying the YouTuber to read aloud to the camera. Due to this misleading information, it causes a lot of people to be lied to about the capabilities of VPNs.

I want to make it abundantly clear that I have nothing against public figures who accept sponsorship deals with VPN providers. Most probably don't know better and simply read the script. YouTube also demonetizes creators so I understand why people would accept these offers. It's perfectly acceptable to lack the knowledge of VPNs. I believe that most people who accept these sponsorship deals are not intentionally spreading misinformation. The problem aren't the creators accepting the sponsorship deals. The problem is when VPN providers intentionally spread misinformation for marketing reasons to cash out on the profits while lying to millions of people about online privacy. 

VPNs are good for: 
- security (they offer an additional layer of encryption, so if you happen to establish an unencrypted session (HTTP, open Wi-Fi, etc.), it'll prevent the data from being accessible to anyone trying to capture your data including the ISP of the network you're on, however the server you're connected to will obviously be able to see everything in plaintext)
- bypassing certain types of censorship (pirating content without your ISP calling you and complaining, geographical restrictions (i.e., media that's only available in 
certain countries), IP bans, IP-based rate limiting, etc.) 
- getting a new IP address

VPNs are not good for:
- privacy (with VERY small exception)
- anonymity

### The very niche situations where VPNs are "good for privacy"

You're probably spinning in your chair confused saying to yourself "why did this idiot say VPN's aren't good for privacy, meanwhile the next section is "why VPN's are good for privacy"". There are 100x more reasons as to why VPNs are absolutely awful for privacy than why they're good for privacy. This is why privacy is included as one of the things VPNs are not good for.

I guess the only privacy advantage VPNs offer is their capability to mask your IP address to prevent your real IP address from being logged on servers that you don't trust or know the owner of. This could potentially be a privacy concern to some. Someone with your IP address can figure out what ISP you use, the country you live in as well as your precise city (and in some situations your IP will lead to your exact city). This is all publicly available information that anyone can obtain if they have your IP address. There are many freely available resources online such as iplocation.net which will tell you all of this information of any IP address you enter. Some consider this vital information that they don't want anyone obtaining. If this is the case for you, then a VPN is a great choice for you. The vast majority of people do not care about the metadata tied to their IP address. "Oh no, somebody online knows I live in Los Angeles and use comcast!!!". VPNs also help mitigate DDoS attacks as the attacker won't have your real IP address to flood with his botnet, but your VPN IP address instead. 

Another advantage of a malicious actor not having your real IP address is the capability to use it to discover internet-facing devices on your network. This doesn't include devices on your network that are connected to the internet, but rather devices on your network that have ports open to the internet that can be remotely connected to from anywhere in the world (outside of your LAN). Every network is different, but an example may include an IOT device that comes built in with a web interface designed to be remotely accessible to administrators. This is common with many IP cameras. 

This is more of a security problem than a privacy problem as it prevents anyone from obtaining your real IP to scan your network, potentially compromising a public facing device. It doesn't make your privacy any better (the potential private data stored on said scannable systems open to the internet) because if you lack the appropriate security knowledge to where you're incapable of securing an internet facing system from attackers, then a VPN isn't going to be the magic bullet that saves the day.

A VPN may benefit you in one or more of these situations, but it's important to note that the majority of people do not care about most of what was mentioned. We may over analyze these factors as security minded individuals. Most don't.

### Why VPNs are not good for privacy

The big problem today is the issue we have with the bulk collection of data. As we already discussed, our ISP is no exception to this problem as they log a lot of information about our internet activity.

When you're using a VPN, your VPN provider essentially becomes your ISP. You're shifting all of your trust into your VPN provider. You're providing your VPN provider with all of the information that you were once providing your ISP. When you're using a VPN, the only thing that your ISP can see is that you're sending and receiving encrypted data to a VPN server IP address (and remember, your ISP can see that the server belongs to a VPN due to the public information tied to IP addresses). 

VPNs do not solve the issue of data collection as most VPNs also collect your data similar to your ISP.

Many people don't know that VPN's are legally allowed to lie about their data collection habits. Many VPN providers will claim they do not keep logs of your activities for marketing reasons when they likely do. There's been many instances where big name VPN providers were caught red handed keeping logs of their users. These logs were then handed off to law enforcement after they subpoenaed the VPN provider for user logs. 

If you're interested, you can read an example of this with the following link:

  https://www.zdnet.com/article/the-800-lectric-xp-lite-e-bike-is-a-sheer-joy-to-ride/


Many big name VPN providers were caught keeping user logs despite claiming they don't meanwhile they are still performing strong in the VPN industry. Why do you think people continue to use and support these VPN providers even after all of the evidence of them keeping your logs? Why do you think stories such as the one linked above didn't blow up in the media as much as it probably should have? Probably because VPNs aren't as good for privacy as you think. Perhaps there's bigger and better reasons to use VPNs? 

Despite all of the evidence, you also have to use a little bit of common sense. Why would VPN providers NOT log your data??? Data is so valuable in todays world that they would be losing out on a lot of potential profit if they chose to opt out of data collection entirely as most claim to do. What if you're using a VPN who offers cheaper subscriptions than their competitors? How do you think they're making up for that profit? They are probably selling your data. Data collection is even more likely with cheaper VPNs.

### Data Retention Laws

This is one of the most common counter arguments that I see online with people defending VPNs as if they are the saint of the planet. Don't get me wrong, I myself use a VPN and heavily encourage you to do the same. However, a VPN is a VPN. VPNs are not magic.

I'm not a lawyer nor do I know the exact details of these laws so excuse me if I get a few minor details incorrect, but the gist of it is that certain countries have data retention laws that require VPN providers to retain certain types of data for a certain period of time. For example, if you operate a VPN provider in the U.S., you will be required legally by the U.S. government to maintain certain types of data for a certain timeframe. This means that if NordVPN, for example, operated out of the U.S. and then claimed to not keep any logs, they wouldn't be believable as they would be legally required by the government they operate out of to do otherwise.

This is why you see many big name VPN providers operate out of countries such as Switzerland or Panama as these countries do not have required data retention laws that you must abide by if you operate a VPN provider. NordVPN claims to not keep logs and they are based in Panama. This makes their claims of not keeping logs more believable. 

Does NordVPN ACTUALLY log your data? Are they lying? We will never know. The only people who know for sure are the higher ups at NordVPN. What we do now however, is that it's stupid to blindly trust claims without valid reasoning. "Trust us that we don't keep your logs because we aren't legally required to!" isn't a good reason. Some VPNs may not be LEGALLY required to keep your logs, but who said they're not deciding to keep your logs on their own terms despite if they're legally required to or not? We already know that data sells well. Why would they lose out on that profit when they can simply claim they don't keep your logs to attract even more customers and then sell it on the side anyway for extra profit? Claiming to not keep logs = more customers = more data to sell = win win for VPN Provider. You don't have to have a degree in business or mathematics to understand these concepts. Businesses are in it for the money. Guess what a VPN provider is? 

### Conundrum land: "What do I do?!" 

Many people opt into using a VPN as appose to routing their traffic directly through their ISP due to the fact that their ISP will certainly log their data, whereas their VPN may or may not. They weigh the risks and go down the VPN route as it's the safer option of the two. This may make sense for your average person who only slightly cares about privacy or if they don't want to allocate a bunch of time and effort into it. However, for someone who deeply cares about privacy, this isn't the best decision.

We shouldn't have to be placed in a situation where we have to roll the dice and calculate risk management to determine which one of our limited options is the best outcome for our privacy. This is the EXACT issue that we have with online privacy; imprecise solutions that don't guarantee an outcome in which gullible people trust. 

You may be asking yourself, "So then what's the solution? I either give my data to my ISP, or I blindly trust a VPN?". When it comes to security, privacy, anonymity, etc., there is ALWAYS a solution. There's always a way to overcome the problem and regain control. Some are harder than others and some may or may not be legal, but the point still stands; there is always a way to overcome the issue. It just depends on how much you care and how much effort you're willing to put into it to "win" the battle.

### The solution: Creating your own VPN

If you do seriously care about your data potentially being logged, there thankfully are ways for you to regain controll. The solution is to create your own VPN. The idea behind creating your own privately controlled and hosted VPN is so that you have full control over the server powering it and can guarantee that your data is in safe hands and isn't being logged.

Creating a VPN is extremely easy to do. This is a common misconception to many as most people think of the big name VPN providers when they hear the word "VPN". They are big companies, what they're doing must be complex, right? Not so much. To make a VPN provider with thousands of servers that millions of people use is a very hard task indeed. However, you're one person. You only need a server that can handle your traffic flow, nobody else.

The only tricky part to creating your own VPN is the hosting. Are you going to host it at home off a Raspberry Pi? Are you going to turn a shitty PC from 2008 that you have in your closet into a VPN? Are you going to rent a cheap VPS and turn it into a VPN? It's entirely up to you and any method of hosting will work. The only caveat you need to be aware of is that whatever network the VPN will be hosted on will be the VPN's public IP address. For example, if you host your VPN at home on your own hardware, your VPN will be using the same IP address assigned to you by your ISP. If you host a VPN in the cloud, that cloud servers IP address will be your IP address when connected to the VPN. The VPN will not magically spit out a random IP address different from the IP of the network it's running on. That obviously wouldn't make sense. A VPN's job is to encrypt the traffic it receives prior to forwarding it to it's destination and vice versa when recieving. Changing your IP address will only be a perk you can leverage if the VPN is hosted on a separate network. I don't like spending money because I'm cheap so I used a raspberry pi that I got years ago and installed PiVPN onto it (FYI: At the time I'm writing this, raspberry pi's are way more expensive than what they normally go for). It works great aside from when I want a new IP different from the one my ISP assigns.

If you use third party server hosting to host your VPN, you have to also consider the privacy policies of that provider. They too will hypothetically become your ISP just as your paid VPN would because your network traffic will be routed to their server that you're renting. They will be able to see your network traffic in plain text (they own the server you're renting therefore they have access to the contents stored on it). Are you doing anything illegal? If so, is that provider able to be subpoenaed? Even if they claim they cannot, do you really trust that they can't? Do you think they're gonna say no to the feds and risk getting shut down or sued over a $15/month subscriber? It's bad OPSEC regardless of the context to route your network traffic belonging to your illegal activities to a server that you pay for with your real identity (including your ISP). Even if you're not doing anything illegal and going Edward Snowden mode leaking NSA documents, do you care if the provider can read your network traffic? If not, then at that point just use a regular VPN or don't use one at all. At the end of the day, SOMEBODY will be able to read your network traffic unless if you have 100% full control over your private VPN. This means there's no middle man that you're relying on for the uptime of your server (i.e., a hosting provider). You have to own the physical hardware in able to have "full" control.

### The Money Shot (Conclusion) 

I know this entire VPN section has been a rollercoaster thus far. The reason I went off on a tangent is due to the fact that there isn't a simple "yes" or "no" answer to VPN's. It depends entirely on your threat model and needs.

Somebody who doesn't want their network traffic monitored whether if they're participating in sketchy activities or if they are a privacy enthusiast will need to take extra steps to accomodate their needs. In contrast, if you're an average Joe who isn't doing anything sketchy and if you don't care about your privacy, then who the fuck cares? Use a VPN or don't. Use a shitty VPN or use a good VPN. Are you doing illegal activities online and your threat model is the government/law enforcement? Then you shouldn't be using a VPN regardless. 

There are a few reasons why someone may want to use a VPN that they've purchased anonymously. They do this not for anonymity, but for convenience reasons. If you want to go full out paranoid mode and use a VPN anonymously, then the correct method would be to use crypto in which you've obtained anonymously, VERY important, to anonymously purchase a VPN subscription that you will connect to ONLY over Tor.  

The connection chain will look like this: You on a Wi-Fi network that you don't own > Tor > VPN. 

Even when connecting to a VPN over Tor that you've payed for anonymously, you have to ask "Am I gaining a genuine advantage?". That's a legitimate question. Are you? 

If you're accessing the clearnet, having a VPN as your end node rather than a tor exit node can often be a lifesaver since websites can tell that you're using Tor. If you're on Google with Tor as your end node, Google will see the IP address of the Tor exit node and assume that you're a bot who's up to no good and will put you in endless captcha land. This can be really annoying if you're simply to browse Google. Some websites may also rate limit you or not allow you to connect to them at all if you're using Tor. These are all reasons as to why it may be good to have a VPN as your end node. 

I recommend watching a video made by a prior Darknet vendor who sold moonshine on the dark web. He often gives OpSec lessons on his YouTube channel and most of his journey is documented not only on his personal channel, but his Defcon conference. 

No Logs VPNs fail for Darknet OpSec - Deep Dot Darknet:

  https://www.youtube.com/watch?v=6arTTIcE4LA

Tor: Darknet OpSec By a Veteran Darknet Vendor & the Hackers Mentality (Defcon 30):

  https://www.youtube.com/watch?v=NGiUhjuB22Y&t

He goes into detail on why it's not really a good idea to combine a VPN with Tor when your threat model is the government trying to arrest you. His OpSec was so incredible that the feds had to break the law to catch him. He never used a VPN. How did he do it? By not being complacent and understanding each layer of his OpSec foundation. The Defcon conference isn't really about VPN's but more of an interesting watch if you're into OpSec.

## Crypto

Cryptocurrency is something you need to be aware of to understand security, privacy, and anonymity. It'll come up at one point or another and you'll benefit from having knowledge on it. This will be more apparent if you're interested in anonymity and use the Dark web a lot. You'll see it plenty there. This will be by no means a "get your PHD in crypto" section. 

The main thing you need to understand is that most cryptocurrencies are not anonymous by default unless if used properly. Bitcoin is a great example and is the one many immediately think of as it's the staple of crypto. All Bitcoin transactions are publicly available for anyone to see, which could be breadcrumbs to help identify patterns that could ultimately lead to your identity being unmasked. We'll cover more on this later, but for now we'll save this for later.

I first recommend that you learn about what crypto is as a whole prior to learning about individual cryptocurrencies (bitcoin, etc.). I'll link some videos to get you started. Feel free to do your own research to fill in any voids not covered in the videos.

How Cryptocurrency ACTUALLY works:

  https://www.youtube.com/watch?v=rYQgy8QDEBI

Explain Crypto To COMPLETE Beginners: My Guide!!: 

  https://www.youtube.com/watch?v=VYWc9dFqROI&t

Do you understand what crypto is yet? Great. We can move on to individual cryptocurrencies such as bitcoin, ethereum, monero, etc.

There's hundreds of different cryptocurrencies. Don't let that scare you. There's only a handful of big ones, many are shitcoins that people try to create (anyone can create a cryptocurrency). I will leave it up to you to learn about the ones you're interested in. You need to remember that although they all share one thing in common: they are all cryptocurrencies, they are also different in terms of how they function. Essentially, a coin gains traction, its value increases, and eventually it becomes mainstream to the point where services we all know and love offer them as a method of payment. Sure, you may own a lot of "Speedy Coin"!! (made that up) But nobody knows what the fuck speedy coin is and it isn't a valued crypto. Nobody is going to accept payment in that coin. Don't pay attention to coins that aren't popular, unless you're trying to make your own or promote/support a smaller coin, etc.  

Bitcoin isn't very convenient for privacy by default, whereas a coin such as Monero is designed to be more private. These are things that are important to know. Crypto can have a huge learning curve so don't worry if you walk away without learning much of value. You'll get it over time.

Fortunately for you, you're just learning the basics. For privacy, anonymity, and OPSEC, the main thing that you need to know is that many cryptocurrencies have a public block chain that logs every transaction tied to that crytocurrency's wallet that anyone at anytime can view. Think of a Bitcoin wallet as your bank account statement being publicly accessible. Anyone can see the amount of bitcoin that you're sending and receiving, as well as the bitcoin addresses you're sending and receiving from. Bitcoin is the best example of this and you will likely get caught if you buy illegal things with bitcoin (or tie them to your illegal activities) without taking the proper steps to obfuscate the payments or if you're using coins that you didn't obtain anonymously.

Bitcoin mixers are quite common and is what many people use to help obfuscate their bitcoin transactions. Think of a bitcoin mixer as a hat. You will "put your bitcoin into a hat" with other peoples bitcoin. The hat will then shake itself and mix the coins. The mixer will randomly spit the bitcoin into random "pools" that will then be sent back to your dedicated "mixing" bitcoin address. You should theoritically have a dedicated bitcoin address that you use solely for retrieving mixed bitcoin for obvious OpSec reasons. 

Getting your first batch of crypto is the hard part. I know it's tempting to simply register at an exhange such as Coinbase and then buy Bitcoin using your Credit Card, but that isn't a good idea for VERY obvious reasons. These exchanges also require you to verify your ID, BTW.

How do you obtain your first batch of crypto anonymously? There are many ways. Just like everything in life, there are legal and not so legal ways of doing it. The legal ways could be setting up a miner and then routing it through Tor, you can earn the crypto by doing work for someone in return for crypto, or you can even utilize websites online that allow you to meet with people local to you to exhange bitcoin for cash (I personally wouldn't recommend but you do you). The not so legal ways may include creating crypto miner malware, or malware that simply steals bitcoin address information. There's even malware out there disguised as Crypto wallet apps (or similar) that phishes you into giving them crypto or your wallet information. The list goes on and on; extortion, you name it (not encouraged, obviously).

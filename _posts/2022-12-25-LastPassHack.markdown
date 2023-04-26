---
layout: post
title:  "LastPass Hack: Why you shouldn't use cloud-based password managers"
published: true
permalink: "/lastpass-databreach"
---

Imagine this. It's Christmas Morning. After John spends time with his family, he goes into his room and logs onto his computer. As of recently, John has had his entire online presence hacked due to him using the same password for all of his accounts. 

John has had enough. He's tired of creating unique passwords for each individual account. John has been tighening up his security practices lately and decides that he wants to create an account over at the one and only password manager: LastPass. 

After brainstorming what he could make his master password to his LastPass vault, he finally comes to the conclusion that his password will be "christmas123". John immediately feels a sense of hope inside as his faith in his security is restored... just for it to be ruined as a hacker cracks his master password due to LastPass being hacked.

## LastPass Hacked

Password managers have been increasing in popularity as of recently. Many companies are actually requiring them to increase employee security. With the most popular password manager currently being LastPass, there's a great chance the company is using LastPass for their password architecture. This will be important to know later.

LastPass has a track record of being hacked as they mainly have a data breach occur yearly. Their data breaches normally aren't significant enough to the point where anyone cares. That has changed as of a few days ago.

A LastPass developer account had been breached a few months ago. I'm assuming this was due to a spear phishing attack. I didn't do that much research so don't quote me on that. LastPass put out a public statement announcing that the breach isn't a big deal and everyone went on their own ways. 

On December 22, 2022, LastPass put out an update that the breach was indeed a lot more damaging than they initially thought.

Link to LastPass's statement:
https://blog.lastpass.com/2022/12/notice-of-recent-security-incident/

The statement says one of their backup servers had been compromised a while back and they are only now realizing the severity of the breach. They go on to explain that the compromised server is separate from their main production servers, meaning the hackers only obtained whatever was on that particular backup cloud server. 

The data stored on the servers were encrypted (as you'd hope), but hackers were able to obtain the keys from the developers to decrypt the storage volumes containing the sensitive data.

> To date, we have determined that once the cloud storage access key and dual storage container decryption keys were obtained, the threat actor copied information from backup that contained basic customer account information and related metadata including company names, end-user names, billing addresses, email addresses, telephone numbers, and the IP addresses from which customers were accessing the LastPass service.  

I love the damage control attempt with the "basic customer account information" line. Ahh yes. "Basic" information such as names, phone numbers, and addresses. 

You can see from the quoted paragraph that they state important customer data had been leaked.

It's pretty ironic when the company who's bread and butter is to keep your data safe has as a data breach.

The encrypted storage containers, once decrypted, also revealed some customer vault data.

> The threat actor was also able to copy a backup of customer vault data from the encrypted storage container which is stored in a proprietary binary format that contains both unencrypted data, such as website URLs, as well as fully-encrypted sensitive fields such as website usernames and passwords, secure notes, and form-filled data. These encrypted fields remain secured with 256-bit AES encryption and can only be decrypted with a unique encryption key derived from each user’s master password using our Zero Knowledge architecture. As a reminder, the master password is never known to LastPass and is not stored or maintained by LastPass. The encryption and decryption of data is performed only on the local LastPass client.

Password managers are a goldmine for hackers as they obviously contain the passwords of an individual(s). Obtaining access to a single password vault would be valuable for a hacker, or even better, multiple password vaults which is exactly what the hacker who compromised LastPass accomplished. In case you're new to password managers or if you don't know how they work, each user has their own respected password vault that contains their passwords and are encrypted with their personal master password.

It's fortunately not as scary as it seems. LastPass's writeup specified that the hacker only obtained access to encrypted user vault data. They didn't walk away with the user vault data for free unencrypted. The only way they'd be able to access any of that data would be to crack the master password for each respected user vault. This means if you have a bad password that it's likely to be cracked.

I like to imagine the hacker who breached the LastPass backup server frantically purshasing a shit ton of mining cards off the internet to create a powerfull cracking rig to achieve the highest hash rates.

Even the hashes of these password vaults will sell for a high price on the darknet. If the hacker (or hackers) who initially breached the data can't manage to crack any of the hashes, then there obviously will be people out there who will. 

## What LastPass users have to worry about 

From LastPass's statement: 

> The threat actor may attempt to use brute force to guess your master password and decrypt the copies of vault data they took. Because of the hashing and encryption methods we use to protect our customers, it would be extremely difficult to attempt to brute force guess master passwords for those customers who follow our password best practices. We routinely test the latest password cracking technologies against our algorithms to keep pace with and improve upon our cryptographic controls.  
> 
> The threat actor may also target customers with phishing attacks, credential stuffing, or other brute force attacks against online accounts associated with your LastPass vault. In order to protect yourself against social engineering or phishing attacks, it is important to know that LastPass will never call, email, or text you and ask you to click on a link to verify your personal information. Other than when signing into your vault from a LastPass client, LastPass will never ask you for your master password. 

There are a few things you need to be aware about before deciding if you want to use LastPass or not. Firstly, this hack has very little impact on your password vault if you have a strong master password. LastPass requires 12 characters minimum for master passwords, meaning all master passwords will be relatively secure by default. Don't let that trick you though. It's certainly possible to create a very shitty 12 character password. 

Many people don't care about the specifics of the LastPass breach. The hack alone is enough for many customers to quit using the service. The reason is obvious. Your typical security minded individual will have alarm bells go off in their minds telling them to immediately stop using a service that has as many (and as severe as this one) data breaches.

If you want to play it safe and go the extra mile to stop using LastPass (or any other Cloud based password manager (i.e., 1Password)), then make sure to read the next section where I go over alternatives.

It's ultimately up to you if you want to continue being their customer or not. If you want to trade the convenience of having LastPass store your passwords for you in the cloud for the potential security risks that come with it, then that decision is yours.

## Alternatives and why you should consider them

Online cloud-based password managers such as LastPass, Dashlane, etc. offer many security risks. These password managers store your password vaults in the cloud. This makes your entire password vault remotely available for anyone to potentially acccess. This means you are storing an important asset to hackers (your passwords) in the cloud, which then become a potential target of theirs.

 Most of these password managers are also closed-source. This means their software is proprietary and the source code is not available to the public for you to view and analyze. It's likely that a lot of software you use is proprietary, but using proprietary software for something as critically important as a password manager isn't a great idea and is something that you should consider avoiding.

Why does this matter? Why should you use something better like a self hosted open-soured password manager? Not only are your passwords not open to the internet (unless you allow them to be), but you can rest assure knowing the software is doing exactly as advertised due to the source code being public. You're 100% certain what code is running, when, how well it's running, and so on. You can modify it too if need be. Open-sourced projects and why they're great is a conversation for another day, but we will be focusing on the basics for the sake of password managers.

When you run software with proprietary source code (closed-source), you don't have a way of knowing what code is running on your system. How well is the code written? How secure is it? Do they **actually** follow their "zero knowledge" policy where they claim to abide by security practices such as not storing your master password? You can read more about that here: https://www.lastpass.com/security/zero-knowledge-security. These are all things you have no way of knowing for sure with closed-source proprietary software. It's all "he said, she said". The goal with open-sourced software is to not be gullible. You as the user should have the luxury of knowing exactly what is happening with software on your computer without blindly trusting an entity. 

The final issue we'll be discussing with closed-source password managers, which are the same issues other closed-source software have as well, is trusting the development team responsible for maintaining the software's security. These are the only people who have access to the source code. You're trusting them to actively find and patch security vulnerabilities in the software that you are an end user of. This is the definition of security by obscurity. With open-sourced software, there are millions of people who can analyze the source code, find these vulnerabilities and report them to get them patched. Many of these people are also way more experienced than the average team responsible for maintaining most closed-source software. This indeed means there are more bad actors who can analyze the source code to develop exploits, but there are way more good guys actively finding and patching these vulnerabilities before the bad guys can discover them.

Good alternatives that are open-sourced would be something like Bitwarden or KeePassXC. Bitwarden is a little more advanced and is more like the password manager you're probably used to. Bitwarden is great and offers a web vault and everything you need to self host, whether it be locally or in the cloud. Bitwarden is also categorized as "freemium" software. Meaning it does have features for free and some you can pay for.

 KeePassXC is way simpler but still a good option. KeePassXC runs off an encrypted file locally on your device that acts as your vault. This is great if you want to store passwords (or anything else) in an encrypted manner on your device for a few accounts you only use on that device, but is really annoying for everyday accounts that you want to access on multiple devices. KeePassXC also won't sync your vault between your devices by default as it's just a file on your computer. KeePassXC does recommend options to sync with Dropbox, Google Drive, and so on. I haven't used this method so I don't know for sure, but I'd have to imagine this would cause issues at times.  

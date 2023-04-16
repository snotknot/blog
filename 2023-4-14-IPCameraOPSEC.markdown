--
layout: post
title: "Avenging an Elderly Man who has IP Cameras in his house" 
published: true
permalink: "/IP-Camera-OpSec.html"
---

I posted a blog exactly one year ago from today going into detail on why you should never use an IP camera. Although there are variants of IP cameras that are more secure than others, I was mainly talking about IP cameras that have a built in web server in which the camera will be streamed to. These web servers will be hosted on a port in which will be open to the internet, allowing anyone from anywhere in the world to connect to and view the video feed. I cover more on how these cameras can be discovered by strangers in my original blog post covering IP cameras.

OSINT (Open-Source Intelligence) is the process of using information publicly available on the internet to help with the analysis or intelligence phase of an investigation. An example may include tracking a missing person down using information pubicly available on the internet. Where was the person last seen? Who were they last seen with? Can this information be found online such as their social medias? Who are they friends with?

A big part of OSINT investigations is using the very little information you have at your disposal to ultimately end up discovering everything. An example may include finding the exact location a picture was taken, or finding out everything about an individual when the only thing you have to start off with is a picture of them or a name. There's actually a game called GeoGuessr, where you are placed at a random location on Google Maps and you have to pinpoint where you are in the world. I'm a really big fan of this game and play it religiously. It's fun to scour Google Maps finding clues on where you're located. It eventually becomes easy and you end up knowing exactly what country you're in within 3 seconds. This game is great for training your brain to look for region specific clues that can aid in locating where you are. There are people in the GeoGuessr community who use their geography skills for good and will help find the location that sentimental fan submitted photos were taken. Rainbolt is a great example of one of these people. Someone else who I want to mention is GeoWizard. GeoWizard has a series on his YouTube channel where he will track down the exact location, down to the exact coordinate, where a picture was taken. These photos will be submitted by fans of his YouTube channel and are often taken on vacation.

In my original blog post about IP cameras, I mentioned that it's been a hobby of mine for years to locate these cameras. However, I never explained why. Do I just stalk people through their cameras? Do I hack into them? Why is it a hobby of mine to discover these publicly available IP cameras? There are various reasons, but the main reason is that I find it interesting. Plain and simple. It's cool to view these video feeds as it gives you a preview of things around the world as cameras often have a dedicated purpose; to watch something intesting. Since I enjoy playing GeoGuessr and performing detective OSINT work, it's also fun to locate the exact location of an IP camera that I discover. I also find it enjoyable to locate other devices on the network in which the IP camera is connected to. Are there other IP cameras on the network aside from the camera that I originally found by Google Dorking? It's all one big playground for me and I find it extremely fun as it combines my interests into one big activity; security, privacy, anonymity, and hacking. "Anonymity" is used lightly as I definitely do not take steps to be anonymous whenenever I'm having fun with these cameras.The most I do for my OpSec is use a VPN. You might be thinking, "oh wow, "privacy" guy who writes security/privacy blogs doesn't even have good OpSec himself!". Hear me out... it's not as bad as you may think. First of all, what I do is not illegal. Accessing publicly available cameras on the internet isn't a crime. Second of all, even if it was illegal, the FBI has more important things to be doing than catching some random guy who's having fun tinkering with IP cameras. It literally took the FBI a year and a half to catch Pompompurin, a hacker who's OpSec was so comically bad that it's actually meme material. 

### The story of an Elderly man who purchased IP cameras to put in his home (Tracking Down IP Cameras) 

Tracking down the exact location of IP cameras can sometimes be tricky as the video feed will often be lackluster of details. An example may include a camera inside of a room without any clues. At that point, the only thing you can really do is lookup the location of the IP to get a city (in which may not even be accurate), and then search online for pictures inside of buildings in the area to find a match of the room. That's too much work for me and isn't something I do. I prefer cameras that are outside. This makes it possible to use Google Maps street and satellite view.

I fortunately rarely find cameras located inside of homes. Most cameras are located outside watching god only knows what. You will be shocked with how many cameras I discover that make me verbally shout "what the actual fuck is this camera even watching?". However, a few days ago I discovered a camera that that was located inside of an Elderly man's home. The camera was on a table in his living room that pointed into his kitchen where his computer is located. This camera allowed anyone to creepily stalk him as he used his computer. It was heartbreaking to know that he was sucked into the trap of purchasing an IP camera with a built in web server to then put it in his home. In case you're not following along: do not put a camera anywhere you expect privacy. 

## Anime Revenge Arc

It was made apparent that this unfortanate man did not have God in his favor. He committed the two worse sins known to man: he purchased an IP camera, and he placed it in his home.

Once I noticed the situation of the camera I just dorked being located in a home of an innocent elderly man, I couldn't help but feel bad. I made it my mission to inform him that his camera was public to the internet with the hopes that he'd get rid of them. 

CBC News actually has a video where they did exactly this. The difference was they reported it to the homeowners in person. I'm doing it digitally. You can watch the video here:

  https://www.youtube.com/watch?v=-P0rSnt2HSU

# OSINT

Having the knowledge of how web servers function and how to navigate around their contents in your browser is useful to have for the purposes of simply seeing what you can locate. It also helps to have knowledge on  domains/subdomains, directories/subdirectories, ports, and just the overall URL.

Below is the URL of the camera that I dorked:

  http://<IP Redacted>:88/ViewerFrame?Mode=Motion&Language=7

The first thing that I noticed is that the camera is running on port 88. This is interesting for two reasons. The first reason is that the default HTTP port is 80. This means that the port was likely manually changed by the person who installed and configured the camera. The second reason is that this likely means there are other cameras on the network. Whenever you dork a camera that has a dedicated port in the URL, that likely means that there are other cameras on other ports too. This is especially apparent if the port isn't 80. This is because, as already mentioned, the default HTTP port is 80. This means that if you have multiple cameras, they cannot all run on the default assigned port 80. You'd have to change them to something else so that they're not conflicting. 

At this point I start to do what I like to call "port plugging". This is when you open another tab in your browser, paste the URL of the camera, and then increment/decrement the port number by 1 every time to find other cameras that are on different ports. I should probably create a script to automate this process, but I've gotten pretty fast at it by this point. Also: No, the solution unfortunately isn't to scan all ports with nmap.

Pro tip: When "port plugging", make sure to get rid of the everything after the port number when you copy/paste the URL into new tabs. You only need to call the port. If there's a camera on that port, it'll send your browser the data required and will autofill it into your URL bar for you.

I will typically port plug 10 ports up and down from the originally dorked port number. It works 99% of the time as the ports will all typically be in the same range.

Port plugging allowed me to discover a handful of other cameras; one watching his kitchen, one outside, one watching his front door, and one in his garage. There were two more as well, but they were password protected and I never attempted bruteforcing.

What I discover next is insane and you're not going to believe me. Remember how I mentioned earlier that his computer is in his kitchen? Remember how I also said he had a camera watching his kitchen? The camera watching the kitchen has the capability to zoom onto his computer screen. Yes. You read that correctly. I can see everything on his computer screen as he uses his computer. There was a light hanging from the ceiling that was annoyingly blocking the screen, but I could still see a good portion of his screen. Seriously though, the light was fucking annoying. The camera kept autofocusing on it.

I was lucky enough to discover that the camera could read his computer screen because if it wasn't for that, it's very likely that I wouldn't have been able to track him down (spoiler alert). Seeing his computer screen was obviously a big plus. This allowed me to see his name and address when he placed orders on Amazon, or did other things such as paying bills. If anyone was watching the feed at the same time I was, then they also walked away with his credit card information and other personal information.

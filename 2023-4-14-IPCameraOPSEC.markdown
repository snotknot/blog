---
layout: post
title: "Avenging an Elderly Man who has IP Cameras in his house" 
published: true
permalink: "/IP-Camera-OpSec.html"
---

I posted a blog exactly one year ago from today going into detail on why you should never use an IP camera. Although there are variants of IP cameras that are more secure than others, I was mainly talking about IP cameras that have a built in web server in which the camera will be streamed to. These web servers will be hosted on a port in which will be open to the internet, allowing anyone from anywhere in the world to connect to and view the video feed. I cover more on how these cameras can be discovered by strangers in my original blog post covering IP cameras.

OSINT (Open-Source Intelligence) is the process of using information publicly available on the internet to help with the analysis or intelligence phase of an investigation. An example may include tracking a missing person down using information pubicly available on the internet. Where was the person last seen? Who were they last seen with? Can this information be found online such as their social medias? Who are they friends with? Many people these days make every detail public. Where was Becky last seen? I don't fucking know, check her snap story. That'll answer your question.

A big part of OSINT investigations is using the very little information you have at your disposal to ultimately end up discovering the full picture. An example may include finding the exact location a picture was taken, or finding out everything about an individual when the only thing you have to start off with is a picture of them or a name. There's actually a game called GeoGuessr, where you are placed at a random location on Google Maps and you have to pinpoint where you are in the world. I'm a really big fan of this game and play it religiously. It's fun to scour Google Maps finding clues on where you're located. It eventually becomes easy and you end up knowing exactly what country you're in within 3 seconds. This game is great for training your brain to look for region specific clues that can aid in locating where you are. There are people in the GeoGuessr community who use their geography skills for good and will help find the location that sentimental fan submitted photos were taken. Rainbolt is a great example of one of these people. Someone else who I want to mention is GeoWizard. GeoWizard has a series on his YouTube channel where he will track down the exact location, down to the exact coordinate, where a picture was taken. These photos will be submitted by fans of his YouTube channel and are often taken on vacation.

In my original blog post about IP cameras, I mentioned that it's been a hobby of mine for years to locate these cameras. However, I never explained why. Do I just stalk people through their cameras? Do I hack into them? Why is it a hobby of mine to discover these publicly available IP cameras? There are various reasons, but the main reason is that I find it interesting. Plain and simple. It's cool to view these video feeds as it gives you a preview of things around the world as cameras often have a dedicated purpose; to watch something of importance. Since I enjoy playing GeoGuessr and performing detective OSINT work, it's also fun to locate the exact location of an IP camera that I discover. 

Here's an example of an IP camera that I located pretty quickly.

IP Camera:

[http://66.84.101.99/view/view.shtml?id=4422&imagepath=%2Fmjpg%2Fvideo.mjpg&size=1](http://66.84.101.99/view/view.shtml?id=4422&imagepath=%2Fmjpg%2Fvideo.mjpg&size=1)

The location on Google Maps: 
[https://www.google.com/maps/@43.3709632,-83.580877,3a,90y,336.46h,91.22t/data=!3m9!1e1!3m7!1s5xb5upVsaHQik1SSuE_-WA!2e0!7i16384!8i8192!9m2!1b1!2i31?entry=ttu](https:// www.google.com/maps/@43.3709632,-83.580877,3a,90y,336.46h,91.22t/data=!3m9!1e1!3m7!1s5xb5upVsaHQik1SSuE_-WA!2e0!7i16384!8i8192!9m2!1b1!2i31?entry=ttu)


You can see that the camera is mounted to the City Hall building. Locating this camera came with a bit of luck but ultimately was easy and only took a few minutes. How did I do it?

The first thing I do in almost every situation is lookup the metadata tied to the public IP address of the network the camera is running on. In this case, the IP is 66.84.101.99. The website I normally use is [iplocation.net](iplocation.net). There are various other resources that replicate the same thing. The city reported from the IP address is Sterling Heights. Keep in mind that this may change with time.

In most cases, the city reported from IP addresses will be a nearby city, and sometimes will be the exact city. In some situations, however, the IP address will report a city that is very far away. That is exactly what happened here. The actual city where the camera is located is Vassar, Michigan. The IP address of the network the camera is running on reports Sterling Heights, Michigan. The distance between these two cities is almost 80 miles and takes roughly an hour and a half to drive.


I never take the city reported at face value as it's incorrect 90% of the time, however I started searching Sterling Heights on Google Maps Map view for a bridge that crosses a river with two buildings on the left & right as you exit the bridge. You start to figure out how areas will look on a map when you start doing this a lot. For example, I knew the camera I dorked was mounted on a building to the east of the bridge. This was something to look out for while scouring Google Maps for bridges in the city, and is something that helped elimate bridges relatively quickly. You can tell within milliseconds if the bridge isn't the correct bridge; if the body of water is too large for the location, if the bridge is too long/short, and so on. Nothing aligned with the cameras POV so I stopped searching in Sterling Heights.

My next move at this point would typically be to start scouring bridges in neighboring cities/suburbs. However, I noticed that the company "Air Advantage LLC" was listed for the ISP of the cameras IP on iplocation.net. 

The ISP listed for IP addresses will typically be, well... the ISP of the IP Address. This would include Spectrum, Comcast, and so forth (in the US). However, if the IP address belongs to a network that is owned by a large organization (i.e., Universities), it is common for that University to be listed for the ISP. For example, I've dorked IP cameras belonging to the University of Arizona dozens of times. The ISP always lists "University of Arizona" when searched on sites such as iplocation.net.

The reason this is important is because I thought maybe the camera was attached to a network owned by a small company. If that were to be true, I could just Google the name of the company and find their address online allowing me to locate the camera. For example, it took me 5 seconds to physically locate the camera that was attached to the Univesity of Arizona's network as the ISP was literally "University of Arizona". Hmmmm, I wonder where the camera is???

I was sad to find out upon Googling "Air Advantage LLC" that it wasn't what I expecting. Instead, Air Advantage LLC is just a non-reputable shitty off brand ISP that I've never heard of.

Just to be safe, I took 5 seconds to look at the address listed for "Air Advantage LLC" on Google to make sure that wasn't where the camera was located. It was easy enough as there wasn't even a river or a bridge anywhere near the building.

At this point, I knew the camera had to be close to the headquarters of this shitty ISP. I also knew at this point that I probably wasted my time searching in Sterling Heights. How do I know this? Although I don't know for sure, I can assume with high confidence that "Air Advantage LLC" is an ISP who's network/infrastructure leeches off of the bigger name brand ISP's (i.e., Spectrum, Comcast, etc.).

Here in the USA, we have 4 main cellular providers: AT&T, Sprint, Verizon, and T-Mobile. These are the 4 MNO's, or the "Mobile Network Operators" who are responsible for the cellular networks in the USA. These 4 companies own and maintain the equipment such as the cell towers that power the cellular networks. 

Here in the USA, we also have MVNO's, or "Mobile Virtual Network Operators" who pay the MNO's (who own and maintain the cellular networks) a fee to use the MNO's network to host their own cellular provider. That's what a MVNO is, and an example of MVNO's here in the USA are: Tracfone, Cricket Wireless, Boost Mobile, and so on. 

Why does this matter? Well, if you buy a phone plan through Cricket Wireless, you're using AT&T's cellular network. Why? Because Cricket Wireless piggy backs off of AT&T's network. 

What this ultimately means is that the ISP of the camera is an off brand ISP who's network probably piggy backs off name brand ISP's such as Comcast or Spectrum. We're essentially working with an MVNO equivalent of an ISP. This would explain why the city isn't even remotely accurate as the IP range belongs to the ISP that "Air Advantage LLC" is leeching off.

I can no longer rely on on the geographical data reported from the IP address. Instead, I started searching for bridges in the area of the off brand ISP. This is due to the fact that customers of off brand ISP's will typically be local to said off brand ISP (off brand ISP's don't have the money/infrastructure to spread across a large geographical range).

If you go on Google Maps and go South of the address listed for "Air Advantage LLC", you will find a river named "Cass River". I started following the river west while looking at the bridges, until I eventually starting following the river east. This is when I found the correct bridge. 

Locating this camera may sound complex since I explained my thought process in great detail, don't let that confuse you. It took less than 15 minutes. Don't forget that this happens in the brain subconsciously.

This camera in particular was very easy to find. The camera was outside, had a good quality feed, and had things that were easy to spot on a map such as a bridge crossing over a river. It unfortunately took 10% more brain power to locate the camera due to the fact that the city of Vassar (of all people) are for whatever reason using a shitty off brand ISP for the internet of their city hall.

I also find it enjoyable to locate other devices on the network in which the IP camera is connected to. Are there other IP cameras on the network aside from the camera that I originally found by Google Dorking? It's all one big playground for me and I find it extremely fun as it combines my interests into one big activity; security, privacy, anonymity, and hacking. "Anonymity" is used lightly as I definitely do not take steps to be anonymous whenenever I'm having fun with these cameras. The most I do for my OpSec is use a VPN. You might be thinking, "oh wow, "privacy" guy who writes security/privacy blogs doesn't even have good OpSec himself!". Hear me out... it's not as bad as you may think. First of all, what I do is not illegal. Accessing publicly available cameras on the internet isn't a crime. Second of all, even if it was illegal, the FBI has more important things to be doing than catching some random guy who's having fun tinkering with IP cameras. It literally took the FBI a year and a half to catch Pompompurin, a hacker who committed high profile attacks (unlike what I do) who's OpSec was so comically bad that it's actually meme material. 

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

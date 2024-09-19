+++
title = 'My 72-Hour BSD Bender: From Network Nightmare to Unix Nirvana'
date = 2024-09-18T14:50:55+03:00
draft = false
tags = ["FreeBSD", "OpenBSD", "networking", "system administration", "troubleshooting", "PF firewall", "X11", "GUI", "partitioning"]
categories = ["BSD", "Networking", "System Administration"]
+++

# FreeBSD, OpenBSD, and Me: A Tragicomedy in Three Acts

Ladies, gentlemen, and Unix enthusiasts of all stripes, gather 'round for a tale of network woe, BSD brilliance, and the kind of sleep deprivation usually reserved for new parents and cryptocurrency day traders. I present to you my 72-hour descent into the wonderful, maddening world of BSD.

## Act I: The Blinking Light of Doom

Our story begins with a blinking light. Not just any light, mind you, but the PON light on my ISP's router. For the uninitiated, PON stands for Passive Optical Network, but in that moment, it might as well have stood for "Panic! Outage! Noooooo!"

Little did I know that this innocuous blinking would lead me on a journey through the very bowels of network configuration, Unix-like operating systems, and my own sanity. Spoiler alert: only two of those three made it out intact.

## Act II: FreeBSD - The Siren's Call

Enter our hero: a plucky Beelink SER5 Pro, armed with an AMD 5600h processor, 16GB of RAM, and a 500GB Intel SSD. Oh, and a fresh install of FreeBSD 14.1-RELEASE. It was supposed to be a simple home server. It became my white whale.

With the confidence of someone who once successfully set up a Wi-Fi password, I decided that clearly, the solution to my network woes was to turn this innocent machine into a router. What could possibly go wrong?

Everything. Everything could go wrong.

### The Config File Cacophony

Over the next 24 hours, I engaged in a Config File Cacophony that would make even the most hardened sysadmin weep:

1. I played DNS roulette, flinging nameservers into `/etc/resolv.conf` like a deranged bingo caller. 1.1.1.1! 8.8.8.8! 192.168.1.1! BINGO!

2. I turned `/etc/rc.conf` into my personal diary of despair, enabling and disabling services with the fervor of a toddler with a light switch.

3. I danced the routing table tango, my partner a particularly uncooperative `netstat -rn`. We moved together with all the grace of a giraffe on roller skates.

4. The PF firewall became my frenemy. We'd spend hours together, carefully crafting rules, only for it to unexpectedly block my access. Et tu, PF?

5. I restarted so many services, I'm pretty sure my computer developed PTSD. "Oh God, not the networking stack again!" it would whimper.

6. In a moment of desperation, I even adjusted the MTU. Because when all else fails, start messing with packet sizes. That's in the sysadmin handbook, right? Right??

### The X11 Xanity Xoss

Just when I thought things couldn't get any weirder, my FreeBSD box decided to cosplay as a raver, restarting itself with the enthusiasm of a caffeinated squirrel. The culprit? X11, apparently throwing a tantrum worthy of a three-year-old denied ice cream because it couldn't find a monitor.

The solution was both elegant and brutal: OUT CAME THE AXE. Goodbye MATE, farewell SLIM, sayonara X11. My system was going on a GUI diet whether it liked it or not. And you know what? The restarts stopped. Apparently, my router didn't need to be prettier than me. Who knew?

## Act III: OpenBSD - The Light at the End of the Tunnel (Probably an Oncoming Train)

As hour 48 approached and my caffeine-to-blood ratio reached levels hitherto unknown to medical science, a miracle occurred. My ISP, in their infinite wisdom, fixed the port issue. Suddenly, I had internet again!

Did I sleep? Did I call my worried family and friends to let them know I was alive? Of course not! I decided that now was the perfect time to install OpenBSD. Because apparently, I hadn't suffered enough.

### The Great Partition Kerfuffle

In my sleep-deprived brilliance, I managed to give OpenBSD a root partition that would make a USB stick blush. 1GB. I'd seen bigger TikToks.

After several hours of trying to convince my system that it was indeed larger on the inside (Time Lord technology, anyone?), I admitted defeat. With a heavy heart and heavier eyelids, I began the reinstallation process. This time, with partitions big enough to actually, you know, do stuff.

## Epilogue: The BSD Awakening

As the sun rose on day three, I emerged from my tech cave, blinking in the harsh light of day. My network was fixed, my FreeBSD box was GUI-free and stable, and my OpenBSD system was partitioned like a rational person would partition it.

Was it worth it? Ask me after I've slept for a week.

## Lessons Learned (Besides "Sleep Is Important"):

1. When in doubt, read the man pages. When still in doubt, read them again.
2. X11 is like a stubborn stain. Sometimes, you just have to throw the whole shirt out.
3. Partition sizes matter. Think "apartment," not "broom closet."
4. The BSD community is amazing, helpful, and probably worried about my mental health now.
5. Coffee is a food group. No, I will not be taking questions at this time.

## What's Next?

Well, after a long nap and possibly a psych evaluation, I plan to dive deeper into BSD. There's a whole world of Unix goodness out there, and I've only scratched the surface. Plus, I hear DragonflyBSD is lovely this time of year.

To all my fellow BSD adventurers, remember: In the darkest hours of debugging, when all hope seems lost, and your system is being less cooperative than a cat at bath time, take a deep breath and remember - it could be worse. You could be running Windows Vista.

Now, if you'll excuse me, I have a date with a pillow. A long, long date.

Happy BSDebating, everyone!

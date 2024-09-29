---
layout: post
title:  "How GameMaker Server Was Born"
date:   2024-09-29 12:50:59 +0200
categories: history
---

Dear readers,

GameMaker Server recently had its 13th anniversary!
I found myself thinking about how different the world -- and the internet in particular -- has become, since the start of GameMaker Server.
Originally, I wanted to write about my #1 mistake that led to GameMaker Server's downfall, but as I was writing about it I realized I first need to describe *what the world was like* when I made GameMaker Server.
So many of the things that we take for granted today, were not at all obvious in 2011 -- the year I released the first version of GameMaker Server.
So I hope this story can shed some light on how GameMaker Server came to be what it is today!

My framing here might be clouded by how young and unexperienced I was,
but in the late 2000s, making video games felt like a mysterious art that was impossible to learn.
It required expensive tools and knowledge of hard-to-learn programming languages like C++.
For example, [Unity only became available free-of-charge in 2009](https://unity.com/news/unity-2-6-released-and-now-free), just two years prior to GameMaker Server's release.
Tutorials on the internet were sparse, because real knowledge could obviously only be gained by reading books.
Who could ever trust anything they read on the internet, if anyone could just put things on there?

We were all still using Internet Explorer and Firefox.
We played RuneScape, which ran as a Java applet in your browser.
Minecraft 1.0 had not even been released.
And of course, we all used flip phones.
Because who on earth would ever spend $499 on a *cell phone* with a stupid name like "iPhone"?
All you need those things for is to call other people.
And the iPhone couldn't even run Flash!
Clearly a product that had no chance at ever becoming successful.

What made GameMaker so amazing, is that it had a free lite version and a cheap $20 upgrade to the pro version, and it was easy-to-learn and well-documented.
You didn't even have to learn how to code to use GameMaker.
It had a relatively powerful system where you could drag-and-drop actions to certain events.
You could spend most of your time just being creative: drawing graphics, designing levels and tweaking game mechanics.

This was also the time when online features in games were becoming popular.
Broadband internet adoption was growing rapidly, which meant that you could be always-online.
(before that you had to use your phone connection at home, which meant that you couldn't receive calls while using the internet)
Free-to-play multiplayer games also became more popular.
For example, in 2011 Valve began to offer Team Fortress 2 as a free-to-play title through Steam.

But again, while making video games was now easy thanks to GameMaker, online functionality in video games still felt like a mysterious art that was impossible to learn.
Everyone just YOLO'ed their own thing.
If you wanted to add online highscores to your game, you would find a `.php` file on the internet that claimed to do that.
You'd upload that file to your free 100MB shared webhosting, and voila!

Online functionality often just disappeared after someone stopped working on their game.
All the free shared webhosting seemed to shut down after a few years, the `.php` files contained security vulnerabilities and they got hacked, or they simply stopped caring and deleted the `.php` file from their hosting.
One of the MMOs that I played for a short period (it was about bananas, if I recall correctly),
would only be online whenever the creator was home and had their PC turned on.
When they stopped working on the game, it -- and the surrounding community -- died.

This is the context in which GameMaker Server was born.
It was born because I wanted to make multiplayer games, but could not find the tools that made such a thing easy to do (and free).
I wanted my games' highscores to remain available, even if I stopped caring about the game.
I wanted my multiplayer games to always be online, not only when I could run them on my PC.

So I set out to learn this mysterious art of making online games.
I started modifying a Minecraft Classic server written in C#.
Initially, I added extra server-side features to Minecraft (which was, of course, run via a Java applet in your browser!).
At that time, anyone could host a Minecraft Classic server and add it to a public server list on minecraft.net.

Later on, I made a simple 2D Minecraft clone in GameMaker.
I modified the Minecraft Classic server to be able to host the multiplayer part of the game, which I ended up calling the "IslandServer".
Of course this project never ended up going anywhere, but it was the beginning of my work on what would later become GameMaker Server.
I copied many of the design decisions made in that server, and eventually ended up building a generic multiplayer hosting server which kept the name "IslandServer" for a long time.

Back then, VPS'es were not as common as they are now, and hosting at home still seemed like a viable option.
So, when GameMaker Server launched, I ran it on an old laptop at home, with a free domain name.
It somehow seems funny now, but back then the server was a UI application with actual buttons -- again, borrowing from the Minecraft Classic server that I modified.
If I recall correctly, it ran on Windows XP.
As GameMaker Server grew, hosting eventually moved to a dedicated Linux machine, and then later a VPS.

Since I was still figuring out how to code, GameMaker Server underwent a few rewrites.
Most of them in the early years.
Somewhere in 2012, I completely rewrote the extension and the site, adding support for the newly released GameMaker: Studio 1.
GameMaker Server moved to `gamemakerserver.com`, and the first English version of the extension was released.
Then somewhere at the end of 2013, I rewrote the server backend and website.
It added comments on the website, most of the current design, and many other features. *

From then on, not much interesting happened.
GameMaker Server mostly improved incrementally.
Rather than starting over from scratch every time, I built on top of the existing code to add new features.
As I learned and got better at coding, I did of course gradually improve parts of the code.
For example, GameMaker Server's server architecture changed a lot over the years.
The server was attacked multiple times, *very* popular games (\*cough\* DF \*cough\*) started using it, and new technologies and programming languages became available, and this led to changes in the architecture to make the servers more robust.

But for now, dear readers, this is the end of the story of how GameMaker Server came to be what it is today.
I hope you have enjoyed reading my ramblings about it!
The journey has had its ups and downs, but I don't regret starting it.
It is amazing to see how long it has survived, and I am grateful for everyone that has used or supported GameMaker Server along the way.

Thank you!

--

<small>
\*:
There was supposed to be one more rewrite!
A *complete* rewrite that would break backwards-compatibility, fix all bad design decisions that I made in the past, and turn GameMaker Server into the best platform it could ever be.
But sadly, it was never finished.
I believe that it was my biggest mistake in GameMaker Server's history.
The one mistake that lead to GameMaker Server ending up on life support as it still is today.
But that is a story for another time.
</small>
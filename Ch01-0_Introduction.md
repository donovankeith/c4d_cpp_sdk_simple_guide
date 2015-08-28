# Introduction

Hello and welcome to an introductory tutorial on the Cinema 4D R17 C++ Software Development Kit. The goal of this document is to get you writing C++ plugins for Cinema 4D as quickly as possible.


## Disclaimer

This Wiki is being written by a relatively inexperienced 3rd party developer and does not necessarily represent official best practice. At the moment this is an incomplete document - but ***you*** can help make it more complete. Please mark issues and make suggestions.


## Assumptions

Unfortunately, this guide cannot be all things, to all people. To that end, certain assumptions have been made.

### About You

* You have prior programming experience.
* You have at least a basic understanding of C++.
* You have a working knowledge of your IDE (Integrated Development Environment)
* You are familiar with Cinema 4D

If you're relatively new to programming, I would recommend starting with the [Cinema 4D Python SDK](http://www.maxonexchange.de/sdk/CINEMA4DPYTHONSDK/index.html) as it's a bit easier to hit the ground running when you don't have to deal with compilation, memory management, and list indexes - all things that make C++ faster to run, and a bit more painful to work with.

### Hardware / Software Setup
You can code on a Mac or PC - but for the purposes of this guide, I will only be
covering this exact setup:

- Cinema 4D  
![Cinema 4D R16.050 About Dialog](http://i.imgur.com/KdlBcuU.png)
- OS X  
![OS X Yosemite About Dialog](http://i.imgur.com/kcgGbBX.png)
- Xcode  
![Xcode v6.4 About Dialog](http://i.imgur.com/HPJdQ5L.png)
- GitHub
![GitHub Homepage Screenshot](http://i.imgur.com/BiOjl2c.png)

If your setup differs, there's a good chance that even if you follow along
exactly with my instructions you will run into problems. Software development,
way more complex than it reasonably should be - and there are a lot of dependencies
between each of the parts. With the wrong mix you can get some very unexpected
results.

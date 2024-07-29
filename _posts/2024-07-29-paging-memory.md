---
title: "How to set the right amount of paging memory on Windows."
tags: "Windows", "Guides"
description: "Made for modern Windows OSes."
layout: post

---
Hello! :wave:

Paging memory is kinda like Linux' swap memory.
It's used for storing memory of large applications too big for your RAM to handle, for our case, games.

Your games wont and can't run on 8 or 16 GBs or ram, probably not even 32 if it's a new AAA game. That's why there's paged memory, and too little of it can cause memory leaks and BSODs.

Windows automatically comes up with the required amount of paging memory, but sometimes it's not enough.

# How to change it
Right Click on Windows/Start Menu > System.
W11: Click on ``Advanced system settings``
W10: Scroll down until you see  ``Advanced system settings`` and click on it.

Click on ``Perfromance`` tab, then under ``Virtual Memory`` click on Change.
Disable ``Automatically manage paging file size for all drives``.

Select ``Custom size`` if not selected already.

## Determining your right amount for the paging pool.

Initial size: 1.5 x your RAM size (e.g. 16 gb)
Maximum size: 3 x Initial Size

Example: 
> "So let's say you have 4 GB (1 GB = 1,024 MB x 4 = 4,096 MB) of memory. The initial size would be 1.5 x 4,096 = 6,144 MB and the maximum size would be 3 x 6,144 = 18,432 MB." 
- [Source: GeeksInPhoenix](https://www.geeksinphoenix.com/blog/post/2016/05/10/how-to-manage-windows-10-virtual-memory)

Then click ``Set`` then click ``Apply`` and ``OK`` on every box, then reboot.

# Congratulations! :tada: 
This is the end of the guide. Your PC/Laptop should now be memory-leak free!
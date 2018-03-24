---
layout: post
title: node event loop 
tags: [nodejs]
---

## the node event loop in a nutshell
I have a few other posts on the workings of node(lowrider.libuv) but this pull things together for a common GROK.

1. When a node program is started, node creates **one thread**.
2. All code is executed in that thread.
3. Inside this process is the node event loop, who's job is to decide at any given time what the thread should be working on.


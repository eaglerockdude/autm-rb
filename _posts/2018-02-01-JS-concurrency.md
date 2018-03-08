---
layout: post
title: javascript concurrency
category: javascript
tags: [javascript]
---

> *"Captain's log stardate... unknown. During an ion storm the landing party has beamed back to the Enterprise and found it and the personnel aboard changed. The ship is subtly altered physically. Behavior and discipline has become brutal, savage."*  Startrek Mirror Mirror episode parallel universe.
  
# Javascript does not run things in parallel
## Concurrency
"Concurrency can be defined as multiple things happening in the same *time frame*..but not really at the same time.

That is what the javascript event loop really gives us.  That advantage is that we don't have to manage things running at the exact same time which is way more complicated to do. 
## So
 In javascript what we are focused on is breaking down the tasks and scheduling
 them in the best order within context of coordinating concurrency.  
 
 Javascript is single-threaded no matter what.  But we can simulate multi-threading.
 
 To coordinate concurrency we can use *callbacks*...and now *promises* via ES6..
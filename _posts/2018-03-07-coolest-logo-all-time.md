---
layout: post
title:  coolest logo of all time
category: javascript
tags: [javascript, nodejs]
---

> "I am the coolest of all time!"    (probably said by "The Fonz" )

I went to the [libuv](http://docs.libuv.org/en/v1.x/design.html) website which is a support library written for 
node.js for I/O polling mechanisms.   It has to do with the event loop and things like that.  I was wowed when I saw their logo...just too cool.

 ![The coool-ist logo of all time](/assets/img/libuv.png)

## Some notes on libuv
[Kudos to  Introduction to libuv by Nikhil Marathe](https://nikhilm.github.io/uvbook/index.html)  

  "The node.js project began in 2009 as a JavaScript environment decoupled from the browser. Using Google’s V8 and Marc Lehmann’s libev, node.js combined a model of I/O – evented – with a language that was well suited to the style of programming; due to the way it had been shaped by browsers. As node.js grew in popularity, it was important to make it work on Windows, but libev ran only on Unix. The Windows equivalent of kernel event notification mechanisms like kqueue or (e)poll is IOCP. libuv was an abstraction around libev or IOCP depending on the platform, providing users an API based on libev. In the node-v0.9.0 version of libuv libev was removed."     
  
> So basically **libuv** was created to have something that worked with node.js across many platforms.
  
### Event loops 
   In event-driven programming, an application expresses interest in certain events and respond to them when they occur. The responsibility of gathering events from the operating system or monitoring other sources of events is handled by libuv, and the user can register callbacks to be invoked when an event occurs. The event-loop usually keeps running forever. In pseudocode:
   
  ``` 
   while there are still events to process:
       e = get the next event
       if there is a callback associated with e:
       call the callback
  ``` 
   Some examples of events are:
   
   - File is ready for writing
   - A socket has data ready to be read
   - A timer has timed out
   
   Node automatically starts the event loop of *libuv*
   
### Blocking & Non-blocking
   A common activity of computers is to deal with Input/Output(versus some kind of number crunching) and these take a lot of time.  These functions are **blocking** meaning no other processing can happen while this task is being worked on.
   Many systems handle this by using *threads* whereby each operation is started or allocated to its own thread or threadpool.  This enables the CPU to work on other things.
   
   **LIBUV** uses another solution..the *asynchronous non-blocking* approach.  Operating systems have event notification built in.  For example, a normal read call on a socket would block until the sender actually sent something. Instead, the application can request the operating system to watch the socket and put an event notification in the queue. The application can inspect the events at its convenience (perhaps doing some number crunching before to use the processor to the maximum) and grab the data. 
   
   It is asynchronous because the application expressed interest at one point, then used the data at another point (in time and space). It is non-blocking because the application process was free to do other tasks. This fits in well with libuv’s event-loop approach, since the operating system events can be treated as just another libuv event. The non-blocking ensures that other events can continue to be handled as fast as they come in.
   
   > LIBUV and OSes will usually run a background/worker thread and or/polling to perform tasks in a **non-blocking** manner.  A default-loop is provided by LUBUV and this is the loop that NODEJS uses as its mail loop.
   
### Error Handling
I/O read callbacks(such as files/sockets) will return a < 0 flag if there was an error.

---
layout: post
title: turbolinks5 
tags: [rails]
---

> "Turbolinks 5 turns your rails application into a single-page application.."
## Turbo-links Hawaii 5.0
Turbolinks 5 was a total rewrite.  I summarize here why these changes
have presented an alternative to the Angular/React approaches and how they reduce complexity of application development as well as the amount of developer resources needed to create and maintain said apps.

1. Turbolinks "intercepts" the event from your links and converts them to an ajax request.
2. On the response return it intercepts again, merging the \<HEAD> and totally replacing the \<BODY> tag.
3. Nothing needs to change on the server.
4. The client does not need to reload things like assets etc.
5. A page refresh of about 300ms is considered not noticeable based on studies, which turbolinks can achieve.  Even that and less.
6. A rails app using turbo links and support not only a web page application but also
phone hybrid apps in android and iOS using adapters.
7. It has no dependencies and is available via NPM. It can be used separate from the asset pipeline, or even in a non-rails app.


    [RailsConf talk on turbolinks by Sam Stephenson a rails core member who helped development on it](https://www.youtube.com/watch?v=SWEts0rlezA)

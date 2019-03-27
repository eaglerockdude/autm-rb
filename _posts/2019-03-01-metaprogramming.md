---
layout: post
title: metaprogramming
tags: [ruby]
---

> "As Ricky Ricardo once said to Lucy...I gotta go to a meta...(meeting).."
## Notes on meta-programming

Notes on metaprogramming.

- Ruby class are just runnable code, meaning the interpreter will run them
even it not instantiated.
- classes can be opened anytime and changed or added to.
- in ruby there is NO connection between instances and instance variables.  Meaning that if you don't use an instance variable, say in a method in an instantiated class, it won't contain the variable.  But of course it can spring up of you use it.

- an object’s instance variables live in the object itself, and
an object’s methods live in the object’s class. That’s why objects of the same
class share methods but don’t share instance variables.

     
   




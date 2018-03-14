---
layout: post
title: turbolinks
tags: [rails]
---

> ... there's a big difference between a) keeping up with open source, and b) hitching your cart to every horse that struts by with shiny new shoes...Jerod Santo/changelog.com
 
## Turbolinks(3.0 latest)

Turbolinks was created by DHH with rails 4.0 in 2012 and was inspired by pjax.  It was re-written for version 5.  Its purpose basically was to make displaying portions of a webpage faster/more efficient using AJAX.      

In the original version it could refresh the entire webpage(<body> tag) which made the web page faster because no javascript nor CSS had to be re-downloaded.  In the **new release** you can be more specific and refresh partially via using javascript **data-** attribute tags.
 
Most associate it with rails but it can be used with other frameworks/languages also.
### Some high-lites
- It doesn't require server-side request detection or alternate rendering
- It doesn't depend on jQuery or any other library
- It includes a CSS-based loading progress bar
- It can reload when assets change
- It can persist elements across page loads
- You can install it with npm/yarn and load it with webpack

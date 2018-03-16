---
layout: post
title: turbolinks
tags: [rails]
---

> ... there's a big difference between a) keeping up with open source, and b) hitching your cart to every horse that struts by with shiny new shoes...Jerod Santo/changelog.com
 
## Turbolinks(3.0 latest) and SPA type behaviors

Turbolinks was created by DHH with rails 4.0 in 2012 and was inspired by pjax.  Its purpose basically was to make displaying portions of a webpage faster/more efficient using AJAX.      

In the original version it could refresh the entire webpage(using the \<head> and \<body> tags) which made the web page faster because no javascript nor CSS had to be re-downloaded.  In the **new release** you can be more specific and refresh partially via using javascript **data-** attribute tags.
 
 ### How it works
 In its basic form, rails creates an HTML page on the server, and then renders it sending it to the browser.  Using Turbolinks, the same approach is used.
 
 With an SPA application the entire page is loaded the first time at once, and any changes in content are updated individually to the net effect of the UI not appearing to flash or refresh. To accomplish this normally a front-end framework is required. The CSS and javascript and other assets like images are not reloaded which increases speed.
 
 *Turbolinks does pretty much the same thing:*
 It intercepts all \<a> links and makes an AJAX request, gets the response and renders it. The window, document, and \<html> element persist from one render cycle to the next. The history API is used to keep the browser URL in sync.
 #### Form submissions
 Turbolinks does not "do" form submissions, but rails itself already handles that and with version 5 AJAX submitted forms are the default. 
 #### Some highlights
- It doesn't require server-side request detection or alternate rendering
- It doesn't depend on jQuery or any other library
- It includes a CSS-based loading progress bar
- It can reload when assets change
- It can persist elements across page loads
- You can install it with npm/yarn and load it with webpack

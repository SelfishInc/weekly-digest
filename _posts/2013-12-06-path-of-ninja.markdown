---
layout: post
title:  "Path of ninja"
date:   2013-12-06 19:00:00
categories: digest
---

# Prototype of upload files in parallel

We are ready to demonstrate working prototype of files uploading in parallel with other actions (like post writing, exploring etc.)

![Alt chart](http://gyazo.com/9145e0d73129e376c33b88ad0ff685bf.gif)

# Cache for story 

As in the stash - all story post also cached and saved in browser history for better user expirience. All posts automatically updated every ten seconds to newest state.

# Popup vertical positioning

Small improvement for popup positioning. Now it always center alignment, independently of screen size and ratio.

# Nginx server prepared for SEO

We are little closer to setup SEO for Selfish. Nginx server and other production scripts ready for search indexing

# Windows IE virtual machines for developers

All developers have access to Internet Explorer virtual machines where they can test and debugging application directly in browser.

# API  for post like functionality

`like` and `unlike` request now getting subject type parameter, that can be file or post

# User group documentation

Some general documentation for user groups with access levels (different groups have different access levels) with API explanation. You can see it [here](http://confluence.frumatic.com/confluence/display/SLF/Selfish+Contact+Groups+API)

# API error request notifications

If API request failed, error notification shows for user.

* * *
Check out [our test server][test] for latest updates. File all bugs/feature requests at [Jira][jira].

[jira]: http://jira.frumatic.com/
[test]: http://test.selfish.frumatic.com


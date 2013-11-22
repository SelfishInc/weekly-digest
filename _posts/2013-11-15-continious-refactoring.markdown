---
layout: post
title:  "Continuous refactoring..."
date:   2013-11-15 19:00:00
categories: digest
---

# Files loading improvement in Ribbon & Stash 

All media elements in ribbon and stash now preloads in its own grid, instead of loading one by one. Now we are little closer to displaying files like Google or Flickr doing it.

# Direct link to attachment from email

If user are notified about new comment in story attachment by email, he has quick access to it by url. When user click Reply button from email - link goes to Selfish and attachment with comments open in current post.

![Alt chart](http://i.minus.com/iq2azlAlkAr9S.png)

# File module refactoring

File module system now separate to `stash`, `ribbon` and `upload` services for more simplicity and stability for each of this module.

# File cahing in Stash

Some other improvements for stash. All files cached and saved in browser so it doesn't need to load its each time for stash opens.

# CSS Refactoring

According to global module refactoring we are starting CSS refactoring too. There are multiple updates to CSS modules and whole `Selfish framework`, like sprites optimization and code improvements.

# Friday presentation topic: "CSS Sprite system in Compass." by Airat Asadullin, "AngularJS $digest." by Grigory Leonenko.



* * *
Check out [our test server][test] for latest updates. File all bugs/feature requests at [Jira][jira].

[jira]: http://jira.frumatic.com/
[test]: http://test.selfish.frumatic.com


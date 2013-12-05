---
layout: post
title:  "Refactoring harvest"
date:   2013-11-29 19:00:00
categories: digest
---

# Ufa Design Proposal
This week Ufa team introduced design proposal for Selfish. This proposal includes design and UX decisions for story and post pages. You can download the design proposal [here](http://ge.tt/5rldTS71/v/0?c)

![Alt design proposal](http://i.minus.com/ibqHGWVfTY2by1.png)

# Added a possibility to align image with floating text in wysiwyg
User can set alignment image to left, right or center with text wrapping around it (only if image has left or right alignment).

![Alt image float](http://i.minus.com/iBwt08iyzCwNB.png)

# Popup refactoring comlete
All popups now working through popups manager.
It is a module, located in `/modules/popups-manager/` directory. Module include 2 directives ( `slf-popup-nest`, `slf-popup` ) and one template.

Here is a little example through this directives:

* slfPopupNest directive

Directive should be located on main content element wrapper. It transclude main content and manage popups.
`index.html` file now looks like this:
{% highlight html %}
<div data-slf-popup-nest>
  <div class="header"></div>
  <div class="container-view" data-ng-view></div>
</div>
{% endhighlight %}
After directive fired html changes this way:
{% highlight html %}
<div data-slf-popup-nest>
  <div data-ng-transclude>
  <div class="header"></div>
  <div class="container-view" data-ng-view></div>
  </div>
  <div class="popup-windows">
    <!-- ngRepeat: window in windows -->
  </div>
</div>
{% endhighlight %}
slfPopupNest directive manipulates windows array. Every windows item has “src” (path to popup template), “params” ( object, that popup controller use as input parameters) and “hideMainContent” option ( hide transcluded content if this window is active )
slfPopupNest directive also close popups on ESC key and close all popups if route changes

# File System Refactoring complete
All File Services separated, `Stash`, `Ribbon`, `UploadPopUp` new controllers and services. Files stores in cache, after upload files receive themselfs metadata. Fixed cover creation, avatar change, upload files to post.

# Diff updates and update log in deploy scheme
Diff updates with updates logged in deploy scheme and sended to developers after each deploy.







* * *
Check out [our test server][test] for latest updates. File all bugs/feature requests at [Jira][jira].

[jira]: http://jira.frumatic.com/
[test]: http://test.selfish.frumatic.com


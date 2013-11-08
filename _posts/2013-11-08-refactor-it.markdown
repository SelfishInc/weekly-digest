---
layout: post
title:  "Refactor it!"
date:   2013-11-08 19:00:00
categories: digest
---

Hi! This is our first demo weekly digest. Here you can follow the newest development progress on working on `Selfish`. Currently there are only `frontend` news, but we going to include `backend` news soon.

On this week we start refactoring existing code base, and work on providing better expirience on `Selfish` for users. So here the main topics:

# Bug fixing

`77` bugs created and `80` resolved

![Alt chart](http://i7.minus.com/iQBSBYknM7TpS.png)

# URL saving after log in
Necessary improvement for not-logged-in users. Now if you read some post or story you don’t need to search it again after login.

# Global namespaces for directives
According to our refactoring plan, we are divided selfish frontend core into modules. One part of it was directive refactor. Now all module directives has it’s own namespaces.

{% highlight javascript %}
// Module directive for using in Story Edit module
'<div slf-story-edit-cover-gallery></div>'
angular.module('story.edit').directive(‘slfStoryEditCoverGallery’, function() {});

// Global directive for universal using
'<input type=”text” slf-story-edit-cover-gallery>'
angular.module('common.directives').directive(‘slfKeypress’, function() {});
{% endhighlight %}
<br />


# Hierarchical model for `Profile` is extended with `Edit Profile` and `Notifications` modules 

As mentioned before this improvement is also accorded to our global module refactoring.

# Friday presentation topic: "Popups system in Selfish." by Ruslan Khakimov, "Directives in AngularJS." by Artem Popov.
And last, but not least. Beginning this week we decided to start make the presentations each week. Topics for this presentations suggests each team member. For most interesting topics we also decided write posts in the future.

* * *
Check out [our test server][test] for latest updates. File all bugs/feature requests at [Jira][jira].

[jira]: http://jira.frumatic.com/
[test]: http://test.selfish.frumatic.com


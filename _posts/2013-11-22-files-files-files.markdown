---
layout: post
title:  "Files, files, files!"
date:   2013-11-22 19:00:00
categories: digest
---

# Justified Gallery on Stash

Some cool new UI/UX intellectual feature for stash files loading. Just take a look to the screenshots…

![Alt chart](http://gyazo.com/000fed22a9c266aefc292967a9fd0663.gif)

# Embedding video from youtube and vimeo

You can past link to your favourite video from youtube or vimeo right into post body and it will automatically appear in video player.

# Popup refactoring

For better performance and code quality we refactor directives to unify style and combine it into one directive with different parameters that developers can use directly from `Selfish framework`.

# File Module Refactoring

Stash controller refactor by new cache factory, ribbon controller refactor, upload and loading files optimization. Upload popup service improvements.

# Tags on stash improvement

User can choose multiple tags for filter and all list tags updates after adding it on some file.

# Started Backend Redesign

Currently components of Selfish backend are strongly coupled by historical reasons due to hot-fix development process. This seriously complicates the development and testing of components, as we have to take into account the behaviour of the associated components, how change will affect them, and often also to make changes in them too. 

Due to stabilization of the common requirements, we decided to redesign backend to divide it into the modules, which will communicate with each other only through message bus using publish-subscribe pattern (no more direct messaging). Project will also be divided into the separate modules. 

* Core module -- Social graph, Stories, Posts, Comments.
* Notification module -- notifications, email sending.
* ACL module -- provide permission management and checking for all other modules * and services.
* Content Recommendation module -- provide recommendations.
* Administration module -- provides API for system management and end user support (moderation).
* Stash service -- file storage will be implemented as a completely separate service, that will provide file storing and processing.

We also decided to migrate from `MongoDB` to another data storage stack. In most cases it will be `Riak` + `Redis`, but several modules can possibly use other databases to achieve required efficiency.

# API Changes

New requests:

* AddViewer — add viewer to user’s story.
* RemoveViewer — remove viewer from user’s story.
* GetViewers — returns all viewers from user’s story.
* GetViewedStories — get all viewed stories.
* SearchProfile — search for some profile.
* GetMCSStories — returns user’s and collaborated stories.

Also SearchQuery request is now accessible for anonymous use.

#Tests

Primary backend functionality, such as logging in, creating stories and posts, commenting, file uploading, getting notifications, is now covered with a set integrational tests. Recently, they were improved to properly work with the standalone file processing service. 



* * *
Check out [our test server][test] for latest updates. File all bugs/feature requests at [Jira][jira].

[jira]: http://jira.frumatic.com/
[test]: http://test.selfish.frumatic.com


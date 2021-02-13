---
templateKey: blog-post
title: How To Isolate A Video in Google Chrome
date: 2021-02-13T17:36:39.436Z
description: Taking a look at the couple of lines code behind my Video Isolator
  extension for Google Chrome.
featuredpost: true
featuredimage: /img/products-grid2.jpg
tags:
  - javascript
  - html
  - google chrome
  - extensions
---
## Why Would I Need To Isolate A Video On A Web Page?

Depending on where you're watching videos, there can be a lot of unnecessary clutter on a website. 

Say you're on some sketchy website that decided a chatbox and 15 ads would be a good idea next to a sports game (not that you should be streaming a sports game on such a website.)

Wherever you find yourself, sometimes it's helpful to just delete everything on the page except for the video.

## The Code

#### Finding and storing the video

First things first, we need to find a video.

To do so, we simply use 

```javascript
var videoCollection = document.getElementsByTagName('video');
```

this will store all of the **video** elements inside of an [HTMLCollection](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCollection) (this is similar to an array, but with a few key differences that we won't be getting into. If you'd like to learn more, refer to the link.)

#### Moving the video

I'm sure you're thinking it's odd that we need to move the video, but I found that this is very useful for a few reasons that I'll describe below.

Next up we use 

```
document.body.before(videoCollection[0]);
```

Alright, why did we need to move the video?





## The Result
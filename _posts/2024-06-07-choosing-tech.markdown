---
layout: post
title:  "Choosing the tech stack"
date:   2024-06-07 17:52:42 +0200
categories: update
---

Now that some ideas have bubbled up and exploration of them has begun it has become apparent that
the primary platform will initially be mobile. This poses some interesting challenges (ignoring the
sheer number of screen size options available...).

There are some fundamental differences between Android and iOS that are simply too tedious to
tackle. It would be nice to have something that could handle all that so that game programming can
be the primary focus. Additionally, environments like Unity and Unreal, though well established, are
just too much for what is needed. Considering all this, there remains _one_ choice for platform
abstraction: SDL. With this library it is possible to hit Android and iOS while being able to test
on desktop as well. It has a small footprint and a large community as well as being open source.

To visualize the stack would look something like:

![Tech Stack](/assets/images/20240607_techstack.jpg)

With the platform abstraction being established it will be possible to write all the core game logic
in C++ (maybe scripting will make an appearance later on), meaning that CMake can take care of the
actual build system stuff.

Intially, the games will be 2D so it should be enough with the SDL Renderer abstraction for pushing
sprites.

All in all, this seems like a promising start for the exploratory stage. More to come, including how
CMake is utilised to build all the dependencies, the game, and how to package it for Android
devices.

Stay tuned!


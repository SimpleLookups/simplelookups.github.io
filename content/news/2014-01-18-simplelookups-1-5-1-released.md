---
author: "Russell Patterson"
date: 2014-01-18 02:17:20+00:00
draft: false
title: SimpleLookups 1.5.1 Released
url: /2014/01/simplelookups-1-5-1-released/
---

Today, I'm releasing SimpleLookups 1.5.1. 

This version is a major rewrite of a lot of the core stuff, so it contains no API changes. Basically, if you used it before, it should still work great for you today. The only new thing is that you can now configure it through the app.config/web.config files. The download package contains an example of how to do that, and I'll be updating the documentation so that it's even more clear.

You may ask yourself, what happened to 1.5? Well, as of today, SimpleLookups is now available in NuGet. The version had to be revved due to me accidentally pushing an early version of 1.5 during a test, and NuGet not having a way to replace the earlier version (unless the version number is higher). I'm planning to release the next major revision soon anyway, so it's not a big deal.

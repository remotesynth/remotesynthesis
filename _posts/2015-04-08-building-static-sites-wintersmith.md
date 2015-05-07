---
layout: post
title:  "Building Static Sites with Node.js and Wintersmith"
date:   2015-04-08 09:00:00
categories: general
---

When I've spoken on the topic or even when I posted my recent [guide to getting started with Jekyll](http://developer.telerik.com/featured/getting-started-with-jekyll/),  the question I always get is if there is a comparable static site generator to Jekyll that is built with JavaScript and available on npm. The reason people cite is that they aren't comfortable with Ruby and thus have trouble when they encounter problems with Jekyll or are unable to customize it completely to their needs. Well, there's good and bad news.

First, the bad news... I have found nothing comparable to Jekyll in terms of overall features, documentation and community. Now I don't know every engine out there, but, so far, there's nothing that even comes close to fully matching Jekyll.

The good news, however, is that I found [Wintersmith](http://wintersmith.io/) to be a viable Jekyll replacement. It has a lot of the key features and is extensible. Plus, there are a reasonable amount of extensions out there for it already. On the other hand, the documentation is awful (let's be honest) and the community is small. So, if you run into a problem, you're stuck reviewing the source code. On the upside, I found the source code is pretty self-explanatory when I needed to rely on it.

Given the lack of a good getting started guide in the Wintersmith documentation, I wrote a two-part series for Sitepoint that walks you through the entire process of building a site. It follows the same exact format of my [Jekyll guide](http://developer.telerik.com/featured/getting-started-with-jekyll/) covering everything from installation to templating, creating posts, custom metadata and custom data.

* [Getting Started with Wintersmith: A Node.js-based Static Site Generator](http://www.sitepoint.com/getting-started-wintersmith-nodejs-static-site-generator/) - Part 1
* [Creating Posts, Custom Metadata, and Data in Wintersmith](http://www.sitepoint.com/creating-posts-custom-metadata-data-wintersmith/) - Part 2

The source code for the example is part of my [Static Site Samples GitHub project](https://github.com/remotesynth/Static-Site-Samples) which also includes the aforementioned Jekyll sample as well as examples for Harp and Middleman.
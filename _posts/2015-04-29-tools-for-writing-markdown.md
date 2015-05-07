---
layout: post
title:  "Tools for Writing and Converting Markdown"
date:   2015-04-29 11:15:47
categories: general
---

By now, most developers are familiar on some level with [Markdown](http://daringfireball.net/projects/markdown/). It's become a somewhat ubiquitous part of developer tooling, probably in no small part due to it's usage for documentation in GitHub. It also plays a big part in nearly all the major static site engines.

The power of Markdown and probably a significant reason for its success is in its simplicity. But this is also its biggest weakness. Developers love Markdown because it offers a shorthand for probably 80% of their writing use cases - things like blog posts and basic documentation. For the other 20%, developers have no problem switching to straight HTML, which, of course, you can include in a Markdown file without issue.

For writers and the general public however, this presents a huge obstacle. They cannot use the tools they are comfortable in writing with and they not only are forced to learn Markdown syntax, but they must learn those cases that Markdown doesn't cover and the HTML to use in these cases. It's multiple layers of complexity for the sake of simplicity.

That being said, as Markdown becomes more widespread in its use, the tooling around it is slowly improving. I use Markdown daily and below are some of the tools that I've found useful in my own experience.<!--more-->

##Desktop Editors

Most code editors such as [Brackets](http://brackets.io/) or [Atom](https://atom.io/) already include some level of Markdown support. However, if you're looking for an editor with richer functionality geared specifically towards Markdown, then there are a number of options.

[Mou](http://25.io/mou/) is my current go to option for writing Markdown. As with pretty much every Markdown editor out there, you write in Markdown and have a live preview available. There is currently no option that I am aware of where you write in rich text and have it converted to Markdown.

Mou offers syntax hinting and highlights as well as keyboard shortcuts, but my favorite feature (and why I prefer it) is the export. I rely heavily on the export to HTML feature and, in my experience, it has the most reliable of the editors I have tried. The only quirk I find is that it often stumbles when using backticks for code blocks (and doesn't recognize the GitHub-flavored Markdown syntax for indicating the type of code within a code block).

Currently Mou is still free, though a 1.0 looks to be forthcoming that will be paid.

Another free option is [Macdown](http://macdown.uranusjr.com/), which was created when Mou appeared to be ceasing development. I found it to be quite buggy, personally, but have not tried it much since its initial release.

If you are on Windows, some options I've heard recommended include [Texts](http://www.texts.io/) and [MarkdownPad](http://markdownpad.com/), though I have limited experience with either.

Lastly, while not technically an editor, [Markdown Live](https://github.com/mobily/markdown-live) is a useful tool for live-previewing Markdown as you write it. Once installed, you simply change directory into the folder you want to serve up and enter `mdlive` and it will open a preview in the browser that will update as you type - without the need to save the file. This can be useful if you prefer to use a plain text editor for writing Markdown.

##Web-based Editors

If you are looking for a free web-based option, [Dillinger](http://dillinger.io/) is a free (and open source) Markdown editor for the browser. It includes a live preview as well as the ability to import documents from numerous sources and export them to various formats.

However, one of the things lacking in both desktop and web-based editors is collaboration. If you are working on a team, the ability to share, comment and collaborate on a document is not just useful, but necessary. [Beegit](https://beegit.com/) is a commercial offering that includes a number of collaboration features. My team uses it mostly for the ability to share and comment on documents as they are being developed, much as you would within Google Drive.

##Converters

When you are working with a number of contributors, it's not always possible to force everyone to use Markdown. While Markdown's simplicity makes it simple to manually convert short documents, converting long documents or groups of documents could get tedious and time consuming. While they aren't perfect, in these cases, a converter can be enormously helpful.

One converter that I rely on frequently is the [Word to Markdown web app](http://word-to-markdown.herokuapp.com/). Simply choose your local file and hit convert. The site will post you the Markdown it generates from the file as well as a live preview. For good or for bad, it even embeds images in the document using Base64 encoding. Personally, I find this can be difficult to clean up and replace with external images, so I often remove them from the source document first and put placeholders.

Word to Markdown is also available as an [open source project and command line tool](https://github.com/benbalter/word-to-markdown). In my experience, I couldn't get the command line tool to work properly for some reason, while the web app worked perfectly.

In other cases, you may encounter rich text that you need converted to Markdown, such as text copy/pasted from the web or some other editor. In these situations, I've found [Mark It Down](http://markitdown.medusis.com/) to be both reliable and helpful (it is also [open source](https://github.com/bambax/markitdown.medusis.com)). Simply paste in the rich text and hit the convert button to get back nice, clean Markdown.

##Other Tools?

This is by no means a comprehensive list of Markdown tools - just the ones that I've personally come to rely on at some level or another. Are there any others that you recommend? Be sure to share in the comments as I'm always looking for new ones.
---
layout: post
title:  "Patterns of Development"
date:   2015-01-21 09:00:00
categories: general
---

Patterns are something that you cannot view close up - a narrow view obscures the pattern. However, given distance and time, we can begin to make out the sequences that repeat. This is one of the few benefits of being old, which I am compared to many developers.

In this post, I am not talking about development patterns as in software design patterns (or anti-patterns), but rather patterns in attitudes and behavior among developers that change the way a large number of us approach our work.<!--more-->

##Front to Back to Front to...

I want to discuss a pattern I have noticed throughout my career and has only become more obvious over time. This pattern is the constant shifting in focus from front-end heavy applications to back-end heavy applications. I'm bringing the topic up becuase I believe we're seeing a shift again, which becomes clear in recent [controversies over AngularJS](http://www.quirksmode.org/blog/archives/2015/01/the_problem_wit.html).

Basically the pattern is that every 5 to 10 years (or so), developers seem to shift in attitude and opinion on where to place much of the burden of the application - moving from placing much of the application and business logic on the front-end, to placing it on the back-end. I think a little history might make this pattern seem clear (though you can feel free to disagree with me).

##Back in My Day...

As an old person, let me give a very oversimplified history.

So, I'm not that old - really I am not. But even when I went to college it was still fairly common for many applications, especially in the enterprise, to simply be a lightweight terminal-type interface to a mainframe that had the power to run the actual application logic. In this case, obviously, the "front-end" application was little more than a text entry interface for entering commands into and receiving data back from the mainframe (which was effectively the server in this case).

###Rich Client Server Desktops Applications

As PC's became more powerful, development tools (PowerBuilder was a popular one) helped developers create more complex and interactive native applications for the desktop. While the back-end might retain a good chunk of logic, the interface itself contained a lot of interactivity and the flow of the application was based upon certain business rules. Basically, many aspects that previously had to be kept on the back-end could now be pushed to the front.

###Early Web Applications

The rise of the web changed this. Why? Well, the early web was slow and limiting in many ways. It was powerful in the sense that I no longer needed to deploy applications across multiple desktops, make sure they were updated and so on. It allowed us to interact with our applications from anywhere. However, the capabilities of the browser meant that our applications were closer to the dumb terminals of earlier days than the rich applications on the desktop. Sure, they may have looked pretty with forms and tables and blinking text, but they were mostly dumb - the application logic residing almost entirely on the server.

###Flash, Flex, Silverlight...

This didn't change because browsers improved - at least not initially. Plugins like Flash built upon the initial attempts (like Java Applets) to give browsers the ability to create rich, desktop-like experiences on the web. Soon Flex and Silverlight were hot and much of the application and even business logic was moving back onto the client. Sure, we had to build portions of our business logic and validation twice, but the experience for the user was much improved. We called these Rich Internet Applications in part to recognize them as an attempt to recreate the interactivity of desktop applications but served in the browser.

###HTML5

This focus on the front-end didn't change with the death of Flash and the growth of HTML5. Actually, if anything, it increased. The primary difference was that now we were writing complex, desktop-like applications in JavaScript rather than ActionScript. In fact, many back-ends became so lightweight that, in many cases, applications would connect directly to data on the cloud or in NoSQL databases.

##A Shift (imo)

I actually wondered if we might be hitting a point where this pattern would break, but a couple of things changed as I see it.

First, there's the rise of JavaScript on the back-end using things like Node.js (or io.js if you now prefer). This isn't because JavaScript is so awesome, but because it allowed us to write business logic and validation and such in one language and it could run on both ends - meaning, for example, I don't have to write data validation in JavaScript on the front-end and Java (or PHP or whatever) on the back. Also, these servers are fast and built for running the types of web applications people seem to be building today.

However, that isn't the big reason. The major shift is because of mobile (of course!). As you may have seen in some of the recent AngularJS debates (among other related topics), placing too much burden for processing and logic on the front-end can make an application run poorly on mobile. And nevermind writing things like writing validation rules twice, we certainly don't want to have to write our applications once for the desktop and then for each mobile platform. Thus, we need to move some of the code that we'd perhaps become accustomed to placing on the client back onto our back-end server...and so goes the cycle.

Now, perhaps this trend will cease. Mobile devices are rapidly becoming very powerful computers in their own right. Or perhaps I am old and my mind is causing me to see patterns that don't exist. But given the back and forth on this that I have witnessed over my career, I suspect we may be in the midst of yet another shift.
---
layout: post
title: "Is the Native Mobile App Ecosystem Worth Saving?"
date: "2015-11-17"
categories: general
---

The native mobile app ecosystem is facing some major challenges. Some have even argued that it is in need of saving. Before we get there, though, let's examine what the problems are.

About 5 years ago, we were in the middle of a modern "gold rush" with companies eager to establish a presence in the app stores. The iOS App Store opened in 2008 and it had already reached its 10 billionth download by 2011. The Android Market (now called Google Play) reached its 10 billionth download in late 2011 as well, having launched in 2008 as well. It's no wonder that companies felt they had to be there - even if little thought was sometimes given to what value their app actually offered. The presence was enough.

Since that 10 billionth download, the app ecosystem continued to grow. This was driven in part by the fact that the mobile browser lagged far behind the ability of native apps. HTML5 was still seriously incomplete - the first working draft wasn't even published until 2008. Adobe was pushing Flash for mobile, which would have brought the "app-like" capabilities of desktop Flash to the mobile browser, but...I don't really need to revisit that, do I?

By 2013, Apple's App Store alone was raking in $10 billion in annual gross revenue. Yes, that's billion with a b.

Apps, it seemed, had won.

So what's changed?

> Please note that this article represents my personal opinion and not  those of my employer, Progress Software / Telerik.

<!--more-->

##No One's Using Our App

In his recent post, [Alex Austin makes a strong case](https://medium.com/swlh/mobile-app-developers-are-suffering-a5636c57d576) that the mobile app ecosystems has become over-saturated and tilted heavily towards the top 0.01% of apps. He posted a chart that illustrates this.

![The punishing app adoption power law](/images/posts/adoptionpowerlaw.png)

Given the dramatic drop off, what chance does your company's app have? As Alex says:

> In the past four weeks, there were 45,000 new apps submitted to the iOS App Store alone. The chances that any of them will ever break into the top 1000 are effectively 0%, and even if they did, they’re still not seeing any amount of traffic to build a successful business.

This assertion is backed up by industry reports. In a recent [mobile apps survey](http://www.gartner.com/technology/reprints.do?id=1-2JLR2P2&ct=150717&st=sb), Gartner covers how reluctant users are to installing new apps.

> Only 8% (U.S.) [of respondents] said they enjoyed searching for new apps.

And in [Comscore's 2015 U.S. Mobile App Report](https://www.comscore.com/Insights/Presentations-and-Whitepapers/2015/The-2015-US-Mobile-App-Report), they note the difficulty in building a mobile app audience.

> Despite growing audiences on apps, the existing digital infrastructure makes it harder to build large audiences on apps than on the web. As evidenced, the mobile web still has 3.5x more web properties with 5 million unique visitors than apps have.

As if to reinforce Alex's point, they note that the "list of Top 25 mobile apps is dominated by the leading digital media companies and tends to concentrate within a few categories." Add to this other recent studies that have noted that a large majority of users don't download a single new app in any given month (it's around 65%, according to a [2014 Comscore survey](http://www.engadget.com/2014/08/22/comscore-app-downloads/)).

While Comscore notes that a company's mobile app audience tends to be worth more because they are more loyal, there are clearly many obstacles in the way of building a substantial and monetizable audience in the app ecosystem.

Well-known venture capitalist Fred Wilson has discussed what he calls the "mobile downturn" since 2014. In a [recent post](http://avc.com/2015/11/the-mobile-downturn-continued/), he noted:

> Doing anything in the consumer mobile space these days is super hard. I can’t think of many consumer facing mobile apps that have gained massive traction and sustained it in the past three years. Can you?

In the [same post](https://medium.com/swlh/mobile-app-developers-are-suffering-a5636c57d576) discussed earlier, Alex Austin shared some ideas of how to save the mobile app ecosystem - more on that later. But first, can't the mobile web offer an alternative?

##The Mobile Web to the Rescue?

So if apps are hurting, does this benefit the mobile web as an alternative? Yes...and no.

In a [recent post](https://atavistinsider.atavist.com/goodbye-native-mobile-apps/) discussing why the [Atavist](https://atavist.com/) is dropping its native apps, Evan Ratliff and Jefferson Rabb note that one of the reasons is that the mobile web has finally caught up, in many respects. The situation is not the same one as in 2012. Many of the features available to native apps are now available in the browser - and it is much easier to develop once for the web than to maintain multiple native apps. Because of this, they note:

> The reasons for creating a native experience began to narrow. Not only was there very little we could do in a native app that we couldn’t do on the web, but the strictures of the native app environment made it nearly impossible to design well for both.

And the mobile web audience is extremely large and growing. Referring again to [Comscore's 2015 U.S. Mobile App Report](https://www.comscore.com/Insights/Presentations-and-Whitepapers/2015/The-2015-US-Mobile-App-Report):

> A comparison of the Top 1000 Apps vs. the Top 1000 Mobile Web Properties shows a surprising result. Not only do mobile web properties have audiences that are
more than 2.5x the size, but these audiences are also growing twice as fast.

So if the web is nearly as powerful, easier to develop for, has a larger reach and is growing faster, what's the problem?

Well, Comscore did follow up the above stats by noting a lack of engagement by mobile web users. Average engagement has been in a steady decline since late 2014, leading them to believe that much of the growth is what they call "drive-by traffic."

The other big problem with the mobile web is that, as I've [discussed in detail before](http://developer.telerik.com/featured/whats-wrong-with-the-web/), the mobile web suffers from performance issues and poor monetization capabilities - these are somewhat related as the [performance problems are often caused by the attempts to monetize](http://developer.telerik.com/featured/the-webs-cruft-problem/). This has led to the rise of mobile ad blockers, which, while [apparently very effective](http://www.nytimes.com/2015/10/01/technology/personaltech/ad-blockers-mobile-iphone-browsers.html?_r=0) in improving performance, are expected to cost businesses upwards of [$22 billion in revenue](http://www.nytimes.com/2015/08/20/technology/personaltech/ad-blockers-and-the-nuisance-at-the-heart-of-the-modern-web.html) this year alone. Yes, that's billion with a b.

##So There's No Hope Then?

So, at this point we've established that the native mobile app ecosystem is potentially broken and the mobile web doesn't currently offer an easy, clear-cut alternative. What can we do?

Let's turn back again to [Alex Austin's article](https://medium.com/swlh/mobile-app-developers-are-suffering-a5636c57d576). He offers a variety of potential solutions to fix the mobile app ecosystem including a better discovery system and, essentially, automatic download/install of apps via intents. He ends with the assertion that "something must be done."

But must it?

I agree that there is a problem with the native mobile app ecosystem. In fact, I've been arguing this on a personal level for years. Before I go further, I will reiterate that this is _my personal opinion_ and does not reflect those of my employer (i.e. Progress Software or Telerik). Ok, now that that's out of the way, I can say that I think the bigger issue is that **most apps suck**.

##That's Right, I Said Most Apps Suck

Yes, I am being hyperbolic here but let me explain.

First, apps have to overcome series of inherent issues such as:

* Apps require a download and install process, even if we link to the app via intents. This isn't necessary on the web.
* Apps eat up space on my device - sometimes needlessly large amounts when you combine the application, cache and data. Web apps use little to no permanent storage (with minor exceptions).
* Many apps can hurt the performance and battery life of my phone by running background processes. Web apps do not (and despite some claims, ads don't kill your battery and mobile web ad blockers have been shown to offer [minimal improvement on battery life](http://www.nytimes.com/2015/10/01/technology/personaltech/ad-blockers-mobile-iphone-browsers.html?_r=0)).
* Apps are noisy (and can be annoying) by design and by default. Managing the mess of app notifications is such a pain that we're willing to pay $350+ for a separate device whose primary benefit is [decluttering app notifications](http://www.techrepublic.com/article/the-only-two-reasons-to-buy-an-apple-watch-for-now/).
* Apps require constant maintenance by the user via updates and app store approvals. Plus it can be difficult, as an app creator, to get your users to update. The web is always running the latest release, no intervention needed.

None of these problems are dealbreakers and some are more prominent on one platform versus the other. And a good app can make all these issues seem trivial. However, it is important to keep in mind that apps don't inherently offer something of value. The value is what you build into it. Simply being in the app store does not make your app worthwhile to consumers.

Let's look at Comscore's list of the top 25 apps (i.e. the apps that eat up over 99% of all usage):

[![Top 25 Mobile Apps](/images/posts/top25apps.jpg)](https://www.comscore.com/Insights/Presentations-and-Whitepapers/2015/The-2015-US-Mobile-App-Report)
_Source: [Comscore](https://www.comscore.com/Insights/Presentations-and-Whitepapers/2015/The-2015-US-Mobile-App-Report)_

Many, if not most, of these apps could arguably run equally well on the web and offer equivalent, or nearly equivalent, functionality. Heck, a number of these are simply "appified" versions of the web site. However, all of them have the brand power to push them to the front of the line regardless (or even come pre-installed on many phones).

The point is, unless you have a massive global brand to fall back on, the only way for your app to stick out in a crowded marketplace is to truly focus on the needs of your users. Better monetization and establishing an app store presence are company problems, not a consumer ones, and not reasons to build an app in and of themselves.

If you already have an app and feel the need to improve adoption via an app install interstitial, it's very likely that you haven't given enough thought as to why your app exists in the first place. Instead of trying to force your web users into your app, focus on making your app more appealing by making it useful. Gartner's advice in their [recent report](http://www.gartner.com/technology/reprints.do?id=1-2JLR2P2&ct=150717&st=sb) speaks to retention, but, in my opinion, applies equally to gaining new users:

> Focus on creating richer, more immersive and personalized app experiences for your apps users to keep them coming back.

###I Did Also Say "Most"

I should emphasize that I am not claiming all apps are bad or apps are bad by nature. In marketplaces that each have [over 1.5 million apps](http://www.statista.com/statistics/276623/number-of-apps-available-in-leading-app-stores/), there are probably thousands of fabulous apps. However, the large number of bad apps are crowding out the good ones, making them hard to find or identify.

Apps also have some innate benefits. For example ,most of the apps I have installed don't really offer a ton of functionality over their web counterparts, but I use them for the one-click convenience the home screen icon offers or because, in some cases, their push notifications matter to me (Slack for instance). These benefits are not without value.

These are areas the web needs to catch up. The one-click convenience does not have to be solely the domain of native apps. And [push notifications](http://www.w3.org/TR/push-api/) on the web are coming (and in some cases, they're [already here](https://developers.google.com/web/updates/2015/03/push-notifications-on-the-open-web)).


##The Native Mobile App Ecosystem Doesn't Need Saving

Native mobile apps don't need to be saved because they aren't dying. This pain the ecosystem seems to be going through is not a pain of injury but one of healing. It is a pain caused by misuse - by filling the app store with thousands of apps that don't need to exist.

It is a pain that, I believe, will cause companies to move from saying "We need a mobile app" to asking "Why do we need a mobile app?" Answering this question gets at the real value your app intends to bring for the consumer/user.

There's a famous scene from the Seinfeld episode named "[The Pitch](http://www.seinfeldscripts.com/ThePitch.htm)" where George Costanza is pitching his show about nothing to a TV executive:

![George Costanza](/images/posts/the-pitch-picture.jpg)

> GEORGE: The show is about nothing.
>
> ...
>
> RUSSELL: Well, why am I watching it?
>
> GEORGE: Because it's on TV.
>
> RUSSELL: (Threatening) Not yet.


For too long, many companies used the George Costanza line of reasoning for their apps - why would anyone want to download this app? Because it's in the app store. And too many apps were about "nothing" in the sense that they didn't focus on the value they intend to offer by being an app beyond just claiming a spot in the app store or offering the company that created it an easier route to monetizing than the web offered.

The current state of the native app ecosystem is forcing companies and developers to come to grips with what value our native apps offer over the web before entering an already overcrowded market. The result, I hope, will be fewer but better apps.

Meanwhile the current state of the mobile web is forcing us to fix the issues we've let fester because of our over-reliance on native apps to solve the ills of the web - namely performance and monetization. The result, I hope, will be a mobile web that better meets the needs of both consumers and companies.

Yes, both ecosystems need some fixing but both will survive. And I believe both will be better for their suffering.

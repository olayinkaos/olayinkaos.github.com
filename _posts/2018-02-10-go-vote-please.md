---
layout: post
title:  "Go Vote, Please?"
date:   2017-10-29 00:00:00
categories: 
image: https://govote.org.ng/assets/queue.svg
disqus: true
description: How and why me and Yomi built are building a bunch of software to help Nigerians vote in the 2019 General Election.
---

Some weeks ago, I decided I wanted to get my PVC to vote in the 2019 Nigerian General Elections. I believe taking a step is better than doing nothing. No revolution ever started with people folding their hands and resigning to their fates, right?

I almost gave up after my supposed conviction for one tiny reason - I could not for the life of me find where to register for my PVC. Checking the INEC website for the locations was the biggest waste of time. After [tweeting about my ordeal](https://twitter.com/olayinkaos/status/957740741761097736), [Efe](https://twitter.com/efefregene) sent me a PDF with all the locations for PVC collection in Lagos on WhatsApp.

The information on the PDF was 10 pages of chaos. It didn't have proper addresses, and all the info on it was unclear. If you're like me, you would most likely have closed the PDF and moved on with life - "next time abeg". For some reason though, I didn't close it - I thought it was a genuine problem. I started thinking of ways to enable the 2019 elections with software. After all that's what software does best, enable.

![Lagos PVC Locations PDF](https://dl.dropboxusercontent.com/s/0tspxghftyth268/Lagos%20PVC%20Locations%20Screenshot.png)

{: style="color:gray; font-size: 80%; text-align: center; margin-top:-55px;"}
Lagos PVC Locations PDF

As I usually do with my ideas, I buzzed a few friends and asked what they thought. Even though no one was super psyched about it, we agreed on one thing - it should be done. That was all the permission I needed. I created a new [Koa](http://koajs.com/) project, saved the data from the PDF to a MySQL database and did some shenanigans to get the proper city and geolocation information for each collection centre. In a few hours, I had completed the [basic API](https://github.com/ErxiaHQ/govote-api).

[Yomi](https://twitter.com/yomieluwande) and [Douglas](https://medium.com/@KendysonD) (the best coders a coder could know) were excited about it too and we decided we were going to build a front facing app and a twitter bot to work with the API. The app is currently live, mostly thanks to Yomz! You can check it out at [govote.org.ng](https://govote.org.ng/).

![GoVote Landing Page](https://dl.dropboxusercontent.com/s/e7idn0b4kwabkaq/GoVote%20Landing.png)

{: style="color:gray; font-size: 80%; text-align: center; margin-top:-55px;"}
[GoVote Landing Page](https://govote.org.ng/)

We named the project GoVote, because that is what we believe everyone should do. Ayoola recently told me that Nigeria isn’t run by our votes. While I may agree, I also know that a revolution does not begin till a group of people decide to fight the odds, go against the impossible, and say to the institution “damn you, I’m taking a step”. Your vote isn’t just the ballot you’re casting, it is a symbol of your hope in the country, and the commitment you’re making to try to make it better.

We believe we are lucky, we have been put in a position to effect change, and we will do our best to. We do not want to do it alone - join us, [contribute on GitHub](https://github.com/ErxiaHQ/), correct the data, add more locations, and let us one step at a time, make our country better.




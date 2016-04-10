---
layout: post
title: Hacking together a data masher
date: '2014-08-12 22:12:16'
---

To say I started my latest hack on Sunday when I had a spare hour would be a misstep.

I actually first had a go at it a few months back, around Easter time.

The idea back then was a simple: Grab all the Leeds based events from Eventbrite and then list them. Listing the data simply and in chronoligical order would help me (and anyone I shared the hack with) find events to go to and help recognise when I could organise events myself by knowing when to avoid. It was also a good chance to see how malleable Eventbrite’s data was and test my PHP skills.

The problem back then was getting the data from Eventbrite wasn’t as straightforward as I thought. I went in blindly thinking "I can just grab this data, sort it, splat it on screen, job done".

Instead of being able to (reasonably easily) ask the Eventbrite API for all the events near Leeds (even by giving a longitude and latitude and then a maximum distance from that), Eventbrite generates location data as through RSS feeds. And pretty much *all the data* I needed was scrunched together and held within *one field* within that feed.

I needed to parse the feed's XML - simple enough - and then write a routine to parse the specific XML field to break *that* down, so I had location, date, time, etc as separate elements. Strewth!

While I had PHP as a good part of my life 10 years back, after a few years of minimal coding my PHP skills were rusty. I spent about half a day playing around, and got something spat out which was bug ridden. But my enthusiasm for the idea waned. Did I really need to spend spare time or down time fuddling about? I decided there were other things to do, other things I could do, other things that wouldn't have me grimacing at the Macbook - as much anyway.

Since then I’ve done lots of work stuff, some of which I've done some coding as a natural occurance of the work, and been lucky to have the chances to do some hacking (one of the joys of [running my own thing](http://www.studioofthings.com/)). Some of those hacks I blogged about:

* A couple of hours writing [a web app that tells me if I can hang the washing out](http://www.ermlikeyeah.com/weathering-a-two-hour-hack/)
* A lunchtime [hacking my local council’s website’s stylesheet to create a responsive version](http://www.ermlikeyeah.com/try-something-new-to-something-already-there/).

All that work all that stuff has sharpened my skills again - and helped push on the shape of this abandoned idea resting at the back of my mind.

It's not the only idea I've had in the holding bay of my brain. Sometimes ideas do need sketching initially and then leaving. Over time you come up with some of what to do, either by working out what you need to do, simply finding the time, finding someone who can help you, or whether to dump them. (I've hinted previously about the idea of "[think-walks](http://www.ermlikeyeah.com/a-dog-one-year-on/)", taking an idea with you on a walk.)

So, Sunday breakfast the rest of the family were upstairs watching and playing with various screens. I had nothng better to do, but thought I'd open up my Macbook and have a go at the Eventbrite project again, from scratch. I felt I'd thought it through a bit more - learning from my initial failure a few months back and building on top of that.

In 90 minutes (which is longer than your average breakfast, but it was Sunday) I’d managed to get the Leeds data from Eventbrite, slurped in and spat crudely and unordered into the browser, with no errors. Progress! I marked the occasion with a celebratory tweet!

<blockquote class="twitter-tweet" lang="en"><p>Quick brekkie hack: list upcoming Leeds events on Eventbrite. To do: order by date, prettify, add other data sources. <a href="http://t.co/46793BrVcX">http://t.co/46793BrVcX</a></p>&mdash; Simon Wilson (@IdleSi) <a href="https://twitter.com/IdleSi/statuses/498397600694173696">August 10, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

A little later, after getting ready, I grabbed half an hour to get that Eventbrite data sorted chronologically. In a couple of hours' work I had cracked out what I originally set out to do months ago.

<blockquote class="twitter-tweet" lang="en"><p>And now orders by chrono. Magic. Will improve when get odd hour here and there. Also: You&#39;re welcome! <a href="http://t.co/46793BrVcX">http://t.co/46793BrVcX</a> <a href="https://twitter.com/hashtag/Leedsevents?src=hash">#Leedsevents</a></p>&mdash; Simon Wilson (@IdleSi) <a href="https://twitter.com/IdleSi/statuses/498408267086045184">August 10, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

During a dog walk ([dog walks, again!](http://www.ermlikeyeah.com/a-dog-one-year-on/)) I thought about how what I had written could easily be scaled to take in more. This is a evolution that I had planned as well, especially from chats with busy event creating people like [Emma Bearman](https://twitter.com/EmmaMBearman) who had mentioned how they have to do so much date checking for *other events* as part of planning their own events.

In the afternoon I grabbed a couple of hours to get data from Lanyrd merged in with Eventbrite data. Lanyrd seemed a small grab - there wasn't lots of data there, but I knew Leeds folk used/loved it (looking at you, [Matt Edgar](http://mattedgar.com/)) and it would also be a good test subject for scaling the data imports. This was easier than I thought, as Lanyrd has RSS feeds much like Eventbrite (albeit formatted neater).

At the same time as the feeds' locations were variables I did a little tweak so I could get, and look at, Bradford data to go with the Leeds data. (I live in Bradford.)

By the end of Sunday I'd spent about four hours scattered over breakfast and gaps between dog walks, cooking meals, eating meals, going to the gym, and the like. It felt like a highly productive day and also a relaxing day.

Monday, back to work, but I found 90 minutes over breakfast to hook the system up to Meetup, add Manchester and New York data sources, and create a version that generated static HTML files to save the server load. In the evening I used 90 minutes to prettify the pages (responsively, naturally).

<blockquote class="twitter-tweet" lang="en"><p>And now orders by chrono. Magic. Will improve when get odd hour here and there. Also: You&#39;re welcome! <a href="http://t.co/46793BrVcX">http://t.co/46793BrVcX</a> <a href="https://twitter.com/hashtag/Leedsevents?src=hash">#Leedsevents</a></p>&mdash; Simon Wilson (@IdleSi) <a href="https://twitter.com/IdleSi/statuses/498408267086045184">August 10, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

This morning I took three quarters of an hour to create XML files from the data collected so people could access the collated data in a raw format.

About the same time a couple of people asked if the events could be grouped together clearly by date to make reading clearer, which took 20 minutes to code, debug, and put live. And their advice was right. It does read better. (Protip: Always listen to your service's users.)

<blockquote class="twitter-tweet" lang="en"><p>This morning&#39;s <a href="https://twitter.com/hashtag/breakfasthack?src=hash">#breakfasthack</a>: a small one, adding XML feeds for the locations to <a href="https://twitter.com/hashtag/eventmasher?src=hash">#eventmasher</a>. (Link: downthe page.) <a href="http://t.co/7C6Eknviaw">http://t.co/7C6Eknviaw</a></p>&mdash; Simon Wilson (@IdleSi) <a href="https://twitter.com/IdleSi/statuses/499100968256929794">August 12, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

In total so far I've spent about nine hours on the hack. (If you're looking above adding up, there's a couple of small things not noted above.)

This isn't a huge amount of time given how quickly I got a minimum viable product out (less than half a day on Sunday) and the number of progresions already to push the original product forward. I've had fun scrapping with XML and designing within the browser (Photoshop was only used to grab some colour references).

It *will* help me find events to go to - and help me find appropriate times to hold my own events. Whether you find it useful or not, your call. Do have a look and let me know what you think.

But my biggest takeaway here: Sometimes the best way of doing things is to let the idea stew so you have it worked out comfortably.

**You view the site at [www.studioofthings.com/eventmasher/](http://www.studioofthings.com/eventmasher/)**

*For any future suggestions and work for the event masher project there is [a Trello board](https://trello.com/b/oSlDAC08/leeds-events-masher).*
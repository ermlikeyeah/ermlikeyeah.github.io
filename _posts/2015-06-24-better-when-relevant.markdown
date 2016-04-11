---
layout: post
title: 'Better when relevant: improving the Hang My Washing Out tool'
date: '2015-06-24 15:39:04'
---

I’ve been looking through some older work recently. Some of it purposely. Some of it accidentally.

Purposely: I've been looking over stuff I've been involved with over the years. Sometimes it's good to reminisce.

Accidentally: I was reminded this week of a little hack I pulled together last summer, a little hack that tells me if I should hang my washing it out.

I got an email earlier this week from someone who uses the hack/app/service. I’d forgotten I’d rattled the app into existence until that email.

The email said the “app” wasn't working quite right. I was surprised that someone was actually using it.

I’d made it as a throwaway thing, one part user centred solution, two parts a test to see if I could come up with something to solve a problem: We were having a week of wet/dry/wet/dry etc weather and wanted to know if I could get the washing out that day. I wanted to solve it  as quickly as possible. I’d cobble it together in whatever form in a couple of hours downtime, nothing more.

([I blogged about the thinking and making of this app back then.](/weathering-a-two-hour-hack))

Back to the present: The emailer said they used it regularly, and it was on their phone’s screen so they could “get to it quick”. (I didn’t think people saved internet bookmarks to their phone’s home screen but here’s someone who does). The weather in the app they said, well, wasn’t the weather outside.

First, I left a little bad. The app should have shown errant weather a bit more than they were suggesting, because I’d left the evaluation logic a little… loose. (I'd done it in a strict two hours...) Second, I was thankful they seemed to be living locally to me as the app is hardwired only to look up the weather in Bradford.

A couple of emails were swapped between us.

I had to thank the person for getting in touch, how did they find out about the service? Someone had shared it on Facebook.

Why did they use it? They replied it just tells them if they should hang their washing out, it simply provides them answers to a real world problem, nothing more. No need to look through weather data, just a yes or a no.

I was enthused that this person just *trusted* the service I’d made. Partly driven by a sense of guilt I'd let something out not finished/buggy and someone relied on it I fixed the problem raised, and got back to them. Here you go, sorry, thanks for using it. Job done.

Not quite.

Last night I logged on and did some more fixes and improvements, including a look-up service so it now works out where you are (based on your internet connection) and uses weather data appropriate to that location. So it's not just about Bradford any more. It's about where your web connection thinks you are.

And I spent half an hour putting in some logic so it constructs and presents a response in English rather than just a Yes/No and some numbers. Why? The person who emailed me said the app was a great idea, but it'd be even better for them if it “spoke to them”. So this felt a move in the right direction.

I pushed this new version live at 1am this morning.

I was and am chuffed the person thought this app is a great idea. For me ideas aren't great unless they solve real world problems, problems that matter.

This app, this thing, this idea that I thought was small and throwaway, did something I’d forgotten until I'd got these email and then I re-read [my blog post on making it](/weathering-a-two-hour-hack): It solved a problem that mattered to someone. It mattered so much they got in touch with me about it, to make it "better". That's the best feeling as a designer and a maker.

Oh, and you can find version two of the app over at [www.studioofthings.com/washingout](http://www.studioofthings.com/washingout). I apologise in advance if it's not quite right. But, you know where to [contact me](/contact).

*[Photo from Flickr.](https://www.flickr.com/photos/viktor_u/8028848433/in/photolist-detWVg-KL5Vi-raBL5-4BxFrP-8ZiW2j-58HYWr-cGYeiC-qbtHRd-4b6Mxz-ey1zqU-fUybWx-qzV9-3eEEF4-8ioK59-9enkQ-qvrSE-53VAVL-8pMLQB-i9Ggsn-9EJ4M-4se2Hc-4vGRwF-g1wjPY-e1vNUv-5393hb-nQisw7-rxsnP2-oCekEJ-oj21gu-6FSbSb-FVpXn-2orEFM-2A7XtC-nc9JGr-mmKx66-5zsr6w-4iaqyo-dJp6uC-ppXhhE-55ZRD2-rW9Rzg-pjhiA-rUBZ2c-qL9sAc-kMfwYZ-28Zdeq-3iMGMR-2aZbC1-qu53RX-6zBS47)*

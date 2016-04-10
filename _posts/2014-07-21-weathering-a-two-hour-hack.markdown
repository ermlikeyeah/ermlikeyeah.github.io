---
layout: post
title: Weathering a two hour hack
date: '2014-07-21 20:13:55'
---

After finding a little time [Friday lunchtime to hack about with Bradford council's website stylesheets](/try-something-new-to-something-already-there/), I found myself with some unexpected downtime today as well.

Towards the end of last week there were threats of thunderstorms across the UK. The [storms were spectacular](http://www.bbc.co.uk/news/uk-28366535).

As the storms hit buildings down south we were wondering if it was safe, here in Bradford, to put the washing out.

We're not a tumble-drier owning family, and to repeat that there we're a family. We get through clothes. So the warm weather means clothes can be washed, hung outside, and dry pretty quick at the mo. (Rather than, say, hung from the curtain rails in our bedroom.)

I joked that this is the sort of situation that an every day widget on our phones could solve - an *actually useful* widget, that says to you "Yeah, you can hang your washing out, at least for the next four hours - but that'll be enough with the current conditions to get everything up to a pair of jeans dry."

I joked. And yet I found myself at a little loose end, and still buzzing from having that quick play on Friday. What could I do? How hard could it be to wedge together a quick web-based prototype of this Can I Hang My Clothes Out idea?

With no up-front research I had a quick scoot through the most popular (with Google anyway) available online weather sources: BBC, Sky, weather.com, the Met Office, and Yahoo!.

I needed available data from these, which knocked Sky off the list straight away (no feeds). And for speed's sake I didn't want to mess around with registering with APIs - I just wanted a raw RSS/XML feed for Bradford for starters, just to get things going quickly.

The feeds all offered different ranges of data: [the BBC's was the simplest files](http://open.live.bbc.co.uk/weather/feeds/en/2654993/3dayforecast.rss), but also the least useful to me, providing just pre-written forecasts of the weather. I didn't want those: I wanted data, I wanted numbers (temperatures! wind speeds!) and scenarios ("partly cloudly"!).

I thought I would get the data in and on-screen quickly. I can honestly say I spent longer on this than I thought, just over an hour, yet discovering each feed's strengths and weaknesses by playing with them, coding on the fly to parse (or try to parse) in PHP.

For this experiment Yahoo! provided [the sweet combination of the type of data](http://weather.yahooapis.com/forecastrss?w=13527&u=c) I needed, along with its ease to parse. (SimpleXML was a Godsend.) I used some ECHO commmands to get the data I needed on screen quickly (*current temperature* and *current conditions*), and then hammered together some rough HTML and CSS to make the data more presentable (which I mainly ripped from another project, hence the handy icons in place already). 

I've put the project online so [you can view it, off the Studio of Things' web server](http://www.studioofthings.com/washingout/index.php).

What I have is a prototype, done in two hours. It was a frenetic and frantic couple of hours, I've created something that's nowhere near complete and very make do as I had other stuff I *really needed* to get on with - but it was also rewarding, hacking against the clock.

There's stuff I can do to iterate it further, much further, and when I get some spare time over the coming weeks I'll have little chips away at it. I tied up the work today by quickly setting up [a Trello board](https://trello.com/b/O3V8Jfli/shall-i-hang-the-washing-out) with a brain dump of progressions to consider and my notebook has some doodles of visual stuff I want to explore.

If you're curious, you can [view the experiment online here](http://www.studioofthings.com/washingout/index.php), and [the project's Trello board here](https://trello.com/b/O3V8Jfli/shall-i-hang-the-washing-out). Drop me a line with what you think, below or through the [contact page](/contact). And if there's anything you've "had a quick crack at" recently let me know too!
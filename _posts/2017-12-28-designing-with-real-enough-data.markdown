---
layout: post
title: Designing with real enough data
date: '2017-12-28 22:00:00'
---
At DWP a lot of people searches seem to be based around an individual’s National Insurance Number (usually called a “NINO” within the government).

A screen like this is not uncommon:

![](/assets/find-someone-using-a-nino.jpg)

On the services and digital products we work on at DWP Digital we need to design with correctly formatted data, the right number of numbers and letters in an order they should be in.

We also need to make sure we use fake correctly formatted data. That is we need to make sure we are not using any possibly real data: “Real enough”. Using someone’s real National Insurance number in our design work wouldn’t be good at all.

A few weeks back I was worried that I was using a possibly real NINO in some design work I was doing. I scrubbed the NINO and asked some colleagues over at HMRC if they knew of a list of fake NINOs we could use in our design work.

No list existed, but some rules about what a National Insurance number wouldn’t contain came back. We have used these to create two tools very quickly, using [CodePen](https://codepen.io). (“Very quickly” being about an hour for both.)

[Colin](https://twitter.com/htmlandbacon) made a quick tool to [generate a fake National Insurance number](https://codepen.io/htmlandbacon/full/vpXrgw/).

I created a quick tool for people to run the National Insurance numbers through to [Check if a National Insurance number is formatted correctly – or not](https://codepen.io/ermlikeyeah/full/gowjYL/).

The tools are not perfect – but they are done. They didn’t take long to pull together and are helping us in the short term (as we’ve a lot on). I also got to have a go at some front-end coding in Javascipt again, which was a bonus.

We’ve shared the tools with our fellow DWP designers and getting them all to check the NINOs in their design work.

We’ll hopefully improve these two tools as we go along. And we’ll make sure we use the tools in future as well. WHich is handy for me, as I need to get a prototype running from seven different National Insurance numbers. I now know I can get seven “safe” NINOs to work with.

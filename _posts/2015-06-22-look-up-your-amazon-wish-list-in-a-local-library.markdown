---
layout: post
title: Look up your Amazon wishlist in a local library
date: '2015-06-22 05:18:02'
---

Another Sunday, another little bit of a quick coding effort.

Following [last weekend's look up Amazon bestsellers in your library effort](//www.ermlikeyeah.com/amazon-lookup/), I received a number of responses. If you took the time out to contact me, thank you! It's good to see something that's me just having a play was described as "useful"!

A few asked if it was possible to apply the same approach to Amazon wishlists. So I've had a go at that.

Knowing I could have a chance of a spare half hour early evening, I did a little research while walking the dog. One of the first problems was Amazon wishlists are not like their bestseller pages - they do not provide readily formatted data for us to just pick up (the bestsellers has RSS/XML feeds we could just look up).

However, HTML is data of its own kind, so I had a look at the code of a wishlist page (which you can do too - go to your wishlist page and select the *view code* option in your browser, if you're curious) and found that all my wishlist entries had a little bit of information against them that indicated they were *wishlist items*: `a id="itemName_`

So I wrote a little bit of code that takes in the HTML code for my wishlist page. It then looks for all the lines with `a id="itemName_` on and stores a list of them.

Unfortunately I was only working on the first page of my wishlist so this meant I only had my most recent 20 entries on my wishlist to work with. At the same time, this made life a little easier as it meant I was only working with 20 entries!

I then extracted all the data on each line by pulling out anything that was between speech marks - there are four items per line. But I only needed to show the second and fourth: *the book name* and *the book's URL on Amazon*.

Knowing we only had 20 books' details the program enters a loop, working through a book at a time to show stuff on screen for visitors to the web page.

The loop displays the book name, simple enough. Then I wanted to create a URL to a library system. If you remember last week's effort, we needed the ISBN number to feed into the library system. This is in the Amazon URL, so I wrote a little bit of code that lifted that 10 character code out of the URL and "spits it out" as part of a web link (to the Leeds libraries system).

Last week I also discovered that Kindle books make up a big part of my wishlist and the library systems don't seem to return those. Again I intriduced a "warning" - Kindle books seems to have an ISBN that starts with *B*, so the code runs a quick check. If the ISBN starts with B, put a little warning up.

And that's it! Total time spent: just less than an hour this time. (And not including the little bit of research while I was out with the dog.)

You can view my wishlist by visiting [www.studioofthings.com/books/amazon-wishlist.php?wishlist=39JNF1CTQYIJ1](http://www.studioofthings.com/books/amazon-wishlist.php?wishlist=39JNF1CTQYIJ1)

If you want to insert your wishlist, take the web address below. Do you see everything after`wishlist=`? Replace that with your wishlist ID. You can find by visiting your wishlist on Amazon. My wishlist URL is `http://www.amazon.co.uk/gp/registry/wishlist/39JNF1CTQYIJ1` You can see my wishlist ID is everything after that last `/`: `39JNF1CTQYIJ1`. Can you see that in the URL? That's what you need to find and replace!

So, if your wishlist ID is `ABCDEFGHIJKLM` you can create your look-up page with the URL `www.studioofthings.com/books/amazon-wishlist.php?wishlist=ABCDEFGHIJKLM`

If you live in Bradford you can force my system to search Bradford libraries, by adding `&location=bradford` into the URL. So: `www.studioofthings.com/books/amazon-wishlist.php?wishlist=YourWishlistID&location=bradford`.

So, my wishlist look-up pushing a search into Bradford libraries' system is [www.studioofthings.com/books/amazon-wishlist.php?wishlist=39JNF1CTQYIJ1&location=bradford](http://www.studioofthings.com/books/amazon-wishlist.php?wishlist=39JNF1CTQYIJ1&location=bradford)

None of your data is taken and stored by this system, by the way. It just looks up your page "on the fly", pulls out what it needs to show it, and that's it. Nothing is squirreled away secretly.

Likewise, any council library system that uses the Capita Discovery system can be "used", like Barnsley's. The Capita Discovery "location" for Barnsley is `barnsleymbc`. So the URL is `www.studioofthings.com/books/amazon-wishlist.php?wishlist=YourWishlistID&location=barnsleymbc`. Maybe at some point I could get a list of all the libraries that use the Capita Discovery system.

And that's it. Thanks again if you replied last week. It was some of those replies that got me thinking about this latest "quick code". I apologise again it isn't the neatest and a little looser than last week's, but I didn't have loads of time (and partially on purpose). As a little "proof of concept" it does the job.

As always let me know what you think, good and not-so-good! You can post comments below, get me on Twitter at [www.twitter.com/ermlikeyeah](//www.twitter.com/ermlikeyeah), and email at [si@studioofthings.com](mailto:si@studioofthings.com).
---
layout: post
title: Look up Amazon bestsellers in the Leeds/Bradford library system
date: '2015-06-15 07:24:42'
---

I had a quick half hour at the weekend to pull together a quick thing that sits between two big databases. Normally I’d call this a “hack”, but some of you might think that suggests something illegal. No laws were broken in the making of this thing! If we have to jargonise it let's call it a "data linker".

I have a lot of time and curiosity for libraries. Amazing places with amazing resources. There’s some interesting debates about the role libraries can play within society now and forwards.

At their most base libraries are delivery mechanisms for books, books from an archive.

A few friends recently have said they’re off on holiday, and they’ll take a book with them. How? They’ll see what’s “popular”. Going on holiday is a time to unwind, not time for books on “management and all that”. It’s about escapism. So they look up the top sellers, in the weekend papers, at Waterstones, on Amazon.

Some of those friends are also “watching the pennies”, so regularly go to their local library.

With this in mind, I wanted to see if I could link a list of “popular” books and make easier the process of looking up that book in a library database.

And: I only had half an hour to do it while the potatoes cooked.

A quick scoot on Waterstones website found nothing easy I could refer to, but Amazon provide RSS feeds for some of their bestseller lists. This gives us data we can look at.

The Amazon data itself just gives me the top ten, and within that data are a few bits we can pull out (with a little jiggery pokery), like the ISBN number of the book and whether it is an ebook.

I live in Bradford and I work in Leeds, so if I can serve both areas, great. A check on both councils’ websites shows they use the same system for an web-based catalogue of their books, meaning what I used for one council’s libraries I could use for the other city’s. And after a little exploring I found I can feed a search into that system by ISBN number.

So, I wrote a quick tool that:

* Reads an Amazon bestseller list
* Pulls out the book’s name, ISBN number, and whether it is an ebook
* Creates a link to the Leeds/Bradford library web service to allow the user to look up that book on the council system

Nothing massive. It took my half an hour to do this, with fifteen minutes a little later to add in several more lists beyond the “top bestsellers”. You can see it at [www.studioofthings.com/books/amazon-bestsellers.php](//www.studioofthings.com/books/amazon-bestsellers.php).

There’s plenty more I could do around and on top of this.

For example: It doesn’t look that great.

Another example: At the moment my data linker doesn't say if the book is available in the library system or not. Can the list actually say “this book in unavailable” instead of the user having to click?

Yet another example: Can I link this to other websites’ data, other than just Amazon’s?

And another example: Could it create an aggregate “top” list from a number of sources?

It has scope to do more, but in half an hour it does a job. 

What else do you think it could do?

**You can find the little look-up tool [at this link](//www.studioofthings.com/books/amazon-bestsellers.php).**
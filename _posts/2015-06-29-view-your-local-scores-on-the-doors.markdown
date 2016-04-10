---
layout: post
title: View your local Scores on the Doors
date: '2015-06-29 05:23:53'
---

This weekend's "hack" was inspired by my ritual Friday night trip to my local curry house to pick up a takeaway.

The routine: I walk to the curry house, order the curry, nip to [Symposium](http://www.tripadvisor.co.uk/Restaurant_Review-g186408-d1318551-Reviews-Symposium_Ale_Wine_Bar-Bradford_West_Yorkshire_England.html) for an ale while it cooks, pick up curry, go home, eat.

On Friday I overheard a quick natter about the Score on the Door sticker.

"How many of those do you think there are in Bradford?"

If only there was a way to find out...

The scores are a [Food Standards Agency](www.food.gov.uk) standard. They are collected by the local authority and the FSA website holds [a searchable database](http://ratings.food.gov.uk/) on all submitted scores. A little digging reveals they have [an API](http://ratings.food.gov.uk/open-data/en-GB). Which means we can get data, hopefully useful data.

So, off we go.

I was interested in Bradford. The FSA's website holds files generated daily for each "location". I found the file for Bradford, and wrote something in PHP that grabbed the file for Bradford (whose location code is 404), went through the file and gave me a total number of "entries" for that location.

Looking closely at the data I found some venues were marked "exempt", so I revised my code to remove the exempts from the total. This left **3639**. So curry house query answered.

Also in the data was the ratings for each venue. So I added in some more code that built up "buckets" for each rating. The totals for Bradford were:

* Exempt: 273
* One: 193
* Two: 133
* Three: 334
* Four: 621
* Five: 2077

I neatened that by getting the code to add on a percentage afterwards. Next: The program worked out an average based on the "live" venues for the location (ie. Bradford). Done!

You can see the results for Bradford [over here](http://www.studioofthings.com/dev/playground/livefoodratings.php?locationcode=404). It runs off live data, so is a little slow but should return results within five seconds.

I then realised that if I had the code for Bradford (404, remember), I could feed this program any location code. This turned out my biggest hassle - getting all the locations and their codes, mainly as accessing the API wasn't too clearly documented. (This is often an issue.) Once I had access to the data, [displaying a list of locations and linking to the earlier program was simple](http://www.studioofthings.com/dev/playground/livefoodauthorities.php).

And to finish it off I added some detail so you could see breakdowns of what venues got whatever score. [Have a look for the 5 rated venues in Bradford yourself](http://www.studioofthings.com/dev/playground/livefoodratingsdetail.php?locationcode=404&scorecheck=5). I made sure I included the "date rated" in the output to give the viewer a sense of context (ie. a few years old to recent).

Again, the outputs are rough and ready, but an easier hack this weekend (issues about how to actually query the FSA API aside) than the previous weekends' [Amazon wish list](http://www.ermlikeyeah.com/look-up-your-amazon-wish-list-in-a-local-library/).

As always, comments welcome, below, [on Twitter](http://www.twitter.com/ermlikeyeah), or [by email](mailto:si@studioofthings.com).
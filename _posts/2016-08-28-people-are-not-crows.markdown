---
layout: post
title: People are not crows
date: '2016-08-28 08:30:00'
---
For starters, a quick bit about some of the work the [NHS.UK team](//transformation.blog.nhs.uk/moving-to-beta) in Leeds I am in is currently looking into.

Time and time again in research sessions people say they go to their doctor because, as someone we spoke to put it succinctly: “My doctor is the door to whatever I need for medical things.” This is a highly shared view by the public and the organisation itself: [A GP](//www.healthcareers.nhs.uk/explore-roles/general-practice-gp) is recognised as many patients’ first point of contact with the NHS by the NHS’s service design.  ‘First  point of contact’ in NHS speak is ‘primary care’. You can [read more on primary care here](//digital.nhs.uk/primary-care).

The NHS is a big thing with lots and lots of services to the people that use it. Patients, current and potential, need guiding to the right place and people.

Those patients don’t need to do the work, shouldn’t need to understand the structure and systems of the NHS to get help.

About 90% of patients’ interactions with the NHS are on a primary care level, and primary care isn’t just GPs.

In recent research sessions we’ve been hearing about people’s experiences with pharmacies. The thing is, this isn’t what we were primarily looking for. We were initially looking into patients’ experiences with doctors: Their GP, and when they were “away”. We were hearing in our research sessions about what people did when their GP wasn’t available: Their GP’s surgery was closed or they were not near their GP’s surgery.

We had a chart hung up that shows when general practice surgeries tend to be open. Seven circles for each day of the week. Each circle was a 24 hour clock showing the average opening times of practices. Basically, 8.30am to 5.30pm on weekdays. 9 hours. The remaining 15 hours in the day? At weekends? People wait – or they use other medical services.

Out of hours services, walk-in centres, accident and emergency centres, minor injury units, pharmacies, NHS 111, dialing 999. I think I’ve missed some places out of that quickly tapped out list. But so many choices. And so much confusion about what each does and why you would go to them and when. It’s easy to see why people would just go to their GP. Contacting a GP is a default state of mind.

“My doctor is the door to whatever I need for medical things.”

While this research was going on, the team in London were releasing their [beta stomach ache page](//beta.nhs.uk/symptoms/stomach-ache), which advises you an action you can take, even somewhere to go if appropriate. When we do that we’re just trying to point you to someone and somewhere that can help.

A lot of research has gone into that stomach ache page (which is still working on, with a lot of other stuff), and in that page is the suggestion the patient can go to a pharmacy.

From our own research and using the beta stomach ache page’s prompt we thought why are we not directing people to a pharmacy there? Some people will know their preferred pharmacy. But what if it is closed? Some people may be away from their “locality”. And some people, maybe they wouldn’t have considered going to a pharmacy in the first place. Is this an opportunity for some positive disruption? What if people even think “I didn’t realise my pharmacy could help me wit that?”

So, we theorised, what if there was an action on that page?


![Screen grab of the stomach ache symptoms page](/assets/stomach-ache-symptoms-grab.jpg)

We decided to test the hypothesis. We hurried through making a prototype. (And [here’s a quick reminder about what a prototype is](//www.ermlikeyeah.com/a-short-note-about-prototyping/).) Less chin stroking, get the idea down, and then take it from there. Because of the pace we were quite hacky. We knew there’d be flaws, gaps, bugs, things missing, but we wanted to validate or invalidate the hypothesis.

One thing that seemed key was bringing real data into the prototype early on. Put people in their own moment, not get them to imagine they were somewhere else. The developers on the team worked fast to grab data from [an openly available NHS feed](//v1.syndication.nhschoices.nhs.uk/?apikey=bbccdd). We would also be testing the data by testing our idea.

We also found time to take the data and apply some context - geography was the easy one (show only what was “nearby”), but also time (show only what was “open” now).

We took the prototype into a lab.


In the lab the idea is getting a good grilling. We’re getting people telling us moments when they would have ended up on something like this (if they would have), what works for them, what doesn’t work for them, how it’d be good to extend it to more than just pharmacies, and “Wait. That’s not my nearest pharmacy.”

![Screen grab of results page](/assets/stomach-ache-results-page.jpg)

“Why do you say that?”

“Because those pharmacies on there, none of them are the one that is nearest to where I live. The one that is nearest is just at the end of my street. Your distances are wrong. Or you are not showing it for some reason.”

Because we’d worked fast we took the distances provided by the feed. We look later. Those distances are point to point in a straight line, as the crow flies as it were. We can make this better, we can get distances that are “As people travel” not “As crows travel”.

This week we’ve been looking into that. It’s reasonably straightforward work to do. And a reminder you’re only as good as your data and your sources. Think of the context of that data, and then the context when the data is presented as information. It does matter to people.

As Steve, one of our developers put it: People are not crows.

![People are not crows](/assets/people-are-not-crows.jpg)

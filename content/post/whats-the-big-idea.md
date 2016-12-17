+++
title = "What's the big idea?"
description = "A brain dump"
date = "2016-12-17T14:17:56Z"
draft = false

+++

![alt text](/images/post/whats-the-big-idea.jpg)

What is it about Birdr that keeps me coming back? I guess I have this feeling that, if done right, Birdr could become as ubiquitous to birding as YouTube is to videos. It would serve as the place to go to keep all your lists & photos. The place to find out about rare birds in your area. The place to read about birding in remote locations and the place to share knowledge and offer encouragement to new birders. This is the vision I have and what keeps me coming back.

Below is a list of features that I hope to add to Birdr:

### Bird Records

Every birding application needs the ability to add records. The key to success here will be providing a simple interface. If recording birds is too much effort people won't do it. Birdr should allow you to record as little or as much detail as you wish.

#### Weather

One of the cool things I've added in the [NENBC](http://nenbc.co.uk/) application is an automatic weather report. If you add the location and date/time of your record we can fetch the weather using a neat service called [DarkSky](https://darksky.net/dev/). Weather actually plays an important part in bird watching. On windy days you will often find rarities along the coast that have been blown over the seas.

### Lists

Birding is all about keeping lists. One of the must-have lists for birders is the life list. For a UK birder, this is the list of birds that you have seen within the UK shores since you started birding. Serious birders will have see upwards of 400 species. Once you get more into birding you might start finding you keep year lists, garden lists, lists specific to a particular county etc. Most applications, and [BirdLists](http://birdlists.me/) is no exception, place the onus of maintaining these lists on you. This can become a burden.

#### Smart Lists

What if we could do something better? What if, rather than having to tell the application which lists to add a record to, it just _knew_? What I'm thinking of is something akin to the 'smart mailbox' feature your email client may have. You would define a set of rules, such as:

* Must be seen in 2016
* Must be seen in the UK
* Must be on the [BOU list](https://www.bou.org.uk/british-list/)

And it would apply these rules to your records, automatically maintaining your 2016 year list. Want to teak the rules? No problem, edit the parameters and the list will automatically update.

If we have this feature it means the only thing you have to do is add your records and your lists will take care of themselves. Bliss.

### Photos

A lot of birders have started getting into photography. Whether that be through some serious SLR telephoto lens or digiscoping (a practice of attaching a camera to your telescope), bird photography is extremely popular.

Birdr will allow you to upload as many photos of your birds as you like. As they're attached to records we can build up a gallery of photos of every species. And give you a public gallery of your photos for people to comment and like.

### Trip Reports

Birdr will allow you to group records into a 'trip'. This trip will be a collection of maps, photos, lists and notes. You will be able to share this with your friends, or print it as a PDF. This could form a memoir of your birding holidays. Eventually, Birdr will house a library of trip reports from across the world. Off to Chile? Check out reports from other birders who have been there.

### Clubs

There are tonnes of bird clubs in the UK (and worldwide); my dad has started two himself! The concept is fairly simple. You form a club that has a designated recording area and your members report what species they see within this area. At the end of the year the club produces an annual report.

The problem is there is a lot of work for some poor soul who has been nominated by the club as the record keeper. Each year they must collate the records - not always submitted digitally - and produce a report. Wouldn't it be great if you could automate this?

Birdr will allow people to form clubs. You will be able to draw on a map to define your recording area. You will be able to invite and manage your users, perhaps even [managing payments](https://stripe.com/gb). All records will be available in monthly and yearly reports to all members, meaning your club record keeper is able to go out and enjoy birding!


### Gamification

Personally, I find bird watching a difficult hobby to get into. Unless you know someone who is a keen birder it can be extremely daunting. A concept in modern applications is gamification. To gamify something is to attach virtual rewards and targets to a hobby or process. For example, the popular software development Q&A site, [StackOverflow](http://stackoverflow.com/), has a great system whereby you earn badges for answering questions and helping to maintain the site.

Birdr will try and introduce the concept of gamification to bird watching. You will be able to earn badges for recording species, and there will be fun achievements for meeting certain criteria. For example, earning a 'flying kites' badge for reporting a Kite during high winds.

The hope is this will help on board new birders by suggesting badges they can aim for. These badges will get progressively harder and by the time they've earned the last one they'll be professionals!


### Rare bird alerts

One of the nice things about having a community of birders adding records into a central system is that it becomes trivial to providing rare bird alerts becomes trivial. Rare bird alerts is something that many keen birders pay good money for. Birdr will provide notification of rare species over push notification and text message - straight to your phone. This is something I have already implemented successfully on the [NENBC](http://nenbc.co.uk/) website. These notifications should be configurable at the club and individual level. Don't care about specific species? Turn off the notifications.

#### Reputation

One of the tricky aspects of a rare bird alert system is that sometimes newer birders can misidentify species. To send out a notification of a rare bird erroneously could be disastrous as many birders travel long distances to see them. To combat this I've thought about a reputation system. Newer birders will have a low reputation and so rare birds wont be notified immediately. Over time they will earn reputation points so that when they do report a mega rarity we can trust it and let people know.

### More advanced features

#### Image Recognition

Recently, Amazon Web Services [announced a new service for image recognition](https://aws.amazon.com/blogs/aws/amazon-rekognition-image-detection-and-recognition-powered-by-deep-learning/). This got me thinking, would it be possible to use such a service to try and identify species of birds in photos? It's a long shot, as most bird photos tend to be of small brown or black objects in the sky. Nonetheless, it is an interesting concept and one I hope to pursue.

Perhaps in the future you will be able to add records simply by uploading photos. The photo would contain date & time, location and we can use image recognition to identify the species. That would mean updating your bird lists simply becomes a case of plugging in your camera and clicking a button.

#### Machine Learning

Machine Learning (ML) is another interesting concept. There are several areas where I feel ML could be utilised in Birdr. We could use it to predict which species might be seen at a given location on a given day. This could form a sort of "what should I expect to see?" feature. It could also be used to identify dubious records. This could provide a safety net for new birders who are about to report an unlikely sighting.

Machine learning is a very hot topic in software development right now and something I will be aiming to use extensively in Birdr.

### Any other ideas?

These are some of the things I've been thinking about over the years but I would love to hear from you. If you have any ideas please leave a comment below.

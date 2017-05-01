---
layout: post
title: "Finding empathy in 604,596 lines of migration data"
description: Irish Ships is a Twitter Bot that is tweeting its way through every human being to have arrived in New York Harbour during the Great Famine in Ireland (1846 - 1851)
date: 2016-09-01 00:00:00
categories: [jekyll]
tags: [twitter, bot, data, scraping, python, Ireland, history, migration, portfolio, humanism]
image: /img/post/2016-09-01-humanising-data-with-irish-ships/3-irish-ships-1.jpg
image-source: https://www.flickr.com/photos/lennox_mcdough/10389431924/in/photolist-gQ5y9C-pUvV5X-9GJMw5-qyQHuc-88YMJT-5VhvAe-f2Y95t-pgcmxD-oYZjBm-oYZDHg-76odQz-8RQ1oZ-8Qd5pN-brsFHm-H2xiu-H2CTM-92qU3Z-8MbJMS-6mx7k9-7M3YTP-7HraDF-nnvxK4-5TbYir-dZAfkZ-dKnMPH-pJ8J8A-5pGRXQ-q3FN5N-7vfAFk-86Qb9Z-fDa9iR-jeZug9-6fMujm-6wNmZj-86Tgw1-jeXjz7-ntGEUp-92qUfH-brsF6j-oYZafL-GdTJqa-egRXk9-zsejUL-5pGPnQ-qySeU6-b25Rpk-buxqF8-qP1cg9-ebKKVX-6Nki8U
image-author: Tobias Abel
---

600,000 human beings - can you picture them? You're visualising a large group of people - you can appreciate that it is vast in size. Perhaps you can't make out the individuals - understand even the simplest things about them, their name, their age or how they relate to each other?

It's not easy thing to do, but it's important. Empathising with those we don't know is one of the greatest things that we can achieve as people.

![Irish Ships: The Great Hunger Twitter bot](/img/post/2016-09-01-humanising-data-with-irish-ships/3-irish-ships.png "Irish Ships: The Great Hunger Twitter bot")

Large, single numbers reduce, they can deny the human that they speak about. We see this around us everyday, particularly in the media - recent reporting on the migration crisis affecting Syria, parts of the Middle East and Europe has done little to educate viewers and help them understand and empathise with those affected. Numbers and data are tools to shape arguments and push policies (Brexit), denying basic rights, forgetting the fact that there is a person at the heart of a crisis like forced migration.

### A "swarm" of migrants

In July 2015, David Cameron used the word [Swarm](http://www.theguardian.com/uk-news/2015/jul/30/david-cameron-migrant-swarm-language-condemned "David Cameron Migrant Language"){:target="_blank"} to describe migrants in the 'jungle' in Calais. This rhetoric struck me as dangerous. It dehumanised those in need and shifted a conversation with real things at stake into a two dimensional, us and them framing.

It was this rhetoric, the use of language as a weapon that had me consider what could be done to subvert the message that Cameron was pushing and begin to shift the focus upon individuals and their stories.

I decided to act creatively, to attempt to tell a story around human beings, not numbers or statistics.

### Migration and story-telling

I began by researching other creative attempts to foster empathy in the viewer and found a number of creative pieces that informed the final output of my work. The outstanding article [Notes on the Syrian exodus: Epic in scale, inconceivable until you witness it](http://www.theguardian.com/world/2016/mar/05/great-syrian-refugee-crisis-exodus-epic-inconceivable-witness-lebos-islamic-state "Notes on the Syrian exodus: Epic in scale, inconceivable until you witness it"){:target="_blank"} by author Richard Flanagan, is heart wrenching - its focus on the individuals forced to leave their homelands by war, fear and death. Other examples include a [scroll](https://twitter.com/rmw/status/594156245734535168 "Migrant Scroll Game"){:target="_blank"} featuring the names of migrants who had drowned in their attempt to cross the Mediterranean that was rolled out along the hallways of the European Parliament. Also a browser based game called ['Passenger'](https://boingboing.net/2015/08/25/passengers-is-a-game-about-the.html "Migrant Passenger Game"){:target="_blank"} that puts the player in the role of the a human trafficker, transporting people across the sea to Europe.

Alongside this research I also considered the history of my home country Ireland. Ireland has a long history of emigration. It is a foundational part of my nation's identity. **It is a part of me.**

![Irish Ships: The Great Hunger Twitter bot](/img/post/2016-09-01-humanising-data-with-irish-ships/3-irish-ships-1.jpg "Irish Ships: The Great Hunger Twitter bot")

### The Great Hunger

In the mid nineteenth century [Ireland faced the specter of famine](https://en.wikipedia.org/wiki/Great_Famine_(Ireland) "Irish potato famine"){:target="_blank"} so severe that approximately 1 million people perished and a similar amount fled across the sea. The population dropped by 20-25% and has never recovered - fascinating. The majority of these migrants made their way to Liverpool and from there across the Atlantic ocean to the port of New York. Upon arriving they were processed by officials, their information documented in ledgers - name, age, country of origin, port of embarkation etc..). This data exists today in digital form and is hosted online - unbelievable.

To me this was an excellent raw material that I could employ to try and tell a story about human beings and migration. I wanted to take this data and contextualise it in a modern setting - pointing at the idea that migration is not something that is new and if managed correctly, it can be a force for good and benefit to all of our cultures.

I began by writing a Python script to scrape the data from tables hosted on over 12,000 webpages, into 450mb of CSV files. From here I wrote another Python script that generated 604,596 tweets from the data in each row in the CSV file. The structure of each tweet allowed me to highlight the name of the individual, their age, their country of origin and their port of embarkation. Next I employed the Twitter API and Python again to create a [Twitter Bot "Build a Twitter Bot with Python"](http://marydickson.com/build-a-twitter-bot-with-python/){:target="_blank"} that would Tweet one line, or one individual, every 30 minutes. I called it [@IrishShips](https://twitter.com/IrishShips "The Great Hunger: @IrishShips"). .

### @IrishShips

The goal of this personal project was to subvert the rhetoric of language that can dehumanise and negate the individual - to find a better way of telling stories with data, that doesn't rely on a single large number or statistic. By employing Twitter as a medium I was able to draw focus on individuals in a performative way, over time.

This was one step towards thinking differently about how we tell stories about the challenges in our world. How data can be used to foster empathy in people, to try and recognise the other as not a shadow, but a reflection of oneself.

### Links

**1)** I've included a link to the Github repository for the Python script I've employed to Tweet every 30 minutes. You'll find it [here](https://github.com/langphil/-.txt-_twitter_bot "Twitter Bot Repository on Github"){:target="_blank"}.

**2)** The original archive of 12,000 web pages from which I scraped the data can be found [here](https://aad.archives.gov/aad/fielded-search.jsp?dt=180&tf=F&cat=TS20&bc=,sl "AAP Archive"){:target="_blank"}.

**3)** The @Irishships Twitter account can be accessed [here](https://twitter.com/IrishShips "The Great Hunger: @IrishShips").

**4)** If you'd like to read more about the Irish Famine, then do check out "The Great Hunger" by Cecil Woodham Smith. It is superbly researched, fascinating and well worth a read. [Get it here](https://www.amazon.co.uk/Great-Hunger-Ireland-1845-1849/dp/014014515X/ref=sr_1_1?ie=UTF8&qid=1463857493&sr=8-1&keywords=the+great+hunger "The Great Hunger Book"){:target="_blank"}.

**5)** Cue some shameless plugging for an interview I conducted with the Irish World newspaper - ["Todays refugees are like 19th century Irish"](http://www.theirishworld.com/todays-refugees-like-19th-century-irish/ "Todays refugees are like 19th century Irish"){:target="_blank"}

**If you'd like to find out more about this project, please get in touch - [plangphoto@gmail.com](mailto:plangphoto@gmail.com "Get in touch")**

***

*Ship image licensed via the [Noun Project](https://thenounproject.com/term/boat/5263/ "Image credit")*

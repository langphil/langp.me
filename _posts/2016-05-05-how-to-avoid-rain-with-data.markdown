---
layout: post
title: "How to avoid rain, with data and the Internet Of Things"
description: Rain-Pi is a prototype IOT device that signifies when rain is due in the next period by turning on a blue LED when there is more than a 70% chance of rain.
date: 2016-05-01 21:00:00
categories: [jekyll]
tags: [iot, data, data radiators, raspberry pi, making, portfolio]
image: /img/post/2016-05-05-how-to-avoid-rain-with-data/2-data_rad.jpg
image-source: Phil Lang
image-author: Phil Lang
---

If you're anything like me you don't particularly like getting caught out in the rain (unless there are pina coladas involved). Like me you may also yearn to be less reliant on your phone for obtaining information and making decisions.

One of the first things I do in the morning is roll over, pick up my phone and check if it's due to rain - do I need an umbrella today? Not a great morning ritual by any means. This caused me to spend a bit of time wondering how I could break this ritual, maintain exposure to this valuable weather data, but have it delivered to me in a less intrusive way. **Enter the data radiators.**

![Umbrella, LED and Raspberry Pi](/img/post/2016-05-05-how-to-avoid-rain-with-data/2-rain-pi.png "Umbrella, LED and Raspberry Pi")

### Data Radiators
I was introduced to the idea of a 'Data Radiator' when talking with my mentor. He described them as being devices that sit in our periphery, that live unobtrusively in our environments, radiating, or signifying with data. Think about a doorbell, it rings when a button is pressed, signifying a person wants to see you. Most of the time it just hangs there, high on your wall, wired through the building to a button on your front door. Those few times when it is in use, it's invaluable. Now imagine the person at your door is actually a visiting rain cloud, who has the courtesy to warn you that rain is on the way. Basically, I wanted to create the rain notification equivalent of the much loved doorbell. "Ding Dong, it's due to rain Phil", but maybe without the ding dong or the disembodied voice. An LED, let's go with a blue LED.

### Rain-Pi

With this in mind I set myself the task of creating a ‘data radiator’ that would signal the potential for rain in the next 12 hours. The concept was to employ a Raspberry Pi, Python script, weather API and a LED light to signal this upcoming rain event. A quick search online provided quite a few similar projects. I was keen to write something myself, so with a bit of inspiration from [this post in particular](http://www.howtogeek.com/140063/build-an-led-indicator-with-a-raspberry-pi-for-email-weather-or-anything/all/ "How to build LED indicator"){:target="_blank"}, I wrote the following [code](https://github.com/langphil/rain_notifier_rpi "Rain Notifier Pi").

![RainPi](/img/post/2016-05-05-how-to-avoid-rain-with-data/2-data_rad.jpg)

The final prototype pictured above is an empty vodka bottle that sits on my book shelf. The majority of the time it is simply a bottle. Whenever the Wunderground API returns a greater than 70% chance of rain in my locality over the next 12 hours, a blue LED turns on. This is immensely useful in the mornings, when I can just glance at my bookshelf to work out whether an umbrella is a necessity.

I've detailed the process for creating this device below and provided relevant links.

I've no doubt that this could be executed in a simpler way. If you've any thoughts on this then please [get in touch](mailto:plangphoto@gmail.com), or create a pull request.

Now go and play!

### The Process

**1)** Get yourself an RPI with [Raspbian](https://www.raspbian.org/ "Raspbian OS") and a PiBorg LED setup.

**2)** Install PiBorg by following the instructions at [Piborg](http://www.piborg.org/ledborg "Piborg / Ledborg"){:target="_blank"}.

**3)** Go to [Wundeground](http://api.wunderground.com/weather/api/ "Wundeground API"){:target="_blank"} & get yourself an API key.

**4)** Work out the [coordinates](http://www.findlatitudeandlongitude.com/ "Longitude / Latitude"){:target="_blank"} that you'd like to get notifications for.

**5)** Enter all three values (API, Lon, Lat) into the URL in line 9 of forecast.py

**6)** Set pop value (% chance of rain **0 - 100**) on line 21 of forecast.py

**7)** Setup up a [cron job](http://www.howtogeek.com/101288/how-to-schedule-tasks-on-linux-an-introduction-to-crontab-files/ "How to set up a cron job"){:target="_blank"} to run the script at intervals.

**8)** Your light should now turn on everytime the script runs and the percentage chance of rain occuring in your location is higher than the pop value you have set.

**9)** Find a pretty glass structure to place your pi within and put it on a shelf / rain jacket closet.

**10)** Wait for rain (not involving pina coladas)....

**If you'd like to talk to me about this project or anything else, you can reach me [here](mailto:plangphoto@gmail.com)**

***

**Image credits**

* Umbrella by [Paul te Kortschot](https://thenounproject.com/term/umbrella/795/){:target="_blank"} on the *Noun Project* (CC BY 3.0 US)

* LED by [Tamara Pasquin](https://thenounproject.com/term/led/48611/){:target="_blank"} on the *Noun Project* (CC BY 3.0 US)

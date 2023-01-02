---
title: "Hobbyist Game Programming - The Beginning"
date: "2013-07-28"
categories: 
  - "game-programming"
tags:
  - "software engineering"
---

## Let's do this!!!!

I've been itching to make a game for the iPhone for a few years now and I'm finally ready to take the plunge. I'm going to be updating this blog regularly, hopefully weekly, to keep everyone updated and to keep me honest. I haven't found too many detailed accounts of the creation of an iphone game online so I hope it will give some insight to future game makers.

## The Concept

One of my fondest memories as kid was my grandmother's annual garage sale. My dad, showing his entrepreneurship streak, would haul up a popcorn popper and a large amount of soda and my sister and I would help him sell it. I gained concrete experience with supply and demand, how customer service affected your sales (and tips... it also helps to be 8 years old), and how expenses affected how much money my dad handed me at the end of the weekend. My first attempt at a hobbyist video game will be to try to capture this experience in a simulation style video game in the vein of lemonade stand.

I've tried to keep it simple and turn based, since I do not have deep experience with graphics or physics engines. The basic mechanics are as follows:

\- Players will sell popcorn 10 weekends in a row (2 days to a weekend) in a quest to earn the most money at the end of the 10 week 'summer popcorn circuit'.

\- Players will have to buy supplies and set prices prior to each day. Since popcorn making supplies and soda don't really 'spoil', random events will occur between each weekend that cuts into left over supplies. The idea here is to try to force the user to be very precise with their supply and demand mechanics, only buying enough supplies to turn a profit that weekend, and buying enough of the correct supplies to maximize profit based on the weather.

\- Weather forecasts will be randomly assigned every day. Each type of day (sunny, blistering hot, raining, freak snowstorm) will affect how likely customers are to stop to purchase items and also which items they purchase.

## Technical Details

I'm going to be using [cocos2d](http://www.cocos2d-iphone.org/) and targeting only iPhones and iPod touches for the first release. As I near completion I'm also hoping to hire an illustrator to make it look awesome, but for now won't be worrying about graphics until all the gameplay mechanics are in place. If you know good illustrators please drop me an email!

In the V1 release I'm going to be releasing the app as a paid app rather than free with in app purchases, and will also not be including any extra things like gamecenter or social sharing. Those features are nice to have's that can be released in later updates, but my main focus is to ship a game and hopefully break even.

I will probably be posting more progress updates than anything but if enough people are interested in code samples and specific implementation details I could post some of those details as well. Let me know in the comments.

## Progress so far

So far I've managed to implement a menu, a primitive "day setup" screen that lets the player set the price of each bag of popcorn or soda and a single 'day' that runs through the simulation. The weather is hardcoded to sunny as well as the ratios that determine whether a customer will actually purchase an item (or both). See the video below for more details. 

<iframe src="//www.youtube.com/embed/EmvyO99VNKM" height="315" width="420" allowfullscreen frameborder="0"></iframe>

## Want To Stay Informed?

If you are interested in receiving email updates about the game or become a beta tester please enter your email below and I'll be in touch.

<!-- #mc\_embed\_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; } /\* Add your own MailChimp form style overrides in your site stylesheet or in this style block. We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. \*/ -->

Receive updates about the game:

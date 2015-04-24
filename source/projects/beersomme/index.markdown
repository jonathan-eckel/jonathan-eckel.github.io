---
layout: page
title: "beersomme"
#date: 2015-04-23 13:16
comments: false
sharing: true
footer: false
---

{% include reflink.markdown %}

## Intro and Motivation
I'm what you may call a beer connoisseur.  I like to keep track
of what beer I'm drinking and where I'm drinking that beer.
[Untappd] is a social network for beer with great functionality.  Users can ``checkin'' the beer they are currently drinking as well as specify a location (powered by [Foursquare]).
[Untappd] also lets you harness this checkin information, to 
search for a specific beer that is nearby.  But what if I'm craving a Dragoon IPA, product of Tucson AZ.  I know I can't find that in NYC, and so does the app, so the search fails.  This is my premise for creating beersomme; if I'm craving a certain beer, find similar beers nearby to recommend the best place to go have a beer (or two).

## Technology Stack -- follow the flow of beer

Overview of the app.  beersomme draws on two data sources, untappd and ratebeer.  the ratebeer data is used for generating beer recommendations.  untappd gives local beer information. This data is fed into a MySQL database.  The main python process 


[Untappd] gives local information.  By querying the local feed, I can find the _**n**_ most recent checkins.  This gives me information about what and where people are drinking.

In order to limit the number of API calls my app makes to [Untappd], I institute a caching mechanism to store bar and beer information locally.  Therefore, the app first checks whether there is sufficient information in the local database before making additional API calls.


I scrape beer descriptions from [Ratebeer].


{% img /images/beersomme_stack.svg %}

- Data Wrangling
   - scraping with Kimono and beautiful Soup
- NLP
    - nltk

## Algorithm
cosine similarity

## Validation?

## Closing Thoughts

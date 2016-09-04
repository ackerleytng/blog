---
layout: post
title: National Day Songs WordCloud!
description: "National Day Songs WordCloud"
modified: 2014-11-19
tags: [national day, songs, wordcloud, singapore]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true

share: true
---

I wanted to find out which words appear most often in our National Day songs, so here's a WordCloud!

![natday-songs-wordcloud]({{ site.github.url }}/post_images/natday-songs-wordcloud.png)

Here's what I did:

1. I got the list of songs from [here](http://www.straitstimes.com/singapore/dick-lee-unveils-2015-ndp-song-our-singapore-revisit-past-national-day-parade-theme-songs)
2. I googled the song titles for the lyrics, and then I checked the lyrics that I copied by listening to all the songs
3. I put all the lyrics into one text file, I duplicated songs as necessary (e.g. Home was used as the national day song in two years, 1998 and 2004). I also expanded the lyrics by copying and pasting choruses as necessary, so that the lyrics are written out as sung
4. I manually removed the contractions (I'll was replaced with I will etc). I think is fairer because then 'll and will won't be considered two different words
5. Used this [script]({{ site.github.url }}/post_downloads/parse-natday-songs.py) to generate the WordCloud

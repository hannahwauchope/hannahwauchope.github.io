---
layout: page
title: Trusting Trends
---

<img src="https://upload.wikimedia.org/wikipedia/commons/d/d7/Balaeniceps_rex_-Ueno_Zoo%2C_Tokyo%2C_Japan_-upper_body-8a.jpg" alt="pelican [CC BY-SA 2.0 (https://creativecommons.org/licenses/by-sa/2.0)]" align="right" width="496.32" height="330"/>

Often conservationists need to know when they can trust the population trend of a species. If you have 5 years of data that tells you your populations of Shoebills is declining, do you immediately start taking action assuming something is wrong? Or could this just be part of the natural ups and downs of the population? (For the record, this study had nothing to do with Shoebills in particular, I just think they're cool).

And equally, what if your vulnerable penguin population was increasing in number over three years - could you conclude they were starting to do better and reduce monitoring and conservation efforts? Or could this just be a bit of natural variation amongst an overall pattern of decline? 

This question doesn't only apply to single populations, but to large scale studies as well. For example, the Living Planet Index tracks population trends of thousands of species across the world, but can sometimes have populations with as little as three years of data. When summaries are made with trends from all sorts of varying time-lengths, is there a way to have an idea of how much more trustworthy a 3-year trend is from a 20-year trend?

I set up to try and answer this question. Using a dataset of tens of thousands of waterbird population trends, I wanted to know how likely it was that trends from varying lengths (of time) matched the longer term trends of the population.

![TheWrongIdea](/img/TT_1.png){: .center-block :}
This is a case of us getting entirely the wrong idea about a population trend from a data subset. If we had only surveyed the population in these 5 years we'd think it was doing brilliantly!

To try and figure out the chances of this happening, I took >27,000 long term waterbird population trends, and then took small chunks out of each one. I looked to see how often the chunks matched the longer term trend, like so:

![ChunkGif](/img/TT.gif){: .center-block :}

In this case the long term trend was negative. If a three year sample matched that, it was correct (tick), if it showed the opposite it was incorrect (cross) and if it showed an insignificant trend, then it was a "missed negative", as in, we missed that a negative trend was occurring. 

In this example, I was taking 3 year chunks from a 30 year trend. But I ran this with every possible iteration within that, e.g. a 10 year chunk from a 29 year trend, a 4 year chunk from a 10 year trend, a 7 year chunk from an 18 year trend etc etc, and found the number of times in each case that the chunk was likely to represent the full trend. And these are the results:

![Results1](/img/TT_Consecutive.jpg){: .center-block :}

The top right box shows cases where the sample and the long-term trend are "matching" (correct). As expected, the closer the sample and long-term trend are in length, the more likely the sample is to be correct. But even when the sample is quite close to the length of the long-term trend, it can still often be incorrect. E.g. if we have a 24 year sample of a 30 year long-term trend, it will only be correct 70-80% of the time. And a 10 year sample of a 30 year long-term trend will only be correct 50-60% of the time! 

But that doesn't tell the whole story, as the bottom left panel shows the amount that we get the opposite trend, and this almost never happens (<10% of the time). The middle two panels show what happens when the long-term trend is insignificant (not really going up or down), but the sample gives a significant positive or negative trend. We can see that this is pretty uncommon too. The final two panels show the situation where the long-term trend is positive or negative, but our sample is insignificant, and this happens a little more often. 

The take home from all of this is that the when we have a significant trend from a sample, it is unlikely to be the opposite of the long-term trend, and also unlikely to be erroneously picking up a trend when the long-term trend is insignificant. So a significant sample trend is likely to be correct!

This has big implications, as it means that a significant trend from a sample of even just a few years is likely to be correct. So if we detect that a population is declining, we should act now!

In the rest of the paper I investigate a bunch of other scenarios that provide some useful info (for instance, what about if we compared the magnitude of the slode, or take samples in intervals etc), see the paper <a href="https://github.com/hannahwauchope/hannahwauchope.github.io/pdfs/Wauchope et al., 2019 - MEE - TrustingTrends.pdf" target="_blank">here.</a> and all the relevant code [here](https://github.com/hannahwauchope/TrustingTrends).


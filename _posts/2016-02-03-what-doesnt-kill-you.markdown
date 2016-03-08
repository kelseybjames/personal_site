---
layout: post
title:  "What Doesn’t Kill You Makes You Stronger"
date:   2016-02-03 12:45:00 -0800
categories: ruby programming learning
---

Yesterday, we were working on a project to build a dashboard displaying various data about an online store, using a database pre-seeded with data. It was an exercise in ActiveRecord, and I really enjoyed it. I felt that I was getting the hang of queries, which led me to feel more confident than I had in at least a week.

In retrospect, I had gone from confident to cocky. I had neglected to make my methods modular, so instead of having neat methods in my models I could call to join other tables on the one I was using, I wrote out the joins separately each time. I justified it to myself by saying that I had a limited amount of time and that I could refactor later, but it would have been faster if I had done it properly from the start.

Even worse than being slowed down, however, were the errors that managed to creep in. When I was looking at several lines of selections, sums, and joins all at once, it was much harder to find and correct any logical errors I made. As the day drew to a close and I started running out of time, my checking grew shoddier. I was just glad that reasonable numbers seemed to be showing up.

I presented my code that evening, but it did not go well. The numbers that had seemed reasonable just a few minutes ago turned out to be thoroughly wrong. When I showed the code that had generated those numbers, there were obvious logical missteps buried in the queries. Worst of all, when I went back to look over the first code I’d written that day, I had forgotten how poorly it was done. I didn’t thoroughly understand how the joins worked, and instead of writing one big query, I wrote Ruby code to iterate through each user and then through each user’s orders, and ran a separate query for each one, which is incredibly inefficient. All in all, I received a thorough and well-deserved savaging for code that I had been proud of half an hour earlier.

Even though it was painful, I learned more in that 15 minutes than I had the rest of the day. It reminded me that, instead of always charging forward at full speed, it’s worthwhile to make sure that I have a clear roadmap of what’s ahead. It taught me that when I find myself saying “Well, we can always refactor later,” I’m going down a dangerous path. With the amount of content we’re learning each day, it’s incredibly tempting to cut corners, but in the end it creates more work than it saves. Thankfully I received those criticisms when my bad habits could be nipped in the bud, so that I can be a better programmer in the long run.
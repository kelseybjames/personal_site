---
layout: post
title:  "Viking Code School: How much can you learn in a month?"
date:   2016-02-01 12:45:00 -0800
categories: ruby programming learning
---

I’ve now completed 4 weeks at Viking Code School. In that time, we’ve covered basic Ruby, algorithms and data structures, web apps built with Sinatra and Rails, and SQL queries. We’ve worked together and separately on various assignments, and we even had a mini-hackathon where we had to think of and build projects using the Star Wars API over the course of a day.

Along with new technical knowledge comes refinement of my existing technique. I find myself looking at code I worked hard on and was proud of only a month ago, and I cringe at the now-obvious clumsiness and redundancy. I find myself thinking of edge cases that had never occurred to me, and how to properly account for them.

As a small example, here’s a snippet of code I wrote in preparation for the program:

{% highlight ruby %}
def is_palindrome(number)
  if number.to_s == number.to_s.reverse
    return true
  else
    return false
  end
end
{% endhighlight %}

It seemed good enough to me at the time, and it does work, but it could be written much more neatly. First, I now know that methods that return boolean values like that are customarily defined with a question mark at the end of their names. Secondly, since I’m testing a comparison that will return true or false anyway, I can just return it directly without a cumbersome if statement. Now, if I wanted to solve that problem the same way, I would write:

{% highlight ruby %}
def is_palindrome?(number)
  number.to_s == number.to_s.reverse
end
{% endhighlight %}

That’s just one small improvement. I’ve found myself looking over code that I wrote for previous projects and working out how best to refactor it. I’m still quite impressed at how much difference a month has made.

These days, even when I’m browsing the web for something completely unrelated, there’s a part of my brain that’s working out the best way to replicate the site I’m visiting. For instance, if I’m checking Facebook, I think of my network of friends and all the content that they generate, and imagine how I would store that data and make it accessible. I look at the source of a website I’m using and observe how they’ve structured it, and I try and notice common practices that would be useful to remember. This is just the beginning of a long journey, but I’m confident that I’m on the right path.
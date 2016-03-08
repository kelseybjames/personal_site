---
layout: post
title:  "Radix sort"
date:   2016-01-18 12:45:00 -0800
categories: ruby programming algorithm
---
I spent a fair amount of time this weekend reading about different sorting algorithms. They were very interesting reads, and helped me think more about exactly what sorting entails. Radix sort was one that I hadn’t heard of before, even in passing. It seemed like a quite reasonable method of sorting, so I read more deeply into it to try and find out why it had flown under my radar.

There are two overarching approaches to radix sort:

Least Significant Digit

In this implementation, you would start by sorting the numbers into 10 different buckets, based on the ones digit. You otherwise retain the original order of the numbers, which cuts down on unnecessary operations and makes the sort stable. Once this step is completed, you sort similarly based on the tens digit, and continue these operations until you have sorted by the most significant digit.

You can optimize this sort by separating the list of numbers ahead of time by their length and then performing the radix sort on each list separately. This removes the need to process the whole list even when only the longest numbers need to be sorted. With these optimizations, the radix sort will run in O(nk) time, where n is the number of elements and k is the average length. Since you don’t have to make comparisons between elements, a radix sort can be faster in certain specific applications.

Most Significant Digit

Naturally, you can also start at the other end with the most significant digit. The process is similar: you sort the objects into buckets based on the most significant or leftmost digit, and then recursively sort until you have the final list. This sort is used more often with strings; you can imagine it as looking in a dictionary for the desired word, starting with the first letter and narrowing down based on each subsequent letter until the word is found.

Pros and cons

Radix sorts can be quite fast, but they’re generally only useful in specific situations. They are more constrained than other types of sorts; they work best with objects all of the same size, and if you have objects longer than the array size, then you can actually have a runtime worse than O(n²). They also only really work well for specific types of objects, mainly numbers of different sorts and strings. They’re quite situational, but if you have a large list of numbers and you have a good idea of how they are bounded, then radix sort may be worth consideration.
---
layout: post
title:  "Finding the missing number in a sorted array"
date:   2016-01-25 12:45:00 -0800
categories: ruby programming algorithm
---
Suppose you have a sorted array of numbers from 0 to n, and you want to find which one of them is missing. How would you do it, and what is the most efficient way?

The naive solution would be to iterate over the elements of the array and, when the next element is 2 greater than the previous rather than 1, you return the missing element. You could also take a bit of a shortcut by taking the sum of all numbers from 1 to n and subtracting the sum of all the elements in the array, again returning the missing number. Both of these solutions take O(n) time, which seems pretty good at first.

However, neither of these solutions takes into account the fact that the list is sorted. Since we know we have a sorted list, until we reach the missing element, the index of any given element should be equal to the value. Using that, we can implement a binary search algorithm. If the middle element of the array has index equal to its value, search over the right array, otherwise search over the left array. If we implement this search, we see that we can find the missing element in only O(log n) time, which is quite an improvement. This is only one of many ways that working with pre-sorted lists is much faster.
---
layout: post
title:  "Algorithms can be fun"
date:   2017-09-08 00:00:00
categories: algorithms python
image: https://dl.dropboxusercontent.com/s/ng8rgpx20gx3rjj/algorithms-olayinkaos-blog.jpg
disqus: true
description: I started a new journey to learn, and really understand complex software algorithms. I share my learnings so far here.
---

One of the the concepts that have always amazed me in software is [Algorithms](https://en.wikipedia.org/wiki/Algorithm). As a self taught web developer, I never really had a real reason to learn them... I mean, as long as the code works, we're good right? Sometimes.

You see, when you work on the small stuff it's fine, but when you start building for very large data sets, every single optimisation counts. That millisecond lag in your code will cost you when you're working with 1,000,000,000s of records, or perhaps an infinite stream of data.

I recently took a strong interest in Algorithms, and as with almost everything else I know in life, I decided to take a head-first dive into learning it. I enrolled in [this course](https://www.coursera.org/specializations/algorithms), and have started the journey to getting better at understanding and analysing common algorithms.


## What do I think so far?

I've only done a few days, and I feel smarter already. Even though I'm really still learning the basics, I think taking a big interest in Algorithms will be absolutely worth it to every developer. At the very least you'll be able to confidently use lingo like [Big O notation](https://en.wikipedia.org/wiki/Big_O_notation), [Divide and Conquer design paradigm](https://en.wikipedia.org/wiki/Divide_and_conquer_algorithm), and so on. 😉

Also, having to implement algorithms in your language of choice can really help improve your analytical skills and make you a better programmer. One of the first things I did in the course was implement the popular [Merge sort](https://en.wikipedia.org/wiki/Merge_sort) algorithm. It's not the typical thing you'd bother about in your daily work as a developer, so I had to think a bit and convert the psuedo-code I was provided with into working software. Here's the implementation I did in Python:

```python
def mergeSort(input):
  """
  My implementation of the famous Merge Sort Algorithm in Python. This procedure takes the array/list of numbers to be sorted as input, then recursively splits, and merges them in sorted order, then returns the sorted list.
  """
  if len(input) > 1:
    # split the list into 2 halves
    half = len(input) / 2; 
    # recursively sort both halves
    left, right = mergeSort(input[:half]), mergeSort(input[half:])
    # merge both halves in sorted order, 
    # taking the smaller values first
    i, j = 0, 0
    output = []
    while i < len (left) and j < len (right):
      if left[i] <= right[j]:
        output.append(left[i]) 
        i += 1
      else:
        output.append(right[j])
        j += 1
    output += left[i:]
    output += right[j:]
  else:
    output = input
  return output

# sample test cases
print mergeSort([8, 22, 4, 32, 3, 1, 2, 44, 'ss', 'al']);
print mergeSort([2.3, 1, 2, 33])
```

And if you think the above was me just shamelessly pluging in my code to show off and ask for feedback, you're absulutely right. Do let me know any way you think the code can be improved. Thanks thanks.

So that's it. I'll try to write a bit more about what I learn as time goes on. As you can see, Algorithms can actually be quite exciting. Don't forget to leave any thoughts on code, algorithms, etcetera, in the comments.



---
title: "Coin Sum"
date: 2021-09-02T16:26:09-04:00
draft: false
---
Question 31 from Euler.com
# Question Statement
In the United Kingdom the currency is made up of pound (£) and pence (p). There are eight coins in general circulation:

1p, 2p, 5p, 10p, 20p, 50p, £1 (100p), and £2 (200p).
It is possible to make £2 in the following way:

1×£1 + 1×50p + 2×20p + 1×5p + 1×2p + 3×1p
How many different ways can £2 be made using any number of coins?
# How to approah this?
At the first glance, the problem may seem simple - sure, let's just count the number of combinations. We only have 8 different face value anyways.

But..is it so?

If we think about this problem using the brute-force way, we can do something like:

For each type of face value, we go over each while looping through all different values for the next type of face value, and loop through all different values for the next ype of face value... By doing so, we are going to have 8 layers of nested for-loops and within each loop we are also testing about differnet possible numbers that each face value can be used! 

It comes not surprising that this solutio will be brutally time-consuming and error-prone. Testing for different combinations of the values can involve millions of times of calculation even for this one which only required all numbers to add up to 200. What about 200,000, or 2 million?

# Divide and Conquer!

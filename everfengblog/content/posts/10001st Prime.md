---
title: "10001st Prime"
date: 2021-09-02T16:10:45-04:00
draft: false
---

Prime and its magic

## Question Statement
This question comes from Euler.com, withe question ID 7. 

The original question is straightforward - how do we find the 1001st prime number among all integers?

## How to approach this?
First, we need to understand what the criterion for a number to be regarded as a prime number : a prime number is an integer that cannot be divded without remainder by any number except for 1 and itself. For example,  3 can only be wholly divided by 1 and 3, and if divided by 2, it will have a remainder of 1.

Thus, in order to test whether or not a number is prime, we can try to divde it by each number from 1 to itself and keep a record of the remainder from each calculation. If it is a prime number, we will find out that there are only two occurances where 0 is the remainder. If there are more than 2 occurances of 0, we will know that this number can be divided by numbeers other than 0 and itself, thus not a prime number.


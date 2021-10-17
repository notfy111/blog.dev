---
title: "Get_17_th_prime"
date: 2021-10-17T15:48:13-04:00
draft: false
---
 What if, you just got an interview from one of your dream employers - Google, and you spent more than 10 hours a day to prepare for it. You have done everything correctly - review key data science concepts, machine learning pipeline, and get several hundred of LeetCode questions done. 
 On the day of interview, you are asked the following question: 
## Give me the first 10- digit prime of the expansion in 17 * pi
 You paniced, get totally thrown off - I have never prepared for this kind of questions before, what do I do?? 
## Divide and Conquer to the rescue!
 This is a question seems large becase it implicitly asks for a lot of sub-parts to be done before you can get an answer. The good news here is also that,
we can tackle the question solving the small questions first. 
### step 1: get pi
 First and foremost, let's think about how to get pi and a long expansion of its decimal parts to make sure we have enough digits to work with. 
 Theoretically, we will need to calculate pi and get the values by writing code for Taylor Expansion. Considerating the complexity in writing that,
and the potential rounding errors that can occur, it is a risky route to take. 
 Luckily, we have libaries like '''sympy''' that helps get whatever digit expansion we'd want to see. 
### step 2: use a window to filter all 10-digit numbers from the expanded long decimals
 For this task, we will need to imagine a moving filter that looks at 10 digits at a time, and after that moves one digit forward to look at the next.
In this case, it is much easier to treat the long decimals as a string, and each number as a character. 
 **Caution** one corner case to think about is when the number starts with 0. 
 In this case, we will need a condiitional statement which ignores 10-digit number that starts with 0. 
### step 3: check whether or not a number is prime
 Here comes our concept of prime number again. A prime number is a positive integer that can only be divided without remainder by 1 and itself.
Based on this concept, we can check if our 10-digit number is prime by dividing it with all possible numbers that are smaller than itself. If it can be fully divided by numbers other than 1 and itself, then it is not prime; otherwise it is. 
 However, dividing a number millions of times may not be as efficient. How can we minimize the number of times that this number is divded by? 
 In fact, an important yet not really intuitive fact to know is that: to find out a number's all posible composites, we only need to check from the smallest to the square root of this number. 
 ### Why is that so? 
 If we think of the number line of composites to large number as symmmetrical, it is clear that - as one of the composite gets larger, the other composite becomes smaller, as they have to multiply to get the same amount. As a s result, if one of the composite is 2, and to get a number of 1786543062, the other composite is large, which is 893271531. On the other hand, if the first composite is 893271531, then the other composite is small, which is 2. As a result, when we have check from one end of the number line to the point of the square root of this number, we have in fact also checked the other end of the number line - because those numbers need to multiply with these smaller numbers to get to the target number. 
 Consequently, once we have checked from 2 to the square root of the number and find no composite, it is safe to say that we are not going to find a corresponding composite in the larger end of pool either. 
 Once wraped our brain around that, the solution becomes much more straightforward. 
 ## Pesudo-code
 First, we need to get a large exapansion of 17 * pi to make sure our decimals are accurate. Then, we need a filter to run through all valid 10-digits from the large expansion. For each of the 10-digit candidate, check whether or not they are prime by dividing the number from 2 to the square root of itself. Once we find such number, stop the work and return the number.  

If you are able to demonstrate this divide-and-conquer mindset, have a great number sense, and to think about corner cases, you''ll impress the interviewer in no time!

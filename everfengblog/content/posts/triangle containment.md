---
title: "Triangle Containment"
date: 2021-09-02T16:38:27-04:00
draft: false
---
How do you tell whether or not, a triangle drawn in a Cartesian plane contains the origin (0,0)?
 It is not a brain teaser as far as we can actually draw the trangle using the coordinates for its three corners, and tell from our eye whether or not it is true. 
 But things get a little bit hard when we need to think about this algorithmically. 
## How to approach it?
 Once we connect the three corners to form a triangle, we have created a plane, in which an almost infinite number of points can be included. 
 If we cannot wrap our head around comparing points to points, it can be a very difficult problem to solve. Do we know the triangle contians the origin if two of the corners' x-coordinates have different signs? What about y-coordinates? Shoould one of the lines cross the axis to confirm that the origin is included in the plane? 
 In fact, answering these questions does not give us a definitive answer, and we'll find that a triangle that satisfy all these requisites can still be really far from the origin, and one that violates all these can still include the origin. 
## Think backwards
 If listing pre-requisites does not help address the problem, then what can? 
 Well, we can work backwards - namely, we can start from the case when the triangle contains the origin, and find out the term that must be true in that fase. 
 If we draw a random trangle that includes the origin, soon we can notice that - this trangle can be perfectly divided into smaller triangles. 
 Say, we have its three corners as A, B, and C. The origin can be the fourth corner (O) which, when combined with any two other corners, can form a smaller triangle. Adding upp the three small tirangles ABO, ACO, BCO can thus give us the same area as the larger triangle. 
 Let's test it on triangles which do not contain the origin.  Apparently, if we connect the corners with the origin, the smaller triangles are always tweaked or streched, and adding them back does not give us the same area as the original triangle. 
## The final solution
 Then everything is simple now! For each triangle, we can assume that it includes the origin, and calculate the sum of the areas of the three smaller triangles formed by any of the two corners and the origin. Comparing the result with the area of the original triangle, we know for sure that whether or not the origin is emcompassed in the triangular plane! 
[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

import scipy.stats

mean = 178 # average height of men in cm
STD = 7.7  # standard dev of height of men in cm
dist = scipy.stats.norm(loc=mean, scale=STD)

Creates a distribution of heights using the mean and std in centimeters.

low = dist.cdf(177.8)    # 177.8 is 5'10 in cm

This pulls the cdf at the lower end of Blue Man group height requirement.

high = dist.cdf(185.4)   # 185.4 is 6'1 in cm

This pulls the cdf at the higher end of Blue Man group height requirement.

low
0.48963902786483265   

high
0.8317337108107857  

high-low
0.3420946829459531  

Subtracting the high cdf from the low cdf we will get the percentage of the male pop that is eligible for the blue man group.

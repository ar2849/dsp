[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

from __future__ import print_function, division

%matplotlib inline

import numpy as np

import nsfg
import first
import thinkstats2
import thinkplot

thousand_random = np.random.random(1000)  
Generates a thousand binary values

pmf = thinkstats2.Pmf(thousand_random)
thinkplot.Pmf(pmf, linewidth=0.1)
thinkplot.Config(xlabel='Random variate', ylabel='PMF')

Creates a probability mass function from the thousand_random variable. Then plots the pmf, revealing a completely useless graph of vertical lines parallel to the y-axis.

cdf = thinkstats2.Cdf(thousand_random)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Random variate', ylabel='CDF')  

CDF is the cumulative distribution function. This will add all the of probabilities prior to that discrete value. Plotting the cdf shows a linear relationship and that the probability of getting a 1 or 0 is equal. 

[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 

Codeblock

```python

# Exercise: In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm 
# and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.

# In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). 
# What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

# scipy.stats contains objects that represent analytic distributions


from __future__ import print_function, division

%matplotlib inline

import numpy as np

import nsfg
import first
import analytic

import thinkstats2
import thinkplot
import scipy.stats


mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)  # takes optional parameters: loc, which specifies the mean, and
# scale, which specifies the standard deviation.
type(dist)


h1 = 177.8  # 5' 10" in cm
h2 = 185.4  # 6' 1" in cm

low = dist.cdf(h1)  # return percentile of male at h1 
high = dist.cdf(h2)  # return percentile of male at h2  

print(low)
print(high)
print((high - low)*100)  # percentage of U.S. male population between h1 and h2


```

34.2% of the US male population qualifies (height-wise) to join the Blue Man Group. 
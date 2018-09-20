[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 

Codeblock

```python
from __future__ import print_function, division

%matplotlib inline

import numpy as np

import nsfg
import thinkstats2
import thinkplot

def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf

resp = nsfg.ReadFemResp()

pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
biased_pmf = BiasPmf(pmf, label='biased')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Number of children', ylabel='PMF')

print('Actual mean', pmf.Mean())
print('Biased mean', biased_pmf.Mean())

```

Referencing the code from ThinkStats2, the necessary modules were imported. The BiasPmf function was copied. The pmf function is from the thinkstats2 module. The pmf function returns the actual pmf and BiasPmf returns the bias PMF. using thinkplot, both pmf were printed in the same graph.

The results of the PMF and biased PMF were as expected, similar to the class size paradox. When childrenwere surveyed and asked how many children are in their household they reported higher numbers. In fact the mean of the biased PMF was 2.4 children per household where as the actual PMF was only 1.02. It is interesting to note that for households with only 1 child, there were no difference in the PMF. This significant difference may be due to the lack of understanding of what the surveryers were actually asking since children may think other childresn who they play with are part of their household. Perhaps children who have siblings believes that many other familys are similar to theirs - having more than one children. This might explain why there was no difference for households that only had 1 child.   

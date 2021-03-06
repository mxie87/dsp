[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 

Codeblock
---

```python
import numpy as np
import nsfg
import first

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d

firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()

CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
```

Based on the NSFG data, it appears first babies are slightly lighter than other babies by .125 lbs, a 1.7 percent difference. Cohen's D was computated to be .089 standard deviations. While this effect size is about 3 times larger than the difference in pregnancy length, it is still a very small negligible difference.
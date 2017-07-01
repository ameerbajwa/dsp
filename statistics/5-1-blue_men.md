[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

    import numpy as np
    import pandas as pd
    import math
    import sys
    import nsfg
    import first
    import thinkstats2
    import thinkplot
    import scipy.stats

    mu = 178
    sigma = 7.7
    dist = scipy.stats.norm(loc=mu, scale=sigma)

    low = dist.cdf(177.8)
    high = dist.cdf(185.4)

    print (low)
    print (high)
    print (high-low)

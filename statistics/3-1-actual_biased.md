[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

  import numpy as np
  import pandas as pd
  import math
  import sys
  import nsfg
  import first
  import thinkstats2
  import thinkplot

  resp = nsfg.ReadFemResp()

  pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

  def BiasPmf(pmf, label):
	  new_pmf = pmf.Copy(label=label)
	
	  for x, p in pmf.Items():
		  new_pmf.Mult(x, x)
	
	  new_pmf.Normalize()
	  return new_pmf

  biased = BiasPmf(pmf, label='biased')
  thinkplot.PrePlot(2)
  thinkplot.Pmfs([pmf, biased])
  thinkplot.Config(xlabel='Number of children', ylabel='PMF')

  thinkplot.show()

  print (pmf.Mean())
  print (biased.Mean())

[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

import numpy as np
import pandas as pd
import math
import sys
import nsfg
import first
import thinkstats2
import thinkplot

df = nsfg.ReadFemPreg()
live = df[df.outcome == 1]
	
first = live[live.birthord == 1]
others = live[live.birthord != 1]

def info_totalwgt():
	
  print ("Difference between first born and other born babies in weight\n")
	
	first_mean_lb = first.totalwgt_lb.mean()
	first_var_lb = first.totalwgt_lb.var()
	first_std_lb = first.totalwgt_lb.std()
	
	other_mean_lb = others.totalwgt_lb.mean()
	other_var_lb = others.totalwgt_lb.var()
	other_std_lb = others.totalwgt_lb.std()
	
	print ("First born babies")
	print ("Mean: " + str(first_mean_lb) + " Std: " + str(first_std_lb))
	
	print ("\nOther born babies")
	print ("Mean: " + str(other_mean_lb) + " Std: " + str(other_std_lb))

	diff = first_mean_lb - other_mean_lb
	n1 = len(first.totalwgt_lb)
	n2 = len(others.totalwgt_lb)
	pooled_var = (n1 * first_var_lb + n2 * other_var_lb) / (n1+n2)
	
	d = diff/math.sqrt(pooled_var)
	print("\nCohen d value: " + str(d) + "\n")
	
def info_prglngth():
	
	print ("Difference between first born and other born babies in pregnancy length\n")
	
	first_mean_pl = first.prglngth.mean()
	first_var_pl = first.prglngth.var()
	first_std_pl = first.prglngth.std()
	
	other_mean_pl = others.prglngth.mean()
	other_var_pl = others.prglngth.var()
	other_std_pl = others.prglngth.std()
	
	print ("First born babies")
	print ("Mean: " + str(first_mean_pl) + " Std: " + str(first_std_pl))
	
	print ("\nOther born babies")
	print ("Mean: " + str(other_mean_pl) + " Std: " + str(other_std_pl))
	
	diff = first_mean_pl - other_mean_pl
	n1 = len(first.prglngth)
	n2 = len(others.prglngth)
	pooled_var = (n1 * first_var_pl + n2 * other_var_pl) / (n1+n2)
	
	d = diff/math.sqrt(pooled_var)
	print("\nCohen d value: " + str(d) + "\n")

info_totalwgt()
info_prglngth()

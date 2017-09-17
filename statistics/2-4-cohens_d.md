[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Cohen's D = -0.08867236333202932

Please code below for this solution:
```
import first
import thinkstats2
import nsfg
import math
live, firsts, others = first.MakeFrames()

resp = nsfg.ReadFemResp()


preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts_weight = live[live.birthord == 1]
others_weight = live[live.birthord != 1]

first_weight_mean = firsts_weight.totalwgt_lb.mean()
first_weight_var = firsts_weight.totalwgt_lb.var()
first_weight_n = firsts_weight.totalwgt_lb.count()

others_weight_mean = others_weight.totalwgt_lb.mean()
others_weight_var = others_weight.totalwgt_lb.var()
others_weight_n = others_weight.totalwgt_lb.count()

pooled_var = (first_weight_n*first_weight_var+others_weight_n*others_weight_var)/(others_weight_n+first_weight_n)
d= (first_weight_mean-others_weight_mean) / math.sqrt(pooled_var) 
```

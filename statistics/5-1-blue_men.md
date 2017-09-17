[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

34.3 percent of men are between 5'10" and 6'1"
```
cm_per_in = 2.54
in_min = 70 * cm_per_in
in_max = 73 * cm_per_in
prct_less_min = dist.cdf(in_min)
prct_less_max = dist.cdf(in_max)
prct_blue_man = prct_less_max-prct_less_min
print(prct_blue_man)

```

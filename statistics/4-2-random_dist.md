[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```
random_range = np.random.random(1000)
pmf = thinkstats2.Pmf(random_range,label='random_numbers')
thinkplot.PrePlot(1)
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel = 'random float', ylabel = 'PMF')
#The PMF plot is wrong because our data does not have a discrete value
#on the x axis. PMF does not know how many bins to divide the data into.
```

[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)
Unbiased mean = 1.0 children/family
Biased mean = 2.4 children/family

```
resp = nsfg.ReadFemResp()
hist_num_child_family = thinkstats2.Hist(resp.numkdhh, label='num_child_unbiased')
mean_num_child_family = resp.numkdhh.mean()

thinkplot.Hist(hist_num_child_family)
thinkplot.Config(xlabel='Num of Children Unbiased', ylabel='Count')

pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')
old_freq={}
new_freq={}

n_children = resp.numkdhh.count()
for x, freq_children in pmf.Items():
    old_freq[x]=freq_children*n_children
    new_freq[x]=freq_children*n_children*x

    
pmf_unbiased = thinkstats2.Pmf(old_freq, label='unbiased')
pmf_biased = thinkstats2.Pmf(new_freq, label='biased')

new_freq_hist = thinkstats2.Hist(new_freq, label='num_child_biased')
thinkplot.Hist(new_freq_hist)
thinkplot.Config(xlabel='Num of Children', ylabel = 'Count')

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf_unbiased, pmf_biased])
thinkplot.Config(xlabel='Num of Children', ylabel='PMF')

total=0
total_families=0
for key, value in new_freq.items():
    total+=key*value
    total_families+=value
    mean_new=total/total_families
total=0
total_families=0
for key, value in old_freq.items():
    total+=key*value
    total_families+=value
    mean_old=total/total_families
print(mean_new)
print(mean_old)
```

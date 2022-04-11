# Research-Notes

**Q. Why are there more statistics in forward rapidity if we make pT cuts higher for the photons in calibration code?**

>Because with higher pT cuts you are asking photons to be more energetic and higher transverse momentum which means these types of photons are mainly found in the very forward (also backward) rapidity instead of the mid-rapidity. Mid-rapidity photons are mainly not so much energetic and momenta. So, if you lower the pT cuts, then you are now trying to accumulate as much of photons possibly even from the mid-rapidity regions.

**Q. Why while doing the plot of `eta_hist[i]` we should restrict the plotting range very much?**

>Because in those plots we really want to only plot the peak area and little bit of background around it. But if we increase the plot ranges to too much then the fit will try to match the background data to that above ranges values also which we don't want to incorporate. This will cause the fit parameters to go in a certain direction to that area which we don't care. Also, in that unwanted range there might be the most statistics and so your fit will try to fit that very high statistics region preferentially (not the pi0 peak). Hence, it is always a good idea to limit the ranges of the fit from let's say (0.07-0.30 in our case).

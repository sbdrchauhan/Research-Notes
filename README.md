# Research-Notes

**Q. Why are there more statistics in forward rapidity if we make pT cuts higher for the photons in calibration code?**

>Because with higher pT cuts you are asking photons to be more energetic and higher transverse momentum which means these types of photons are mainly found in the very forward (also backward) rapidity instead of the mid-rapidity. Mid-rapidity photons are mainly not so much energetic and momenta. So, if you lower the pT cuts, then you are now trying to accumulate as much of photons possibly even from the mid-rapidity regions.

**Q. Why while doing the plot of `eta_hist[i]` we should restrict the plotting range very much?**

>Because in those plots we really want to only plot the peak area and little bit of background around it. But if we increase the plot ranges to too much then the fit will try to match the background data to that above ranges values also which we don't want to incorporate. This will cause the fit parameters to go in a certain direction to that area which we don't care. Also, in that unwanted range there might be the most statistics and so your fit will try to fit that very high statistics region preferentially (not the pi0 peak). Hence, it is always a good idea to limit the ranges of the fit from let's say (0.07-0.30 in our case). See the image below:

![Pi0 Image](https://github.com/sbdrchauhan/Research-Notes/blob/main/images/pi0%20fit%20range.png)


**Q. How to transfer files to and from rcas machine to your local computer?**

>SDCC uses **sftP** to do this job. Please go to this webpage [SDCC page](https://www.sdcc.bnl.gov/information/transfer-files-using-sftp-gateways).
Then do the following steps. You do not have to **ssh** anything to go behind the firewall for this, you can directly do **sftp** from your terminal and then start doing things as described below. **get** downloads files from rcas to your local computer; **put** uploads file from your locat machine to the rcas machine.
```
sftp schauhan1@sftp.sdcc.bnl.gov
sftp> get filename.root   // this file downloads from where you did above command in your local machine
sftp> put file2.jpg     // uploads file2.jgp to your home rcas machine
```

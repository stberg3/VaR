# CVaR

There is an R package available that does the calculations for us. [This video]
(https://www.youtube.com/watch?v=0N7XBk7YA5A) explains its usage.

To perform the calculations manually, here's [a video](https://www.youtube.com/watch?v=2QJykxUNb6I)
on calculating VaR and CVaR in Excel.

If you watch this pay close attention to the final calculations, since the video
author chooses specific return values instead of interpolating from a model. You
could modify the calculation in R by feeding the data into a distribution and
picking a derived data point (ie. a return value that isn't actually in the data
set) from the distribution.
	-	Long story short, VaR(data, alpha=95) is the return value of the data that's
		where 5% of the returns are lower, and 95% are greater
	-	CVaR(data, alpha=95) is the mean of the bottom 5% of returns.
	- Don't worry about the calculus we've seen in the formulas we've seen. They
		offer a GENERAL solution to the CVaR. But since we have data, we can
		solve it though simple manipulation of the data.

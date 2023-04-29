# lognormal-fitting

what is a lognormal distribution?
1. Suppose a normally distributed random variable X has mean mu and standard deviation sigma. Then Y = exp(X) is lognormally distributed with s = sigma and scale = exp(mu).
2. Suppose a lognormally distributed random variable X has scale = exp(mu) and standard deviation sigma. Then Y=log(X) is normally distributed with s = sigma and mean = mu.

from scipy.stats import lognorm

samples = lognorm.rvs(s=0.7, loc=2, scale=1, size=10000)

plt.hist((samples), bins=200,alpha=0.2,density=True)
plt.show()
plt.hist(np.log(samples), bins=200,alpha=0.2,density=True)
plt.show()

plt.hist((samples-2), bins=200,alpha=0.2,density=True)
plt.show()
plt.hist(np.log(samples-2), bins=200,alpha=0.2,density=True)
plt.show()
print(min(samples))

chain = sample(model, HMC(0.05, 10), 1000)

This is the second chain to finish execution for this model. However, rhat values are either missing or less than 1 and ess is too low. An analysis of the chains shows that the sampler is not exploring the distribution fully and the density function of some of the parameters looks bimodal which may indicate a bottleneck in the geometry of the posterior (if my understanding is correct).

This outcome is very similar to 24-06-22_09-53 chain. This indicates that there is likely an issue with my model.
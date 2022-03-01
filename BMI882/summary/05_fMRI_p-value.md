# 05_fMRI_p-value


## Summary

fMRI has been developed a long time ago but its most common statistical methods have not been validated using real data. This paper conduct 3 million task group analyses on resting-state fMRI data from 499 healthy controls. They found the most common software packages for fMRI analysis result in false-positive rates of up to 70%. These findings speak to the need of validating the statistical methods being used in the field of neuroimaging. They found due to the underlying assumption of these models such as theoretical null distribution, the spatial autocorrelation function of noise.

## Reaction

I think this paper pinpoints to a problem for many statistical methods: the assumption of the model does not fit the real data. The problem may come from the requirement to publish papers in statistical journal: only requires proof, simulation based on the oracle model, and very little and even no real data analysis. Since  the data in the simulation is generated based on their true model, it cannot represent how the real data looks like. Thus, it will leads to inflated type-I error

## Questions for discussion

1. How to make sure the assumptions in our models are valid? It is not easy to find a negative control data.
2. Are there examples of such problem in other field?


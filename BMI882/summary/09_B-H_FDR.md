# 09_B-H_FDR

Before this paper, people use FWER to address the multiple testing problem. However, FWER is defined as the probability of not getting any type-I error and may be too conservative. B-H propose to use the FDR, the expetation of the type-I error over all discoveries, as another useful metric to address multiple testing problem. They propose a sequential P-value method to contol the FDR and demonstrate it is universial powerful than methods to control FWER like Bonferroni correction.

This is a pioneering paper and got cited more than 80k shown in google scholar now.  A very intersting thing to me is that the FDR (pFDR) has a Bayesian interpretation provided by John Storey.  It has a very similar story as the James-Stein estimator: People first use a freqentist perpective to define a new thing but it lacks interpretaions. Then other people find a Bayesian interpretaions of the new thing. Another observation is that many people won COPSS has a big contribution in FDR field (Dr. Efron, Dr. Storey, and Dr. Barber).

## Questions for discussion

1. Why people in some field like GWAS still use FWER rather than FDR?
# 12_Batch_Effects

This paper talks about batch effects, which occurs when the measurements are affected by the laboratory  condition, reagent lots and personnel differences. It first talk about how to identify batch effects and provide some example of batch effects in some existing dataset. Then it gives some instructions on how to avoid batch effects by better experimental design solutions and statistical solutions.

This is an important paper that talks about the bias comes from generating the data. However,  I don't see it much in GWAS field. I think it is more important in gene expression analysis than GWAS sicne the batch effects should not corrected with the phenotype (?). But one "batch" effects in GWAS analysis is population stratification, which people commonly use PCs or mixed model to control.

## Questions for discussion

1. Why don't we directly add PCs as covariates to address the batch effects? Is it because it will reduce the power of the test?
2. Are there batch effects in testing covid19 positive reported?
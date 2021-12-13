# 14_tSNE

Reference: https://www.jmlr.org/papers/v9/vandermaaten08a.html

## Summary
This paper propose a new method to visualize high-dimensional data by giving each datapoint a location in a two or three-dimensional map. It extends the Stochastic Neighbor Embedding (SNE) to t-SNE. The name "t" is because it uses the t-distibution to replace the Gaussian to calculate similarity in low-dimensional space. Since t-distribution has t-Distribution is a long tail distribution, it prevents the crowding problem. The author used several data sets and showed the results t-SNE are significantly better than other approaches.

## Reaction
I have seen a lot of papers using this methods and other methods called UMAP. But I never applied it in my field. In genetics, the most frequent dimension reduction methods we use is PCA. The PC from PCA represents the ancestry and there is a famous paper that maps the genetics PC to the European map. So I am quite curios why in my field, seems no one is using t-SNE and UMAP. And in some other field like single-cell RNA-seq, people never use PCA. And recently, I saw a paper called "The Specious Art of Single-Cell Genomics" by Prof. Lior Pachter in twitter. It critize such method but I didn't read it through. Seems there are some art in it. :D

## Questions for discussion
1. What the advantages and disadvantages between t-SNE, UMAP and PCA?
2. Is there other future development for t-SNE?

## Take away from discussion

We use different libraries of ROUGE, most of them implemented in python, to show the result scores of different experiments. Despite the fact that in the description library said that are a similar implementation of the original ROUGE measure, the scores are different for each library.

We begin with very simple toy examples and proposed to form sentences with repeated words in order to observe changes between document and its ROUGE measure. For the simple toy examples we used sentences extracted from DUC 2002 corpus. The results of these examples are in the "Toy examples" folder.

Additionally, we calculated for each experiment ROUGE measure by hand and our conclusion is that the library that obtains the same result is pyrouge. These are preliminary conclusions, so we presented experiment results using DUC corpora.

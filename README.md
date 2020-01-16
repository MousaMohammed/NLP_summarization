# DUC_experiments_using_different_ROUGE_libraries

The output summaries for 2004 (100 words length, multi-document, abstractive approach) supervised approach are shown in the next section, evaluated with the same ROUGE libraries mentioned above (for more details about experiments, see my other project called supervised_summarization).

"DUC2001_supervised_pyrouge", "DUC2002_supervised", "DUC2004_supervised_pyrouge", "DUC2001_supervised_easy_rouge" folders have the trained model for each experiment using the supervised approach.

"duc2001_testing_r1_a_supervised_easyrouge.csv", "duc2001_testing_r1_b_supervised_easyrouge.csv", "duc2001_testing_r2_a_supervised_easyrouge.csv", "duc2001_testing_r2_b_supervised_easyrouge.csv" files contain ROUGE metric of java library for DUC 2001 labeled with easy-rouge library.

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

The "model..." folders are the gold standards for each experiment.

----------------------------------------------------------------------------------------------------------------------------------------



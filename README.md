# DUC_experiments_using_different_ROUGE_libraries

The output summaries for DUC 2001 (100 words lenght, multi-document task, abstractive gold standard), 2002 (200 words length, multi-document, extractive gold standard) and 2004 (100 words length, multi-document, abstractive approach) supervised approach are shown in the next section, evaluated with the same ROUGE libraries mentioned above (for more details about experiments, see my other project called supervised_summarization).

The output summaries for DUC 2001 corpus labeled using easy-rouge are located in "testing_classifier_test_30collectionALL_4_0.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_cl4_for_ROUGE_pltrdy_A_DUC2001.rar" and "summaries_cl4_for_ROUGE_pltrdy_B_DUC2001.rar" folders contain the output summaries for rouge library.

In the following table the results are shown.

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.2472 | 0.2932 | 0.1593 | 0.1980 |
| ROUGE-1 precision | 0.2235 | 0.2622 | 0.0870 | 0.1806 |
| ROUGE-1 F score | 0.2314 | 0.2622 | 0.0866 | 0.1867 |
| ROUGE-2 recall | 0.0268 | 0.0380 | 0.0112 | 0.0104 |
| ROUGE-2 precision | 0.0219 | 0.0339 | 0.0040 | 0.0091 |
| ROUGE-2 F score | 0.0236 | 0.0339 | 0.0055 | 0.0096 |

The output summaries for DUC 2001 corpus labeled using pyrouge are located in "testing_classifier_pyrouge_4_0.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_cl4_for_ROUGE_pltrdy_DUC2001_pyrouge.rar" folder contains the output summaries for rouge library.

In the following table the results are shown.

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.1961 | 0.2117 | 0.1467 | 0.2829 |
| ROUGE-1 precision | 0.2347 | 0.2548 | 0.0671 | 0.1491 |
| ROUGE-1 F score | 0.2023 | 0.2548 | 0.0859 | 0.1947 |
| ROUGE-2 recall | 0.0203 | 0.0210 | 0.0045 | 0.0216 |
| ROUGE-2 precision | 0.0231 | 0.0245 | 0.0014 | 0.0112 |
| ROUGE-2 F score | 0.0204 | 0.0245 | 0.0020 | 0.0147 |

The output summaries for DUC 2002 corpus are located in "testing1_no_batches_classifierALL_3.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_for_ROUGE_pltrdy_A_DUC2002_supervised_3.rar" and "summaries_for_ROUGE_pltrdy_B_DUC2002_supervised_3.rar" folders contain the output summaries for rouge library.

In the following table the results are shown.

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.4342 | 0.4024 | 0.0793 | 0.2406 |
| ROUGE-1 precision | 0.3952 | 0.3902 | 0.0948 | 0.2834 |
| ROUGE-1 F score | 0.4096 | 0.3902 | 0.0805 | 0.2579 |
| ROUGE-2 recall | 0.1530 | 0.1374 | 0.0071 | 0.0278 |
| ROUGE-2 precision | 0.1416 | 0.1369 | 0.0062 | 0.0317 |
| ROUGE-2 F score | 0.1458 | 0.1369 | 0.0062 | 0.0294 |

The output summaries for DUC 2004 corpus are located in "testing_classifier_4_0_DUC2004_balanced.rar" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_cl4_for_ROUGE_pltrdy_DUC2001_pyrouge.zip" folder contains the output summaries for rouge library.

In the following table the results are shown.

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.2378 | 0.2417 | 0.1611 | 0.1750 |
| ROUGE-1 precision | 0.3008 | 0.3126 | 0.1164 | 0.2211 |
| ROUGE-1 F score | 0.2631 | 0.3126 | 0.1008 | 0.1939 |
| ROUGE-2 recall | 0.0427 | 0.0381 | 0.0168 | 0.0136 |
| ROUGE-2 precision | 0.0517 | 0.0471 | 0.0095 | 0.0169 |
| ROUGE-2 F score | 0.0461 | 0.0471 | 0.0117 | 0.0150 |

Finally, the output summaries for DUC 2002 using an unsupervised approach are located in "experiments_DUC2002_unsup.zip" folder, these output summaries were used for java library and (the finally results are in the "java_library_DUC2002_unsupervised.xlsx" and each output file (.csv) are located in "evaluation30_duc2002_unsupervised_java_library.rar"), pyrouge (the finally results are in the "pyrouge_library_duc2002_unsupervised.xlsx" and each output file (.npy) are located in "experiments_DUC2002_unsup_pyrouge.zip") and easy-rouge libraries, "summaries_for_ROUGE_pltrdy_A_DUC2002.rar" and "summaries_for_ROUGE_pltrdy_B_DUC2002.rar" folders contain the output summaries for rouge library. In this particular case, the unsupervised approach has a code segment which depends of randomness, so I ran the experiment 30 times and the output was the average result of the 30 experiments.

In the following table the results are shown.

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.5279 | 0.4645 | 0.0859 | 0.3064 |
| ROUGE-1 precision | 0.2981 | 0.2856 | 0.1091 | 0.1850 |
| ROUGE-1 F score | 0.3754 | 0.2856 | 0.0874 | 0.2263 |
| ROUGE-2 recall | 0.2146 | 0.1592 | 0.0498 | 0.0289 |
| ROUGE-2 precision | 0.1219 | 0.0954 | 0.0614 | 0.0171 |
| ROUGE-2 F score | 0.1523 | 0.0954 | 0.0500 | 0.0211 |

"DUC2001_supervised_pyrouge", "DUC2002_supervised", "DUC2004_supervised_pyrouge", "DUC2001_supervised_easy_rouge" folders have the trained model for each experiment using the supervised approach.

"DUC2002_unsupervised_A.rar" and "DUC2002_unsupervised_B.rar" folders have the gold standards of DUC 2002 unsupervised experiments.

"duc2001_r1_a_supervised_pyrouge.csv", "duc2001_r1_b_supervised_pyrouge.csv", "duc2001_r2_a_supervised_pyrouge.csv", "duc2001_r2_b_supervised_pyrouge.csv" files contain the ROUGE metric of java library for DUC 2001 labeled with pyrouge library.

"duc2001_testing_r1_a_supervised_easyrouge.csv", "duc2001_testing_r1_b_supervised_easyrouge.csv", "duc2001_testing_r2_a_supervised_easyrouge.csv", "duc2001_testing_r2_b_supervised_easyrouge.csv" files contain ROUGE metric of java library for DUC 2001 labeled with easy-rouge library.

"duc2002_r1_a_supervised.csv", "duc2002_r1_b_supervised.csv", "duc2002_r2_a_supervised.csv", "duc2002_r2_b_supervised.csv" files contain ROUGE metric of java library for DUC 2002 using supervised approach.

"duc2004_r1_a_supervised.csv", "duc2004_r1_b_supervised.csv", "duc2004_r1_c_supervised.csv", "duc2004_r1_d_supervised.csv", "duc2004_r2_a_supervised.csv", "duc2004_r2_b_supervised.csv", "duc2004_r2_c_supervised.csv", "duc2004_r2_d_supervised.csv" files contain ROUGE metric of java library for DUC 2004 using supervised approach.

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

The "model..." folders are the gold standards for each experiment.

----------------------------------------------------------------------------------------------------------------------------------------



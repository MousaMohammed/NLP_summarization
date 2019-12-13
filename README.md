# NLP_summarization_toy_examples

The results of very simple summaries evaluated with different python libraries based on ROUGE metric

The libraries are:

a. java ROUGE 2.0 https://rxnlp.com/rouge-2-0/#.XdXcKuhKiUk (no stemming, no stop words removal and no synonyms dictionaries)

b. easy-rouge python https://pypi.org/project/easy-rouge/

c. rouge python https://github.com/pltrdy/rouge (the output and reference summary files must contain the same number of lines)

d. wrapper of ROUGE 1.5.5.pl on python (default configuration: -c 95 -2 -1 -U -r 1000 -n 4 -w 1.2 -a -m) intalled following tutorial from https://medium.com/@prabha88978/installation-working-process-of-rouge-1-5-5-6c0dfdca49e8 and https://ireneli.eu/2018/01/11/working-with-rouge-1-5-5-evaluation-metric-in-python/#more-1840, the original ROUGE 1.5.5.pl can be obtained in https://github.com/bheinzerling/pyrouge located in pyrouge folder

The folder "toy_example1" contains three variant of summaries:

a. plain text

b. contains some punctuation marks

c. the text is in one sentence format

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

Original ROUGE 1.5.5.pl wrapper does not run in colab (something related to Permission denied: '/content/gdrive/My Drive/Codigos_doctorado_DUC2001/pyrouge-master_with_ROUGE155/tools/ROUGE-1.5.5/ROUGE-1.5.5.pl'). But, I installed locally in jupyter notebook. The ROUGE metric for each output summary is contained in numpy files (.npy) named ROUGE_2002_toy_example_simple (plain text), ROUGE_2002_toy_example_simple_punctuation (contains punctuation marks) and ROUGE_2002_toy_example_simple_one_line (the text is in one sentence format) for pyrouge library.

The output files from java ROUGE 2.0 are comma separated files (.csv).

--------------------------------------------------------------------------------------------------------------------------------------

The folder "toy example2" contains two documents to summarize and one gold standard. The first document has three sentences, the second has four sentences and the gold standard has four sentences. For this example I create four output summaries (located in "toy_example2_d1", "toy_example2_d2", "toy_example2_d3". "toy_example2_d4" folders), which contains the following:

a. The last two sentences from document one and document two

b. The sentences of both documents

c. The sentences from document one

d. The sentences from document two

The "toy_example2_model_summaries" folder contains the gold standard.

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

The ROUGE metric for each output summary is contained in numpy files (.npy) named ROUGE_2002_toy_example2_d1, ROUGE_2002_toy_example2_d2, ROUGE_2002_toy_example2_d3 and ROUGE_2002_toy_example2_d4 for pyrouge library.

The output files from java ROUGE 2.0 are comma separated files (.csv).

----------------------------------------------------------------------------------------------------------------------------------------
# DUC_experiments_using_different_ROUGE_libraries

The output summaries for DUC 2001 (100 words lenght, multi-document task, abstractive gold standard), 2002 (200 words length, multi-document, extractive gold standard) and 2004 (100 words length, multi-document, abstractive approach) supervised approach are shown in the next section, evaluated with the same ROUGE libraries mentioned above (for more details about experiments, see my other project called supervised_summarization).

The output summaries for DUC 2001 corpus labeled using easy-rouge are located in "testing_classifier_test_30collectionALL_4_0.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_cl4_for_ROUGE_pltrdy_A_DUC2001.rar" and "summaries_cl4_for_ROUGE_pltrdy_B_DUC2001.rar" folders contain the output summaries for rouge library.

The output summaries for DUC 2001 corpus labeled using pyrouge are located in "testing_classifier_pyrouge_4_0.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_cl4_for_ROUGE_pltrdy_DUC2001_pyrouge.rar" folder contains the output summaries for rouge library.

The output summaries for DUC 2002 corpus are located in "testing1_no_batches_classifierALL_3.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_for_ROUGE_pltrdy_A_DUC2002_supervised_3.rar" and "summaries_for_ROUGE_pltrdy_B_DUC2002_supervised_3.rar" folders contain the output summaries for rouge library.

The output summaries for DUC 2004 corpus are located in "testing_classifier_4_0_DUC2004_balanced.rar" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_cl4_for_ROUGE_pltrdy_DUC2001_pyrouge.zip" folder contains the output summaries for rouge library.

Finally, the output summaries for DUC 2002 using an unsupervised approach are located in "experiments_DUC2002_unsup.zip" folder, these output summaries were used for java library, pyrouge and easy-rouge libraries, "summaries_for_ROUGE_pltrdy_A_DUC2002.rar" and "summaries_for_ROUGE_pltrdy_B_DUC2002.rar" folders contain the output summaries for rouge library. In this particular case, the unsupervised approach has a code segment which depends of randomness, so I ran the experiment 30 times and the output was the average result of the 30 experiments.

"duc2001_r1_a_supervised_pyrouge.csv", "duc2001_r1_b_supervised_pyrouge.csv", "duc2001_r2_a_supervised_pyrouge.csv", "duc2001_r2_b_supervised_pyrouge.csv" files contain the ROUGE metric of java library for DUC 2001 labeled with pyrouge library.

"duc2001_testing_r1_a_supervised_easyrouge.csv", "duc2001_testing_r1_b_supervised_easyrouge.csv", "duc2001_testing_r2_a_supervised_easyrouge.csv", "duc2001_testing_r2_b_supervised_easyrouge.csv" files contain ROUGE metric of java library for DUC 2001 labeled with easy-rouge library.

"duc2002_r1_a_supervised.csv", "duc2002_r1_b_supervised.csv", "duc2002_r2_a_supervised.csv", "duc2002_r2_b_supervised.csv" files contain ROUGE metric of java library for DUC 2002 using supervised approach.

"duc2004_r1_a_supervised.csv", "duc2004_r1_b_supervised.csv", "duc2004_r1_c_supervised.csv", "duc2004_r1_d_supervised.csv", "duc2004_r2_a_supervised.csv", "duc2004_r2_b_supervised.csv", "duc2004_r2_c_supervised.csv", "duc2004_r2_d_supervised.csv" files contain ROUGE metric of java library for DUC 2004 using supervised approach.

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

----------------------------------------------------------------------------------------------------------------------------------------

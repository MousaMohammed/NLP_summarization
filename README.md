# NLP_summarization_toy_examples

The results of very simple summaries evaluated with different python libraries based on ROUGE metric

The libraries are:

a. java ROUGE 2.0 https://rxnlp.com/rouge-2-0/#.XdXcKuhKiUk (no stemming, no stop words removal and no synonyms dictionaries)

b. easy-rouge python https://pypi.org/project/easy-rouge/

c. rouge python https://github.com/pltrdy/rouge (the output and reference summary files must contain the same number of lines)

d. wrapper of ROUGE 1.5.5.pl on python (default configuration: -c 95 -2 -1 -U -r 1000 -n 4 -w 1.2 -a -m) installed following tutorial from https://medium.com/@prabha88978/installation-working-process-of-rouge-1-5-5-6c0dfdca49e8 and https://ireneli.eu/2018/01/11/working-with-rouge-1-5-5-evaluation-metric-in-python/#more-1840, the original ROUGE 1.5.5.pl can be obtained in https://github.com/bheinzerling/pyrouge located in pyrouge folder

The folder "toy_example1" contains three variant of summaries:

a. plain text

b. contains some punctuation marks

c. the text is in one sentence format

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

Original ROUGE 1.5.5.pl wrapper does not run in colab (something related to Permission denied: '/content/gdrive/My Drive/Codigos_doctorado_DUC2001/pyrouge-master_with_ROUGE155/tools/ROUGE-1.5.5/ROUGE-1.5.5.pl'). But, I installed locally in jupyter notebook. The ROUGE metric for each output summary is contained in numpy files (.npy) named ROUGE_2002_toy_example_simple (plain text), ROUGE_2002_toy_example_simple_punctuation (contains punctuation marks) and ROUGE_2002_toy_example_simple_one_line (the text is in one sentence format) for pyrouge library.

The output files from java ROUGE 2.0 are comma separated files (.csv).

**Summary results**

Toy example A text:

Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail.
Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev.
Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin.

Gold standard text:

Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail.
Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev.
Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin.

Results of toy example A

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 1 | 1 | 1 | 1 |
| ROUGE-1 precision | 0.7333 | 0.4037 | 1 | 0.7333 |
| ROUGE-1 F score | 0.8462 | 0.4037 | 0.9999 | 0.8462 |
| ROUGE-2 recall | 1 | 1 | 1 | 1 |
| ROUGE-2 precision | 0.7143 | 0.4000 | 1 | 0.7273 |
| ROUGE-2 F score | 0.8333 | 0.4000 | 0.9999 | 0.8421 |

Toy example B text:

Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail.

Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev.

Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin.

Gold standard text:

Mikhail, Mikhail, Mikhail, Mikhail, Mikhail Mikhail Mikhail Mikhail.

Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev.

Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin.

Results of toy example B

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 1 | 0.9420 | 0.5000 | 1 |
| ROUGE-1 precision | 0.7333 | 0.4037 | 1 | 0.7333 |
| ROUGE-1 F score | 0.8462 | 0.4037 | 0.6666 | 0.8462 |
| ROUGE-2 recall | 1 | 0.8824 | 0.3333 | 1 |
| ROUGE-2 precision | 0.7143 | 0.3750 | 1 | 0.7273 |
| ROUGE-2 F score | 0.8333 | 0.3750 | 0.5000 | 0.8421 |

Toy example C text:

Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Mikhail Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin.

Gold standard text:

Mikhail, Mikhail, Mikhail, Mikhail, Mikhail Mikhail Mikhail Mikhail Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Gorbachev Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin Yeltsin.

Results of toy example C

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 1 | 0.9860 | 0.7500 | 1 |
| ROUGE-1 precision | 0.7333 | 0.7460 | 1 | 0.7333 |
| ROUGE-1 F score | 0.8462 | 0.7460 | 0.8571 | 0.8462 |
| ROUGE-2 recall | 1 | 0.9719 | 0.7143 | 1 |
| ROUGE-2 precision | 0.7273 | 0.7347 | 1 | 0.7273 |
| ROUGE-2 F score | 0.8421 | 0.7347 | 0.8333 | 0.8421 |

----------------------------------------------------------------------------------------------------------------------------------------

The folder "toy example2" contains two documents to summarize and one gold standard. The first document has three sentences, the second has four sentences and the gold standard has four sentences. For this example I create four output summaries (located in "toy_example2_d1", "toy_example2_d2", "toy_example2_d3". "toy_example2_d4" folders), which contains the following:

a. The last two sentences from document one and document two

b. The sentences of both documents

c. The sentences from document one

d. The sentences from document two

The "toy_example2_model_summaries" folder contains the gold standard.

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

The ROUGE metric for each output summary is contained in numpy files (.npy) named ROUGE_2002_toy_example2_d1, ROUGE_2002_toy_example2_d2, ROUGE_2002_toy_example2_d3 and ROUGE_2002_toy_example2_d4 for pyrouge library.

The output files from java ROUGE 2.0 are comma separated files (.csv).

Document D1:

Cut to a row of dour Communists in ill-fitting gray suits announcing Gorbachev's illness and a palace coup.

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

Documento D2:

Gorbachev was set to board a plane in the Crimea, where he was vacationing at the time of Monday's coup, for the two-hour flight to Moscow, said a deputy to Russian Defense Minister Konstantin Kobets.

Earlier reports that the plane had already taken off were incorrect, officials said.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Gold standard:

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

**Summary results**

Toy example D1 text:

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

Gold standard text:

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Result of example D1:

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 1 | 1 | - | 1 |
| ROUGE-1 precision | 0.6733 | 0.6667 | - | 0.6700 |
| ROUGE-1 F score | 0.8047 | 0.6667 | - | 0.8024 |
| ROUGE-2 recall | 1 | 1 | - | 1 |
| ROUGE-2 precision | 0.6667 | 0.6637 | - | 0.6667 |
| ROUGE-2 F score | 0.8000 | 0.6637 | - | 0.8000 |

Toy example D2 text:

Cut to a row of dour Communists in ill-fitting gray suits announcing Gorbachev's illness and a palace coup.

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

Gorbachev was set to board a plane in the Crimea, where he was vacationing at the time of Monday's coup, for the two-hour flight to Moscow, said a deputy to Russian Defense Minister Konstantin Kobets.

Earlier reports that the plane had already taken off were incorrect, officials said.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Gold standard text:

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Result of example D2:

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 1 | 1 | - | 1 |
| ROUGE-1 precision | 0.4024 | 0.4021 | - | 0.3941 |
| ROUGE-1 F score | 0.5738 | 0.4021 | - | 0.5654 |
| ROUGE-2 recall | 1 | 1 | - | 0.9849 |
| ROUGE-2 precision | 0.3974 | 0.3989 | - | 0.3846 |
| ROUGE-2 F score | 0.5687 | 0.3989 | - | 0.5532 |

Toy example D3 text:

Cut to a row of dour Communists in ill-fitting gray suits announcing Gorbachev's illness and a palace coup.

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies. 

Gold standard text:

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Result of example D3:

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.6177 | 0.6053 | - | 0.6119 |
| ROUGE-1 precision | 0.7500 | 0.7667 | - | 0.7321 |
| ROUGE-1 F score | 0.6774 | 0.7667 | - | 0.6667 |
| ROUGE-2 recall | 0.5500 | 0.5333 | - | 0.5303 |
| ROUGE-2 precision | 0.6600 | 0.6780 | - | 0.6364 |
| ROUGE-2 F score | 0.6000 | 0.6780 | - | 0.5785 |

Toy example D4 text:

Gorbachev was set to board a plane in the Crimea, where he was vacationing at the time of Monday's coup, for the two-hour flight to Moscow, said a deputy to Russian Defense Minister Konstantin Kobets.

Earlier reports that the plane had already taken off were incorrect, officials said.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Gold standard:

The camera zooms in on the impassive faces of the two men last seen in Gorbachev's office.

What is going on here? OK, it's a hackneyed device that would only work in the movies.

The Soviet leader, in a statement for radio and television, said he was fully in command of the situation and that the coup leaders would bear "full responsibility" for their actions.

In the United States, President Bush hailed Gorbachev's return to power and said the coup leaders had "underestimated the power of the people, underestimated what a taste of freedom and democracy brings."

Result of example D4:

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.5000 | 0.6447 | 0.1195 | 0.6716 |
| ROUGE-1 precision | 0.2970 | 0.3798 | 0.0620 | 0.3947 |
| ROUGE-1 F score | 0.3727 | 0.3798 | 0.0810 | 0.4972 |
| ROUGE-2 recall | 0.6471 | 0.5200 | 0 | 0.5152 |
| ROUGE-2 precision | 0.3894 | 0.3047 | 0 | 0.3009 |
| ROUGE-2 F score | 0.4862 | 0.3047 | 0 | 0.3799 |

----------------------------------------------------------------------------------------------------------------------------------------
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

Finally, the output summaries for DUC 2002 using an unsupervised approach are located in "experiments_DUC2002_unsup.zip" folder, these output summaries were used for java library and (the finally results are in the "java_library_DUC2002_unsupervised.xlsx" and each output file (.csv) are located in "evaluation30_duc2002_unsupervised_java_library.rar"), pyrouge and easy-rouge libraries, "summaries_for_ROUGE_pltrdy_A_DUC2002.rar" and "summaries_for_ROUGE_pltrdy_B_DUC2002.rar" folders contain the output summaries for rouge library. In this particular case, the unsupervised approach has a code segment which depends of randomness, so I ran the experiment 30 times and the output was the average result of the 30 experiments.

In the following table the results are shown.

| ROUGE library | Java | Easy-rouge | Rouge | Pyrouge |
| --- | --- | --- | --- | --- |
| ROUGE-1 recall | 0.5279 | 0.4645 | 0.0859 | 0.3045 |
| ROUGE-1 precision | 0.2981 | 0.2856 | 0.1091 | 0.1868 |
| ROUGE-1 F score | 0.3754 | 0.2856 | 0.0874 | 0.2271 |
| ROUGE-2 recall | 0.2146 | 0.1592 | 0.0498 | 0.0291 |
| ROUGE-2 precision | 0.1219 | 0.0954 | 0.0614 | 0.0175 |
| ROUGE-2 F score | 0.1523 | 0.0954 | 0.0500 | 0.0215 |

"DUC2001_supervised_pyrouge", "DUC2002_supervised", "DUC2004_supervised_pyrouge", "DUC2001_supervised_easy_rouge" folders have the trained model for each experiment using the supervised approach.

"DUC2002_unsupervised_A.rar" and "DUC2002_unsupervised_B.rar" folders have the gold standards of DUC 2002 unsupervised experiments.

"duc2001_r1_a_supervised_pyrouge.csv", "duc2001_r1_b_supervised_pyrouge.csv", "duc2001_r2_a_supervised_pyrouge.csv", "duc2001_r2_b_supervised_pyrouge.csv" files contain the ROUGE metric of java library for DUC 2001 labeled with pyrouge library.

"duc2001_testing_r1_a_supervised_easyrouge.csv", "duc2001_testing_r1_b_supervised_easyrouge.csv", "duc2001_testing_r2_a_supervised_easyrouge.csv", "duc2001_testing_r2_b_supervised_easyrouge.csv" files contain ROUGE metric of java library for DUC 2001 labeled with easy-rouge library.

"duc2002_r1_a_supervised.csv", "duc2002_r1_b_supervised.csv", "duc2002_r2_a_supervised.csv", "duc2002_r2_b_supervised.csv" files contain ROUGE metric of java library for DUC 2002 using supervised approach.

"duc2004_r1_a_supervised.csv", "duc2004_r1_b_supervised.csv", "duc2004_r1_c_supervised.csv", "duc2004_r1_d_supervised.csv", "duc2004_r2_a_supervised.csv", "duc2004_r2_b_supervised.csv", "duc2004_r2_c_supervised.csv", "duc2004_r2_d_supervised.csv" files contain ROUGE metric of java library for DUC 2004 using supervised approach.

The notebooks (.ipynb files) contains the python implementations (easy-rouge and rouge python, both run in colab) and in their cell output we can observe the ROUGE metric.

The "model..." folders are the gold standards for each experiment.

----------------------------------------------------------------------------------------------------------------------------------------



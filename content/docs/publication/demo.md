---
weight: 10
bookFlatSection: true
title: "Demo"
---

#  Demo

## Demo website
<a href="https://graphics.cs.wisc.edu/Vis/Boxer/demo/dist/index.html" target="_blank">Click here</a> to open the online demo in a new browser tab.


## Public Datasets

|  Dataset Name| Description |Related Use case
| -| ----------- | ----------- | 
| Imputation| The Mushroom dataset that considers a testing set of 2,000 (of 8,124) randomly selected instances. | [Model Selection](../../user_guide/use_cases/3rd-level/case6)
|IMDB Confidence | The data consists of 5044 movies with 27 features, however, 25% is sequestered for final assessment. A stratified sampling of 200 movies per class is held out from the 3756 for testing.|[Model Selection and Tuning](../../user_guide/use_cases/3rd-level/case4)
|recid| This dataset is used for fair learning: the Broward County recidivism dataset, popularized by ProPublica. The data set contains 6,172 instances and 14 numeric features (created by one-hot encoding the categorical features in the initial seven feature data set). 20% are held for testing. | [Fairness Assessment](../../user_guide/use_cases/3rd-level/case2)
| date-12000-strat | The dataset is the TCP collection of historical documents. It took a random sample of 12,000 documents, and held out 30% using stratified sampling. While the testing set is balanced (1,800 per class), the training set is highly skewed (only 15% before 1642)|[Bias and Data Discovery](../../user_guide/use_cases/3rd-level/case3)
| fuzz-mod-5-02 | The data set is a collection of 554 plays written in the Early Modern Period (1470-1660). Five linguistic features are used. It contains four kinds of plays : Comedy, History, Tragedy and Tragicomedy.| [Feature Sensitivity Testing](../../user_guide/use_cases/3rd-level/case5)
| tcp-tree-select-9-10 | This dataset considers a corpus of 59,989 documents from a historical literary collection and the data counts the 500 most common English words in each document.| [Model Selection and Data Discovery](../../user_guide/use_cases/3rd-level/case1)
| (continuous) wine quality | The dataset is used for wine quality classification, which requires classifying the quality of a wine from its properties. | [(Continuous) Hyper parameter Tuning](../../user_guide/use_cases/3rd-level/case7)
|(continuous) income | The dataset comes from income classification benchmark dataset from that has been downsampled. Classifiers determine whether an individual???s income is above a certain level. | [(Continuous) Model Selection](../../user_guide/use_cases/3rd-level/case9)
|  (continuous) cifar-sampled-scaling | The datset is created based on CIFAR 100 computer vision benchmark using Tensorflow. The data set has 100 classes, and the trained classifier produces a distribution over these classes as its decision.A binary classifier has been created for a ???meta-class??? which combines 5 of the main classes. This datasets aims to classify flowers, which can be any one of 5 of the original classes. Because the test set contains all 100 classes, it is quite imbalanced: flowers are only 5% of the total instances |   [(Continuous) Model Selection and Detail Examination](../../user_guide/use_cases/3rd-level/case20)
|(continuous) cdate-2500 | This dataset considers a corpus of 59,989 documents from a historical literary collection: Text Creation Partnership (TCP) transcriptions of the Early English Books Online (EEBO). The data counts the 500 most common English words in each document. For the experiment, we took a random sample of 2500 documents, and held out 30% using stratified sampling.  | [(Continuous) Data Examination](../../user_guide/use_cases/3rd-level/case8)

<!-- | (continuous) heart disease | This dataset is a standard data set used in machine learning education. The scenario is an example where the cost of a false negative error (not warning a patient of a potential problem) is more costly than a false positive (which may cause extra caution, or fear).  | to be updated -->
---
weight: 7
bookFlatSection: true
title: "(Continuous) Model Selection and Detail Examination"
---

 
### **Model Selection and Detail Examinationt**
  This use case shows how our approach can help with model selection and threshold tuning. A classifier was built for the CIFAR 100 computer vision benchmark using Tensorflow.

  - Dataset: 
   In this example, we have a dataset of various flower images. The dataset has 100 classes. Our goal is to create a binary classifier for a “meta-class” which combines 5 of the main classes. In particular, we want to classify flowers, which can be any one of 5 of the original classes. Because of this, the dataset is quite imbalanced: flowers are only 5% of the total instances.

  - Classifier: 
   The classifiers were created using three different strategies that combine the base classes: sum, average, and largest. Because of the class imbalance, we use Mathews Correlation (MCC) as the metric. Each combination strategy produces different ranges of scores.

  - Walkthrough: 
  
    ![Example image](../../../../../image/cifar.png)

    After loading the dataset, we opened the *Reliability Curve view (A)*, *Bandwidth Assessment view (B)*, *Rejection Curve view (C)*, *Trinary Distribution view (E)*, and *Focus Item view (F)*.

    &emsp;
    &emsp;
    &emsp;
    &emsp;
    &emsp;
    &emsp;
    &emsp;
    &emsp;
  
    ***

    ![Example image](../../../../../image/cifarA.png)

    Each combination strategy produces different ranges of scores. We can use the *Reliability Curve view* to see the differences, and estimate appropriate thresholds for each.

    &emsp;

    ![Example image](../../../../../image/cifarB.png)
    For each model, we use the *Bandwidth Assessment view* to choose a threshold that provides high MCC yet provides a range of available rejection rates.

    &emsp;

    ![Example image](../../../../../image/cifarC.png)
    The *Rejection Curve view* shows that each model gets a performance gain from a 10% rejection rate. After tuning each model appropriately all have similar performance.

    &emsp;

    ![Example image](../../../../../image/cifarE.png)
    Using the *Trinary Distribution view* we can make selections to look for differences in the similar performance. We note that while each model rejects the same number of items, they reject different items. While the number of errors is small, they are different between models. One model has more false positives, while the other has more false negatives.

    &emsp;

    ![Example image](../../../../../image/cifarF.png)

    We select the false positives of the largest model. The *Focus Item view* allows us to step through these errors to look for patterns. We notice that many of the errors are flowers with insects on them. Because these images are labeled as insect, they are scored as misclassified.
    


---
weight: 5
bookFlatSection: true
title: "(Continuous) Hyper parameter Tuning"
---


### **Hyper parameter Tuning**

- Dataset: The scenario uses wine quality benchmark from UCI Machine Learnng Repository, which requires classifying the quality of a wine from its properties.

- Classifiers: Because we are trying to determine a hyper-parameter, we perform this analysis using the training data. We build a random forest
classifier, and find that it gives good performance over a range of
thresholds. We want to understand if changes in the threshold affect
the outcomes

- Walkthrough:

    After loading the data, let's first open the *Bandwidth Assessment* view.
    ![Example image](../../../../../image/wine-1.png)


    We see that the accuracy is constant for thresholds around .5. Then we use the *Probability Control panel* to adjust the threshold. 
    ![Example image](../../../../../image/wine-2.png)


    For several values in the range, we create new classifiers that use the same model with different
    thresholds (.5, .55, .6, .65) and compare these models. 
    ![Example image](../../../../../image/wine-3.png)


    We see that accuracy, F1 and MCC scores are very similar across the four.
    ![Example image](../../../../../image/wine-4.png)


    However, if we select the errors (left click to select the errors when threshold is .5, and right click to select the errors when threshold is .6), we see that they are different: 
    ![Example image](../../../../../image/wine-5.png)


    For the lower thresholds, there are more false negatives, while for the higher thresholds more false positives. *Trinary Instance Distribution* view also shows this.
    ![Example image](../../../../../image/wine-6.png)


    In conclusion, this classifier is quite sensitive to small changes in the threshold, even though those changes do not affect the most common metrics.

  
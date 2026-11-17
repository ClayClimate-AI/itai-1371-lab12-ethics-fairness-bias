# Reflection Journal: Lab 12, Ethics, Fairness, and Bias in ML

**Course:** ITAI 1371  
**Name:** Joseph Clay

---

## Results at a Glance

| Metric | Men | Women | Gap |
|---|---|---|---|
| Accuracy | 81.20% | 91.81% | 10.61 points |
| False Positive Rate (FPR) | 10.26% | 2.81% | 7.45 points |
| False Negative Rate (FNR) | 37.80% | 47.84% | 10.04 points |

Overall model accuracy: **84.61%**

---

## Looking Beyond Overall Accuracy

This lab helped me understand that evaluating a machine learning model involves more than looking at its overall accuracy. At first, a single accuracy score of 84.61% seemed like a good measure of performance, but I learned that it can hide important differences in how the model performs for different groups of people.

## Comparing Groups

By comparing the model's accuracy for men and women separately, I saw that one group could receive more incorrect predictions than another. The model was 81.20% accurate for men and 91.81% accurate for women, a gap of 10.61 percentage points. This showed me that a model can appear successful overall while still producing unequal outcomes.

I also learned that a higher accuracy score for one group does not automatically mean the model is fair. Sometimes a model can achieve high accuracy simply by making the most common prediction rather than accurately identifying individuals. Women had the highest accuracy (91.81%), but they also had the highest false negative rate (47.84%), meaning nearly half of the women who actually earned over $50K were missed by the model.

## False Positives and False Negatives

The most important concept I learned was the difference between false positives and false negatives. These error types helped me understand not only how often the model was wrong, but also who might be affected by those mistakes. Men had a higher false positive rate (10.26% vs. 2.81%), while women had a higher false negative rate (47.84% vs. 37.80%). Depending on the application, such as hiring or lending decisions, different types of errors can have significant consequences for people.

## Conclusion

Overall, this lab demonstrated the importance of examining subgroup performance and error rates when evaluating machine learning systems. It showed me that fairness cannot be determined by overall accuracy alone and that a deeper analysis is necessary to identify potential bias and ensure that models treat different groups equitably.

## Deployment Decision

I would not approve this model for deployment in a hiring context. Although the model achieves reasonably high overall accuracy (84.61%), the substantial performance gap between demographic groups (10.61 points in accuracy and 10.04 points in false negative rate) suggests disparate impact. Differences in subgroup accuracy and error rates may lead to unequal treatment of applicants. Additionally, removing the sex attribute would not fully eliminate bias because other correlated features can serve as proxy variables. Before deployment, fairness mitigation techniques such as reweighting, feature auditing, and subgroup-based evaluation should be performed to reduce the risk of discriminatory outcomes.

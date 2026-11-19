
# Module 11 Lab – Hyperparameter Tuning and AutoML
## Group 4 – Reflection Journal
**Course:** ITAI 1371 – Introduction to Machine Learning

---

### Member 1: Patrick Rostand Gandjouon Tchassem

**Reflection:**

This lab helped me understand why hyperparameter tuning is important in machine learning. Before working on this assignment, I thought that once a model was trained and gave a good accuracy score, there was not much else to do. After completing the lab, I realized that we can adjust different settings to see how they affect the model's performance.

One part I found interesting was comparing Grid Search and Random Search. Grid Search tested every combination we provided, while Random Search selected combinations from a larger range. In our results, both methods achieved 94.29% cross-validation accuracy, even though they selected different hyperparameters. This helped me understand that there can be more than one good combination of settings for the same dataset.

I also learned something important from the baseline model. It achieved 100% accuracy on the test data, but the tuning methods gave lower cross-validation scores. At first, that seemed confusing. I learned that these scores come from different evaluation methods, so they should not be compared as if they measured exactly the same thing.

Another interesting part was using AutoGluon. Instead of manually selecting and tuning one algorithm, AutoGluon trained and compared several models automatically. Seeing the leaderboard helped me understand how AutoML can save time and make the machine-learning workflow easier to manage. I also noticed that the model selected using validation results was not necessarily the one with the highest test accuracy.

Overall, this lab improved my understanding of hyperparameters, model evaluation, and automation. It also helped me become more comfortable running Python code in Google Colab, troubleshooting errors, and reviewing the results instead of just focusing on whether the code runs.

---

### Member 2: Kenneth Kouokam

For Module 11, my role is interpreting the baseline and evaluation results. The two reported
percentages raise an interesting question: why would a baseline model score 100% while the tuning
methods report 94.29%? Looking only at the numbers could suggest that tuning made the model
worse. Understanding where each score comes from gives me a different explanation. The scores
describe different evaluations, so I need to examine the data used for each before drawing a
conclusion.

The baseline uses 105 Iris examples for training and 45 for testing. Its reported 100% test accuracy
means that it correctly classified those 45 flowers. That is a useful result, but it is still based on a
small set of observations. A single mistake would reduce the score to about 97.8%. This connects to
the earlier ensemble lab: a perfect score on one split does not settle which model will be more reliable
when the examples change.

The tuning scores come from five-fold cross-validation within the 105 training examples. For each
candidate setting, the process repeatedly trains on four folds and evaluates on the remaining fold. In
this setup, each fit uses 84 examples and validates on 21. This is different from fitting the baseline on
all 105 training examples and evaluating on the separate test set. The average validation score helps
compare candidate settings, but it should not be treated as the same measurement as the baseline
test accuracy.

The matching 94.29% scores from Grid Search and Random Search also need careful interpretation.
They tell me that the best reported average scores were equal at the displayed precision. They do not
establish that both searches selected identical settings or made the same predictions. To understand
the comparison more fully, I would want to examine the best parameters and the scores across the
individual folds. Those details would help explain a tie instead of assuming that the two search
methods behaved identically.

My main takeaway is that a score only becomes useful when I understand how it was produced.
Hyperparameter selection should use training and validation data, while the test set should remain
separate for final evaluation. Repeatedly changing settings after inspecting test results would weaken
that separation. For a fair comparison, I would evaluate the baseline and selected tuned models
under matching conditions and explain both the results and their limits. This role helps me connect
the idea of tuning to the practical question of whether a comparison actually supports the conclusion
being made.

### Member 3: [Enter Full Name]

**Reflection:**

---

### Member 4: [Enter Full Name]

**Reflection:**

---

### Member 5: [Enter Full Name]

**Reflection:**


---
